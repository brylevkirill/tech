Freebase
	Freebase - Google's public RDF compatible database

	http://mql.freebaseapps.com/ch03.html - MQL for reading sub-graph of object graph
	http://mql.freebaseapps.com/ch05.html - MQL for writing sub-graph of object graph
	http://freebase.com/docs/data - Freebase API

	http://rpbouman.blogspot.com/2011/01/mql-to-sql-json-based-query-language_07.html - quick introduction
	http://vimeo.com/4269223# - quick video introduction
	http://freebase.com/queryeditor - live query editor and samples
	http://freebase.com/view/freebase/freebase_query - more samples


	MQL query language:
	- comparison with SQL - http://code.google.com/p/mql-to-sql/wiki/SampleMQLQueries
	- query serialization into URL and support for paging - http://wiki.freebase.com/wiki/MQL_Read_Service
	- easy to implement on top of relational database - http://code.google.com/p/mql-to-sql/
	- easy to implement on top of graph database

	https://github.com/michael/data - JS library for operations on resource graph with Freebase schema


	schema:

	http://slideshare.net/jamietaylor/freebase-schema

	- object identifiers:
	    * UUID for object ("guid" property of object)
	    * zero or more unique fully-qualified names for object ("id" property of object is set to one of them and can default to UUID) from single or multiple namespaces
	    * non-unique user-friendly name for object ("name" property of object)

	- value-type properties (literals) and object-type properties (links) of object        #! semantics of "resource relations" concept
	- small set of value-type properties: /type/int, /type/float, /type/boolean, /type/text, /type/rawstring, /type/uri, /type/datetime, /type/key, /type/id
	- unique and non-unique (multi-value) properties for object, all values of non-unique property have to be different from each other        #! semantics of "resource collection relation" concept + semantics of "multi-value attribute of resource"
	- "order" optional system property for each value (which is a link) of non-unique (multi-value) object-type property of object        #! semantics of "ordered resource collection link" concept
	- default property of object type (property of object which value can be used as text representation of object in cases when representation of object as JSON map of properties is not needed and thus inconvenient) - "name" property as default property for object of any types other than built-in, "value" as default property for value-type (literal) property
	- automatic bidirectionality of properties - presense of reverse (reciprocal) property for each object-type property (link) and for each value-type property
	- possibility either to have explicit name for reverse property (/music/artist/album reverse property for /music/album/artist master property) or to identify reverse property using name of master property using "!" operator (!/music/album/artist)        #! semantics of "strong link" and "weak link" concepts

	- zero or more types explicitly associated with object (default type /type/object is implicitly assumed for any non-system object)
	- "expected_type" property is defined for object property (in /type/property object), although value of object property is allowed to be set to object of any type, because expected type for property of object is never enforced in any way and is only used by MQL, when particular type or types are explicitly specified in query to constraint set of object properties to those which are defined in schemas for those types - so that it is possible for query either to force strict typing or to use duck typing

	- any object can be used as namespace for object, every object is linked or chain-linked to some object of /type/namespace (at most root namespace object)
	- one or more fully-qualified names for each namespace object
	- namespaces as collections of objects, optional support for enforcing unicity of objects (by user-friendly name) in namespace        #! semantics of "not linked resource collection" and "resource membership in collection" concepts
	- "enumeration" type for property of object for constraining possible values of property to be among fully-qualified names in particular namespace (specified as property of property of "enumeration" type), so that value of this property must point to element of namespace and each value of property gets exposed as element of namespace automatically in case of presence of permissions to modify namespace        #! semantics of "restricted resource collection" concept + semantics of "automatic publishing in collection" concept

	- built-in support for localization via "lang" property of any property with text type (such as "name" property for each object)
	- "timestamp" and "creator" properties for objects and links
	- "valid" and "operation" properties for objects and links, possibility to explore history of revisions for objects and links
	- objects and links live in storage forever even after deletion, possibility to work with storage snapshot corresponding to given timestamp from the past



	read query:

	* possibility to retrieve sub-graph of objects graph or its projections in single read query
	* query by example, symmetry of query and result - possibility to construct new queries from previously returned results (as opposed to SQL where query language is an algebra and result is table data)

	- "*":null - reflecting on list of object properties accordingly to expected type of object (static typing), returning default property for each property ("name" for /type/object and non-system types, "id" for /type/lang)
	- "/type/reflect/any_master", "/type/reflect/any_reverse", "/type/reflect/any_value" - reflecting on list of object properties regardless of expected type of object (duck typing)
	- "name":{} - reflecting on value-type property (literal), returning ("type", "value") properties for each property
	- "type":[{}] - reflecting on object-type (link) property, returning ("id", "name", "type") properties for each property
	- "*":{} or semantically equivalent "*":[{}] - reflecting on list of object properties and properties of those properties at the same time ([{"*":{}}] is possible while [{"*":{"*":null}}] is not possible)
	- when reflecting on properties of object, type(s) of object can be specified explicitly in query (static typing) or otherwise inferred automatically (duck typing)
	- "link":{} - reflecting on links to sub-queries ("source", "target", "target_value", "reverse", "master_property" properties of object-type property), which are links from object in sub-query (containing "link" directive) to object in parent query
	- "type":"/type/link" - reflecting on links in top-level queries

	- INTERSECT SQL operator semantics by means of prefixes for queries, UNION SQL operator semantics by means of array of queries
	- "limit":N - limiting or pruning (in case of 0) objects returned for sub-query
	- "return":"count" and "return":"estimate-count" - returning number of objects instead of objects
	- "count":null and "estimate_count":null - returning number of objects together with objects
	- "sort":["a","b"] - ordering objects by values of set of properties (of object in query or in sub-queries at any level)
	- "index":null - returning partial order for values of non-unique (multi-value) object-type (link) property
	- "...>", "...~=", "...|=", "...!=" operators to specify constraints for value-type properties (literals) or default properties of object-type properties
	- "optional":"optional" or "optional":true - not pruning objects found for enclosing query if no objects are found for sub-query (containing directive) + including objects found for sub-query into results for enclosing query
	- "optional":"forbidden" - pruning objects found for enclosing query if any objects are found for sub-query (containing directive)



	write query:

	* possibility to modify sub-graph of objects graph in single write query
	* prohibited to request certain properties of certain objects to be returned in results for write query similar to read query, except "id" property (although it is possible to introduce such behavior)

	- directives for object:
	    * "create":"unless_exists" (find existing object or otherwise create new one)        #! semantics of "acquire" operation without "link" operation
	    * "create":"unless_exists" (drop existing link + link existing object or otherwise create and link new object)        #! semantics of "acquire" operation with "link" operation
	    * "create":"unless_connected" (leave existing link or otherwise create and link new object)
	    * "create":"unconditional" (create new object)
	  return statuses: "create":"created", "create":"existed", "create":"connected"

	- directives for link:
	    * "connect":"insert" (create new link)
	    * "connect":"update" (create or change link for unique property)
	    * "connect":"replace" ("insert" for non-unique property or "update" for unique property)
	    * "connect":"delete" (delete link)
	  return statuses: "connect":"inserted", "connect":"updated", connect":"present", "connect":"deleted", "connect":"absent"

	- "index":N - assigning optional partial order for value of non-unique (multi-value) object-type (link) property
	- "key":{"namespace":null,"value":null} - possibility to either assign or re-assign fully-qualified name in given namespace to some object and possibility to assign fully-qualified name in some namespace for given object - both operations handle link from object to namespace object and reverse link and have reciprocal effect on those links
	- manipulation with security model via operations on object graph (user groups and permission groups, per-object and per-property access control for links and namespaces)




<brylevkirill@gmail.com>
