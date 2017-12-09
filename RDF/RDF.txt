 * technologies in RDF stack
 * introduction to RDF
 * RDF data model
 * RDF technologies/specifications
 * RDF description of RESTful API
 * RDF major applications
 * RDF service/data integration platforms
 * RDF schemas/vocabularies/ontologies
 * RDF knowledge bases
 * RDF in the wild
 * RDF stack features
 * RDF databases
 * RDF libraries and tools
 * articles about RDF




[technologies in RDF stack (overviews)]

  - https://github.com/brylevkirill/tech/blob/master/RDF/schema.org.txt
  - https://github.com/brylevkirill/tech/blob/master/RDF/JSON-LD.txt
  - https://github.com/brylevkirill/tech/blob/master/RDF/OWL.txt
  - https://github.com/brylevkirill/tech/blob/master/RDF/SPARQL.txt
  - https://github.com/brylevkirill/tech/blob/master/RDF/LDP.txt
  - https://github.com/brylevkirill/tech/blob/master/RDF/R2RML.txt
  - https://github.com/brylevkirill/tech/blob/master/RDF/Hydra.txt




[introduction to RDF]

	* RDF - framework for description of data related to resource in a way which doesn’t require prior knowledge of the vocabularies being used
	* Linked Data - powerful distributed open graph data model based on RDF to integrate data stored in various databases and to integrate applications around data

	Data (observing and recording, RDF) -> Information (organizing, RDFS/OWL) -> Knowledge (understanding, semantics) -> Wisdom (predicting)


	"What happened to the Semantic Web?" - https://slideshare.net/pmika/what-happened-to-the-semantic-web


	introduction into modern RDF - http://youtube.com/watch?v=vioCbTo3C-4

	"Key Things You Need to Know About RDF and Why They Are Important" - http://dbooth.org/2014/key/key-slides.pdf

	"Linked Data: Introduction and Application Scenarios" - http://euclid-project.eu/modules/chapter1 + http://euclid-project.eu/modules/course1
	"Querying Linked Data" - http://euclid-project.eu/modules/chapter2 + http://euclid-project.eu/modules/course2
	"Providing Linked Data" - http://euclid-project.eu/modules/chapter3 + http://euclid-project.eu/modules/course3
	"Interaction with Linked Data" - http://euclid-project.eu/modules/chapter4 + http://euclid-project.eu/modules/course4
	"Creating Linked Data Applications" - http://euclid-project.eu/modules/chapter5 + http://euclid-project.eu/modules/course5

	http://habrahabr.ru/company/itis/blog/258405/  (course in russian)


	http://slid.es/mhgrove/semantic-graphs-are-for-everyone
	http://mkbergman.com/1626/seven-arguments-for-semantic-technologies/
	http://slideshare.net/lanthaler/stop-reinventing-the-wheel-use-linked-data-to-build-better-ap-is

	http://semanticweb.com/the-business-value-of-reasoning-with-ontologies_b38364
	https://dropbox.com/s/01ii0nnzeomnepa/Linked%20Data%20Platform%20as%20a%20novel%20approach%20for%20Enterprise%20Application%20Integration.pdf
	https://dropbox.com/s/fi4zq9vjc2bhgu0/Linked%20Data%20in%20the%20Enterprise.pdf


	interesting selected publications - https://dropbox.com/sh/c427b94xex62a40/AABii9_MRHrCZPGJ_Adx_b3Ma




[RDF data model]

	RDF data model features (with comparison to APS data model) - https://dropbox.com/s/zuomah695zntjv7/RDF%20data%20model.txt

	"How RDF Databases Differ from Other NoSQL Solutions" - http://blog.datagraph.org/2010/04/rdf-nosql-diff

	what's new in RDF 1.1 - http://slideshare.net/cygri/whats-new-in-rdf-11
	diagram and overview for entity types in RDF/RDFS/OWL - http://infowebml.ws/website/graphical-representations.htm

	hypergraph extension to RDF data model - http://arxiv-web3.library.cornell.edu/abs/1406.3399
	reconciliation of RDF model and Property Graph model - http://arxiv.org/pdf/1409.3288v1.pdf




[RDF technologies/specifications]

	[types]
		Schema.org (collection of type schemas) -
			http://schema.org
			https://github.com/brylevkirill/tech/blob/master/RDF/schema.org.txt
			https://dropbox.com/s/pefw66f8vjft3p5/schema.org%20intro.txt
	[serializations]
		JSON-LD (JSON serialization) - http://json-ld.org + https://github.com/brylevkirill/tech/blob/master/RDF/JSON-LD.txt
		Turtle (most comprehensible serialization) - http://w3.org/TR/2013/CR-turtle-20130219/
		RDFa (serialization into HTML) - http://rdfa.info
		HDT (binary serialization) - http://rdfhdt.org/what-is-hdt/
		RDF Patch (graph delta serialization) - http://bertails.org/2014/09/20/why-ldpatch/ + http://w3.org/TR/ldpatch/ + http://afs.github.io/rdf-patch/
	[API]
		Hydra (REST API definition) - http://hydra-cg.com/spec/latest/core/ + https://github.com/brylevkirill/tech/blob/master/RDF/Hydra.txt
		Linked Data Fragments (SPARQL to REST) - http://linkeddatafragments.org + https://dropbox.com/s/33r12d8khfia2p2/Linked%20Data%20Fragments.txt
		Linked Data Platform (REST API) - https://github.com/brylevkirill/tech/blob/master/RDF/LDP.txt
		RDF Interfaces (programming language API) - http://w3.org/TR/2012/NOTE-rdf-interfaces-20120705/
	[query]
		SPARQL (query language) - http://w3.org/TR/rdf-sparql-query/ + https://github.com/brylevkirill/tech/blob/master/RDF/SPARQL.txt
		LDPath (simple query language) - http://wiki.apache.org/marmotta/LDPath
	[schema]
		RDF Schema (basic schema definition) - http://w3.org/TR/rdf-schema/
		OWL (schema definition) - http://w3.org/TR/owl-features/ + https://github.com/brylevkirill/tech/blob/master/RDF/OWL.txt
	[validation]
		Shapes Constraint Language - http://w3c.github.io/data-shapes/shacl/ + http://w3c.github.io/data-shapes/data-shapes-primer/
	[rules]
		Notation 3 (most comprehensible serialization) - http://w3.org/DesignIssues/Notation3
		SPIN (simple schema) - http://spinrdf.org/spin.html
		RIF (complex schema) - http://w3.org/2005/rules/wiki/RIF_FAQ + http://w3.org/TR/2013/NOTE-rif-primer-20130205/
	[data mapping]
		RDB2RDF/R2RML (relational to RDF) -
			http://w3.org/2001/sw/rdb2rdf/wiki/Main_Page
			http://w3.org/TR/r2rml/
			https://github.com/brylevkirill/tech/blob/master/RDF/R2RML.txt
	[security]
		Credentials (identity, authentication, authorization) -
			http://opencreds.org
			https://dropbox.com/s/mv3om35ojy6krl1/Credentials%20intro.txt
		WebID (identity, authentication) - http://w3.org/wiki/WebID
		WAC (authorization) - http://w3.org/wiki/WebAccessControl
	[provenance]
		PROV-O (context for graphs) - http://w3.org/TR/prov-o/




[RDF description of RESTful API]

	Hydra -
		https://github.com/brylevkirill/tech/blob/master/RDF/Hydra.txt
		http://hydra-cg.com/spec/latest/core/
		http://markus-lanthaler.com/hydra/
		http://markus-lanthaler.com/research/creating-3rd-generation-web-apis-with-hydra.pdf 
	RESTDesc -
		http://restdesc.org
		http://slideshare.net/RubenVerborgh/distributed-affordance-21175728
		http://ruben.verborgh.org/phd/
	semantic workflow engine on top of RESTDesc -
		http://ruben.verborgh.org/publications/coppens_cold_2013/
	OSLC - https://dropbox.com/s/9zpw2zipn1v0p9a/OSLC.txt




[RDF major applications]

	- emerging agreements around schemas (Schema.org, Facebook Open Graph Protocol)
	- large amounts of data published in RDF (as Linked Data, inside HTML pages, inside email text messages)
	- private knowledge graphs inside corporations

	* knowledge bases for web search engines
		http://searchengineland.com/search-answers-knowledge-graphs-galore-163217

	* semantic search
		"Now, Google, the world’s most popular search engine, will focus more on trying to understand the meanings of and relationships among things, as opposed to its original strategy of matching keywords."
			http://bits.blogs.nytimes.com/2013/09/26/google-changes-search-to-handle-more-complex-queries/
			http://searchengineland.com/future-seo-understanding-entity-search-172997
			http://searchengineland.com/5-ways-to-unlock-the-benefits-of-semantic-search-hummingbird-175634

		http://gigaom.com/2013/11/24/lets-build-a-semantic-web-by-creating-a-wikipedia-for-relevancy/

		information extraction and semantic search
			http://openie.cs.washington.edu
			https://youtube.com/watch?v=csWh3iUDE-I

		http://slideshare.net/TomAnthony/the-evolution-of-search
		http://slideshare.net/pmika/related-entity-finding-on-the-web
		http://glimmer.research.yahoo.com

		knowledge extraction platform (application search by functionality) - http://appcrawlr.com/app/technology

		transformation of natural language query to SPARQL query -
			http://treo.deri.ie - entity search, spreading activation search, distributional semantic relatedness
			http://quepy.machinalis.com + https://bel-epa.com/posts/taking-quepy-for-a-spin.xml

	* publishing data on the web
		organizing the world's scientific information - https://standardanalytics.io + http://semanticweb.com/building-scientific-knowledge-graph_b43294

	* expert systems
		IBM Watson - http://videolectures.net/eswc2012_welty_watson/

	* intelligent web agents
		http://ruben.verborgh.org/blog/2013/05/31/towards-serendipitous-web-applications/
		http://ruben.verborgh.org/blog/2013/01/31/what-web-agents-want/
		http://ruben.verborgh.org/publications/verborgh_web_2013/

	* exploratory search and discovery
		http://discoveryhub.co
		Wikipedia browser demo - http://youtube.com/watch?v=S81ovcr_pPU
		http://slideshare.net/ncmarie/discovery-hub-an-exploratory-search-engine-on-the-top-of-dbpedia
		http://slideshare.net/fabien_gandon/discovery-hub-onthefly-linked-data-exploratory-search

	* personalization (interests graph)
		http://about.primal.com/about/technology

	* shared distributed data space for applications
		http://youtube.com/watch?v=3mIv6LlmCJ4

		"Socially Aware Cloud Storage" design by Berners-Lee - http://w3.org/DesignIssues/CloudStorage.html

		RWW.IO - personal data space (linked data store) with implementation of W3C SPARQL and W3C LDP API
			https://github.com/deiu/rww.io
			calendar application - https://plus.google.com/110661547709905058143/posts/eYbge1AJoMJ

		CrossCloud - personal data space (linked data store)
			https://github.com/sandhawke/crosscloud/
			http://knightfoundation.org/blogs/knightblog/2013/6/25/introducing-crosscloud-project-get-your-data-out-silos/
			http://w3.org/2014/Talks/0605-sandro/Crosscloud%20W3C%20Tech%20Talk.pdf
			http://w3.org/2012/Talks/0320-crosscloud-sandro/

			Cimba microblogging application integrated with RWW.IO - https://youtube.com/watch?v=z0_XaJ97rF0

			Linked Data Platform features wishlist for CrossCloud - http://lists.w3.org/Archives/Public/public-ldp-wg/2014Nov/0010.html

		OpenLink Data Spaces - named structured data cluster within a distributed data network where each data item has a unique id
			http://openlinksw.com/dataspace/doc/kidehen@openlinksw.com/weblog/kidehen@openlinksw.com%27s%20BLOG%20%5B127%5D/1662
			http://ods.openlinksw.com/wiki/ODS/

		global entity registry system - http://worldwidesemanticweb.org/projects/entity-registries/

	* social activity
		http://w3.org/Social/

	* natural language processing
		OpenCalais - http://opencalais.com/about + http://opencalais.com/documentation/opencalais-web-service-api/interpreting-api-response/rdf
		AlchemyAPI - http://alchemyapi.com/api/entity-extraction/ + http://alchemyapi.com/api/relation-extraction/ + http://alchemyapi.com/api/linked-data-support/

	* data platforms for biology, chemisty and medicine
		visual builder of query as graph - http://sparqlgraph.i-med.ac.at
		overview
			http://cambridgesemantics.com/solutions/pharma/competitive-intelligence/webinar
			http://chembionavigator.org/tutorial
		http://openphacts.org




[RDF service/data integration platforms]

	OASIS OSLC and Jazz for Service Management by IBM, enterprise cloud service integration platform
		https://dropbox.com/s/9zpw2zipn1v0p9a/OSLC.txt
	FluidOps eCloudManager, enterprise cloud applications automation platform
		https://dropbox.com/s/3rcazmszvubgdnq/FluidOps
	Scorpio4 - http://scorpio4.com + https://github.com/scorpio4/scorpio4/wiki
	PoolParty, enterprise linked data integration and management
		addressed problem - http://poolparty.biz/portfolio-item/enterprise-linked-data-integration-poolparty/
		http://poolparty-software.com/see-how-it-works/
		http://poolparty-software.com/poolparty-functionalities-and-features-at-a-glance/
		http://poolparty-software.com/solutions/
		http://youtube.com/watch?v=Pj0Uh0x4yos + http://youtube.com/channel/UC51b4InJT5EzbpwCIaO0-XQ




[RDF schemas/vocabularies/ontologies]

	schema.org - http://schema.org - by Google, Yahoo, Microsoft, Yandex
		schemas for multiple knowledge domains understandable by web seach engines and many others
		currently used on 15% of all pages on the web after 2 years of adoption

		https://github.com/brylevkirill/tech/blob/master/RDF/schema.org.txt
		technical overview - http://w3.org/2013/04/odw/odw13_submission_53.pdf
		current state of adoption - http://videolectures.net/iswc2013_guha_tunnel/

	Good Relations - http://purl.org/goodrelations/
		the most popular vocabulary for product, price and company data that can be embedded into existing static and dynamic Web pages
		and that can be processed by the latest generation of search engines, recommender systems, and other novel applications

		partially included into schema.org - http://blog.schema.org/2012/11/good-relations-and-schemaorg.html

		design - http://heppnetz.de/ontologies/goodrelations/v1#uml
		catalog of over 300000 product types - http://productontology.org

	people and organizations - http://w3.org/TR/vcard-rdf/
	Organization Ontology - http://w3.org/TR/vocab-org/
	Description of a Project - https://github.com/edumbill/doap
	Internet of Things Database - https://iotdb.org
	enterprise cloud services management by FluidOps - http://fluidops.com/ontologies/
	HTTP protocol - http://w3.org/TR/HTTP-in-RDF10/




[RDF knowledge bases]

	Google Knowledge Graph (570m items, 3.5b links, 1500 item types, 35k link types) and Freebase (40m items, 2b statements, 60000 properties)
		http://technologyreview.com/news/523846/how-a-database-of-the-worlds-knowledge-shapes-googles-future/
 		Freebase as base - https://developers.google.com/freebase/ + https://github.com/brylevkirill/tech/blob/master/RDF/Freebase.txt + http://basekb.com
	Facebook Entity Graph (1b persons and other entities, 100b+ statements)
		public RDF API
			http://semantic-web-journal.net/content/facebook-linked-data-graph-api
			http://lists.w3.org/Archives/Public/public-lod/2011Oct/0032.html + http://lists.w3.org/Archives/Public/public-lod/2011Sep/0092.html
	Microsoft Satori RDF graph (300m items, 800m statements) + Microsoft Bing as Platform
		Trinity graph database for RDF data with SPARQL end-point - http://research.microsoft.com/apps/pubs/default.aspx?id=183717
			http://research.microsoft.com/en-us/projects/graphengine/ + http://graphengine.io
		Bing Entity public API - http://bing.com/blogs/site_blogs/b/search/archive/2013/06/26/bingbuild.aspx
		http://techcrunch.com/2014/03/30/microsoft-has-big-plans-for-bings-entity-engine/
	Yahoo Knowledge Graph (10m items, 10m statements, 30m properties)
		http://semtechbizsj2014.semanticweb.com/sessionPop.cfm?confid=82&proposalid=6452
		http://semanticweb.com/at-semtechbiz-knowledge-graphs-are-everywhere_b37724
	DBPedia by Wikipedia (3.6m items, 1b statements, 500 classes, 2000 properties)
		http://dbpedia.org/Datasets
	Wikidata by Wikipedia (15m items, 30m statements, 900 properties)
		http://cacm.acm.org/magazines/2014/10/178785-wikidata/fulltext
		http://meta.wikimedia.org/wiki/Wikidata/Development/RDF + http://korrekt.org/papers/Wikidata-RDF-export-2014.pdf
		https://www.mail-archive.com/wikidata-l@lists.wikimedia.org/msg05601.html
		https://lists.w3.org/Archives/Public/public-sparql-dev/2015JanMar/0031.html
	Yago
		http://mpi-inf.mpg.de/yago-naga/yago/
	ConceptNet (2.5m items, 7.5m statements)
		https://github.com/commonsense/conceptnet5/wiki
	LinkedGeoData - OpenStreetMap data (1b items, 20b statements)
		http://linkedgeodata.org

	LOD cloud cache by OpenLink (150b statements)
		http://lod.openstatementsw.com + http://lod.openstatementsw.com/b3s/
	FactForge by OntoText (500m items, 3b statements)
		http://factforge.net + http://ontotext.com/factforge

	structured data from sites on the web (17b statements) - http://lists.w3.org/Archives/Public/public-vocabs/2014Apr/0002.html




[RDF in the wild]

	samples of SPARQL queries -
		http://factforge.net/sparql
		http://lod.openlinksw.com/b3s/
		http://linkedlifedata.com/sparql
		http://code.google.com/p/void-impl/wiki/SPARQLQueriesForStatistics
	SPARQL sexy end-points with query validation -
		http://yasgui.laurensrietveld.nl
		http://sparqlbin.com
	list of public SPARQL end-points - http://labs.mondeca.com/sparqlEndpointsStatus/

	locator of all link paths between two entities on the RDF web - http://goo.gl/E7TSNY

	transformation of natural language query to SPARQL query - http://quepy.machinalis.com

	open process for data modelling in WikiData community - http://wikidata.org/wiki/Wikidata:Property_proposal/all




[RDF stack features]

	* RDF databases (see list of databases below)
		"How RDF Databases Differ from Other NoSQL Solutions" - http://blog.datagraph.org/2010/04/rdf-nosql-diff
		performance of SPARQL in Virtuoso RDF store vs SQL in analytics benchmark - http://goo.gl/0Q38OV

	* Linked Data platforms
		https://dropbox.com/s/01ii0nnzeomnepa/Linked%20Data%20Platform%20as%20a%20novel%20approach%20for%20Enterprise%20Application%20Integration.pdf

		W3C Linked Data Platform - https://github.com/brylevkirill/tech/blob/master/RDF/LDP.txt
		Graphity LDP - http://fusepool.eu/more/links/projects/graphity + https://github.com/Graphity/graphity-ldp
		http://blog.ldodds.com/2013/06/15/building-the-new-ordnance-survey-linked-data-platform/
		https://code.google.com/p/lmf/

	* RDF graphs federation
		support for SPARQL Federated Query and for regular SPARQL Query over federated sources in http://fluidops.com/fedx/
			http://slideshare.net/aschwarte/fedx-for-federated-query-processing-on-linked-data
			demo at http://fedx.fluidops.net/resource/Help:Start

		specification and sample query - http://w3.org/TR/sparql11-federated-query/#simpleService

		"Querying over Federated SPARQL Endpoints - A State of the Art Survey" - http://arxiv.org/pdf/1306.1723.pdf

		"A Comparison of Federation over SPARQL Endpoints Frameworks" - http://goo.gl/0YHdsP

		reasoning over multiple federated end-points - https://github.com/djogopatrao/SPARQLFederator/wiki

		automatic query federation (query rewriting based on URI coreference information) - http://schlegel.github.io/balloon/balloon-fusion.html

	* export of relational database to RDF
		by mapping relational schema to RDF vocabulary in either of two ways:
			- dynamic rewriting of SPARQL query into SQL query
			- batch transform of relational data into RDF dump

		http://antoniogarrote.wordpress.com/2011/01/10/translating-sparql-queries-into-sql-using-r2rml/
		sample mappings - https://github.com/LinkedBrainz/MusicBrainz-R2RML/tree/master/mappings

		https://github.com/brylevkirill/tech/blob/master/RDF/R2RML.txt

	* validation
		http://throwww.com/a/7kv
		http://w3.org/2014/data-shapes/charter

		RDF Validation Workshop by W3C
			http://w3.org/2012/12/rdf-val/report
			notes - http://w3.org/2013/09/10-rdfval-minutes + http://w3.org/2013/09/11-rdfval-minutes
			presentations - https://w3.org/2012/12/rdf-val/agenda
			http://w3.org/2012/12/rdf-val/SOTA
		Stardog RDF database ICV
			* constraints defined in OWL (with Closed-World Assumption and weak Unique Name Assumption) or SPARQL
			* constraints translated to SPARQL queries

			sample constraint in natural language:
				"Only employees who are American citizens can work on a project that receives funds from a US government agency"
			sample constraint in OWL Manchester syntax:
				":Project and (:receives_funds_from some :US_Government_Agency))
					rdfs:subClassOf (inverse :works_on only (:Employee and (:nationality value "US")))" ~
			sample constraint in Turtle:
				"[ owl:intersectionOf (:Project
			                [ a owl:Restriction ; owl:onProperty :receives_funds_from ; owl:someValuesFrom :US_Government_Agency ]) .
				] rdfs:subClassOf
			                [ a owl:Restriction ; owl:onProperty [owl:inverseOf :works_on] ;
			                        owl:allValuesFrom [ owl:intersectionOf (:Employee 
			                                [ a owl:Restriction ; owl:hasValue "US" ; owl:onProperty :nationality ]) ] ] ."

			http://w3.org/2012/12/rdf-val/submissions/Stardog
			samples of constraints - http://docs.stardog.com/icv/
			http://clarkparsia.com/pellet/icv/
			sample at https://gist.github.com/evren/5612900
		W3C RDF Data Shapes - http://w3.org/2014/rds/charter
		OSLC Resource Shapes
			http://w3.org/Submission/2014/SUBM-shapes-20140211/
			http://ibm.com/developerworks/rational/library/linked-data-oslc-resource-shapes/index.html
			http://events.linkeddata.org/ldow2013/slides/ldow2013-slides-02.pdf
			http://events.linkeddata.org/ldow2013/papers/ldow2013-paper-02.pdf
			http://open-services.net/bin/view/Main/OSLCCoreSpecAppendixA#oslc_ResourceShape_Resource
		RDF Validation at Google
			http://w3.org/2001/sw/wiki/images/0/00/SimpleApplication-SpecificConstraintsforRDFModels.pdf
		SPIN rules - http://spinrdf.org
		RDF Shape Expressions - http://w3.org/2013/ShEx/Examples/ + http://w3.org/2013/ShEx/Primer.html
		Jena Eyeball
			http://jena.apache.org/documentation/tools/eyeball-guide.html
			http://jena.apache.org/documentation/tools/eyeball-manual.html

	* vocabularies/schemas/ontologies
		"Web Ontology Language Use Cases and Requirements" - http://w3.org/TR/webont-req/
		http://daverog.wordpress.com/2013/05/30/ontologies-in-software-a-conflict-of-interest/

		Web Ontology Language - https://github.com/brylevkirill/tech/blob/master/RDF/OWL.txt

		registry of all vocabularies - http://lov.okfn.org/dataset/lov/
		most used terms/relations and vocabularies - http://lov.okfn.org/dataset/lov/stats/

		"Ontology Development 101: A Guide to Creating Your First Ontology" - http://protege.stanford.edu/publications/ontology_development/ontology101.pdf
		best practices for publishing schemas on the web - http://w3.org/TR/swbp-vocab-pub/

		OWL Manchester Syntax (human-friendly) sample - https://dropbox.com/s/k1x2g6tthq5ggce/ontology.manchester_syntax.txt

		RDF store access control - http://ns.bergnet.org/tac/0.1/triple-access-control.html

		schema learning / ontology generating - http://gold.linkeddata.org/?p=59
		schema mapping - http://umbel.org

	* reasoning/inferencing/entailment
		reasoning:
			conjunctive query answering (checking presence of facts while deriving new facts from stored facts)
			proof searching
			consistency checking (check for presence of contradictions)
			concept satisfiability (check for possibility of class to have any instances)
			classification (compute subclass relations between classes to create complete hierarchy)
			instance type checking (compute direct types for resource)

		http://semanticweb.com/the-business-value-of-reasoning-with-ontologies_b38364

		demonstrating reasoning in StarDog (great technical introduction) - http://docs.stardog.com/owl2/
		demonstrating reasoning in Virtuoso - http://kidehen.blogspot.com/2014/01/demonstrating-reasoning-via-sparql.html

		samples of OWL reasoning/inferencing - http://ksl.stanford.edu/software/jtp/doc/owl-reasoning.html

		reasoning rules for RDFS and OWL description logics (formal defitions) -
			https://dropbox.com/s/cewl9ls41kmdmch/rdfs-definition.n3
			https://dropbox.com/s/4ksaj49yvt1o378/owl-definition.n3

		several levels/profiles - RDFS (simplest), OWL-QL (large number of instances, limited expressivity, log space), OWL-RL (tradeoffs between QL and EL), OWL-EL (large number of classes/properties, polynomial time), OWL-DL (most rich expressivity)

		implemented either through query rewriting or materialization of statements
			(materialization can be seen as worse strategy because of data freshness, data size, multiple reasoning profiles, computing resources)

		Pellet open-source reasoner for Jena and Stardog (support for OWL-DL as most powerful profile) - http://clarkparsia.com/pellet/ + https://github.com/clarkparsia/pellet
		implementations of reasoners - http://en.wikipedia.org/wiki/Semantic_reasoner

		probabilistic reasoning over ontologies with uncertainty (Pronto extension for Pellet)
			http://weblog.clarkparsia.com/2007/09/27/introducing-pronto/
			http://weblog.clarkparsia.com/2007/10/02/using-pronto/
			http://clarkparsia.com/files/pdf/Pronto-SemTech08.pdf
			http://shcherbak.net/2009/03/nemnogo-o-neopredelennosti-i-nechetkosti-v-ontologiyax/
			http://semanticfuture.net/index.php/%D0%92%D0%B5%D1%80%D0%BE%D1%8F%D1%82%D0%BD%D0%BE%D1%81%D1%82%D0%BD%D1%8B%D0%B5_%D0%BE%D0%BD%D1%82%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D0%B8
			http://semanticfuture.net/index.php/Pronto

		solving Sudoku problem using reasoning - http://eulersharp.sourceforge.net/2007/07test/sudoku_test

		constructor for classes of description logic and evaluator of complexity of reasoning over them - http://cs.man.ac.uk/~ezolin/dl/

		applications of reasoning:
			medicine - http://slid.es/mhgrove/improving-healthcare-through-semantics
			hardware complexity management in OS - http://inf.usi.ch/highlights/event/highlights_event_detail.htm?doc_id=23557

	* reification
		statements about statements (reification) in RDF 1.0 vs graphs about graphs (named graphs) in RDF 1.1

		"RDF was shaped by the constraints of first order predicate logic. Allowing statements about statements into RDF model theory shifts that logic from first order predicate calculus, which does not
permit statements about statements, into second order predicate calculus.
		The original concept of the Semantic Web steered clear of second order predicate calculus in order to avoid some pitfalls associated with previous knowledge representation frameworks."

		proposal for reification in schema.org vocabulary - https://w3.org/wiki/images/b/b5/RolesinSchema.org.pdf
		extension of the RDF data model and the SPARQL algebra that reconciles RDF Reification with statement-level metadata - RDF* and SPARQL*
			http://blog.bigdata.com/?p=716 + http://bigdata.com/whitepapers/reifSPARQL.pdf
			support in Systap Bigdata - http://systap.com/rdr

			:bob foaf:name "Bob" .
			<<:bob foaf:age 23>> dct:creator <http://example.com/crawlers#c1>
				dct:source <http://example.net/homepage-listing.html> .

			SELECT ?age ?src WHERE {
				?bob foaf:name "Bob" .
				<<?bob foaf:age ?age>> dct:source ?src .
			}

	* planning
		HTN-DL planner (combines OWL-S and Pellet reasoner)
			http://weblog.clarkparsia.com/2009/02/04/what-is-automated-planning
			http://clarkparsia.com/talks/oap/
		RESTdesc
			http://notes.restdesc.org/2011/images/usecase-3.html
			http://slideshare.net/RubenVerborgh/distributed-affordance-21175728
			http://ruben.verborgh.org/phd/

	* workflows / composition of web services
		RESTdesc
			http://slideshare.net/RubenVerborgh/distributed-affordance-21175728
			http://ruben.verborgh.org/publications/coppens_cold_2013/
			http://ruben.verborgh.org/phd/

	* provenance
		http://w3.org/2005/Incubator/prov/wiki/What_Is_Provenance
		http://slideshare.net/tdenies/20130722-tom-de-nies-method-2013
		http://goo.gl/me15I

	* annotations
		http://openannotation.org/spec/core/
		http://hypothes.is

	* resource graph revisions/changes and diffs/patches
		http://w3.org/TR/2014/WD-ldpatch-20140918/
		http://afs.github.io/rdf-patch/
		http://w3.org/2001/sw/wiki/PatchRequirements
		http://w3.org/2009/12/rdf-ws/papers/ws07

	* resource graph update subscriptions and notifications
		OWLIM - http://owlim.ontotext.com/display/OWLIMv50/OWLIM-SE+Notifications
		Jena - http://jena.apache.org/documentation/notes/event-handler-howto.html

	* resource graph-level security
		Jena (access restrictions to graphs and/or triples within the graphs) - http://jena.apache.org/documentation/security/
		OpenLink Virtuoso - http://virtuoso.openlinksw.com/dataspace/doc/dav/wiki/Main/VirtRDFGraphsSecurity
		Universal Access Control for triplestores - https://bergnet.org/people/bergi/files/documents/2014-02-14/index.html

	* full-text search extensions for query
		http://answers.semanticweb.com/questions/8676/do-you-use-full-text-search-with-sparql-if-so-how-and-why
		Jena - http://jena.apache.org/documentation/query/text-query.html

	* analytics
		http://slideshare.net/fadimaali/rdf-analytics-sparql-and-beyond

		VisualDataWeb - visualizations of data web exposed via SPARQL end-point
			interactive relationship discovery in RDF data - http://www.visualdataweb.org/relfinder.php
			visual analysis of trends and correlations in RDF data - http://www.visualdataweb.org/semlens.php
			graph-based faceted exploration of RDF data - http://www.visualdataweb.org/gfacet.php
			hierarchical faceted exploration of RDF data - http://www.visualdataweb.org/tfacet.php

	* visualization
		Sgvizler framework - https://code.google.com/p/sgvizler/
			timeline (zoomable) - http://sgvizler.googlecode.com/svn/release/0.5/example/exNPD8.html
			graph with labelled curved edges (clickable, movable) - http://sgvizler.googlecode.com/svn/release/0.5/example/exEnhetsregisteret1.html
			graph with unlabelled edges (clickable, moveable, zoomable) - http://sgvizler.googlecode.com/svn/release/0.5/example/exWorld7.html
			hierarchy chart (clickable) - http://sgvizler.googlecode.com/svn/release/0.5/example/exNPD7.html
			motion chart - http://sgvizler.googlecode.com/svn/release/0.5/example/exNPD5.html
			Google Maps layer - http://sgvizler.googlecode.com/svn/release/0.5/example/exDBpedia1.html
			pie chart - http://sgvizler.googlecode.com/svn/release/0.5/example/index.html
			bar chart + geo chart - http://sgvizler.googlecode.com/svn/release/0.5/example/exWorld1.html
			bubble chart - http://sgvizler.googlecode.com/svn/release/0.5/example/exWorld4.html
			treemap - http://sgvizler.googlecode.com/svn/release/0.5/example/exNPD6.html
		VisualBox framework - https://github.com/alangrafu/visualbox
			demos - http://visualbox.org/demos/home.html
			http://slideshare.net/alangrafu/visualizations-using-visual-box
			creation of visualization - https://github.com/alangrafu/visualbox/wiki/How-to-create-a-new-visualization

		http://mkbergman.com/414/large-scale-rdf-graph-visualization-tools/
		http://semanticscience.wordpress.com/2010/02/17/visualisation-of-ontologies-and-large-scale-graphs/
		http://answers.semanticweb.com/questions/1071/visualisation-toolkits-for-rdf
		visualization strategies - https://github.com/timrdf/vsr/wiki

	* semantic UI
		https://w3.org/community/rdfjs/wiki/Comparison_of_RDFJS_libraries

		RDF JavaScript Libraries W3C Community Group -
			http://w3.org/community/groups/proposed/#rdfjs
			http://lists.w3.org/Archives/Public/public-rdfjs

		semantic Web Components - http://video.dataversity.net/video/semantic-web-components/

		FluidOps Information Workbench - auto-generated Linked Data UI with support for widgets and customizations
			http://iwb.fluidops.com
			http://youtube.com/watch?v=_9Lu7cVIRSw
			http://fluidops.com/information-workbench/
		LodLive - web of data browser
			http://youtube.com/watch?v=3bt7XpgXPuc
			http://en.lodlive.it
			https://github.com/dvcama/LodLive
		HTML5PivotViewer - pivoted Linked Data browser in HTML5
			http://youtube.com/watch?v=JVwInt2nTuk
			original Pivot by Microsoft - http://youtube.com/watch?v=BZuFUZpEZ-A
			http://lists.w3.org/Archives/Public/public-lod/2013Jun/0095.html
			https://github.com/openlink/html5pivotviewer
		LODSPeaKr - linked data publishing framework
			http://alangrafu.github.io/lodspeakr/applications.html
			https://github.com/alangrafu/lodspeakr
		SPARQL query editors
			http://yasgui.laurensrietveld.nl + https://github.com/LaurensRietveld/yasgui/
			https://github.com/epimorphics/qonsole

	* context
		context-aware presentation of resources - http://ns.inria.fr/prissma/v2/prissma_v2.html

	* RDF dataset autodiscovery
		http://patterns.dataincubator.org/book/dataset-autodiscovery.html
		"Describing Linked Datasets with the VoID Vocabulary" - http://w3.org/TR/void/

	* specialized categories of RDF data
		data beyond graphs - http://w3.org/2013/04/odw/odw13_submission_53.pdf
		tabular data in CSV-LD - https://w3.org/2013/csvw/wiki/CSV-LD
		geo data - http://en.wikipedia.org/wiki/GeoSPARQL
		temporal data - http://blog.mynarz.net/2013/07/capturing-temporal-dimension-of-linked.html




[RDF databases]

	https://dropbox.com/s/esqw0qh3j08545y/Philip%20Howard%20-%20All%20About%20Graphs%3A%20A%20Primer.pdf

	https://dropbox.com/s/tq4jwsw7905neza/Graph%20and%20RDF%20Databases%202015.pdf -
		http://bloorresearch.com/technology/graph-databases/
		http://bloorresearch.com/research/market-update/graph-rdf-databases-2015/

	http://en.wikipedia.org/wiki/Graph_database

	http://semanticweb.com/introduction-to-triplestores_b34996

	http://forbes.com/sites/ciocentral/2015/04/06/the-hype-around-graph-databases-and-why-it-matters/
	http://insideanalysis.com/2015/01/the-graph-database-and-the-rdf-database/
	Graph and RDF databases in 2015 - https://dropbox.com/s/ts9kse7j5xv1bxb/tak-bloor.pdf

	"A Survey of RDF Data Management Systems" - http://arxiv.org/abs/1601.00707

	RDF triple stores overview - http://garshol.priv.no/blog/231.html
	features of RDF store - http://virtuoso.openlinksw.com/rdf-quad-store/?gclid=CLn8jdun4LUCFat7cAodwU0AXQ
	popularity ranking - http://db-engines.com/en/ranking/rdf+store
	evaluation/comparison of RDF stores - http://eprints.cs.univie.ac.at/2833/1/europeana_ts_report.pdf

	analysis of commercial RDF database market - http://weblog.clarkparsia.com/2010/09/23/the-rdf-database-market/

	list of RDF stores - http://w3.org/2001/sw/wiki/Category:Triple_Store
	large stores - http://w3.org/wiki/LargeTripleStores
	comparison of RDF stores - http://garshol.priv.no/blog/231.html

	comparison of RDF stores for Wikidata - https://docs.google.com/spreadsheets/d/1MXikljoSUVP77w7JKf9EXN40OB-ZkMqT8Y5b2NYVKbU

	about performance, scalability, availability, security of SPARQL end-point - https://plus.google.com/112399767740508618350/posts/UN6XyT4Xbcs

	performance of SPARQL in Virtuoso on store with 150B triples - http://static.lod2.eu/Deliverables/D2.1.4.pdf
	performance of SPARQL vs SQL in Virtuso for analytics benchmark - http://goo.gl/0Q38OV

	performance benchmarks - http://w3.org/wiki/RdfStoreBenchmarking
	Berlin SPARQL performance benchmark -
		http://wifo5-03.informatik.uni-mannheim.de/bizer/berlinsparqlbenchmark/
	biological data performance benchmark -
		http://ncbi.nlm.nih.gov/pmc/articles/PMC3471352/

	http://thinklinks.wordpress.com/2013/04/03/5-heuristics-for-writing-better-sparql-queries/


	[native graph stores]

	* Amazon Neptune
		large-scale, low latency, graph database that supports both RDF graphs and property graphs, along with their respective query languages SPARQL and TinkerPop Gremlin

		https://aws.amazon.com/neptune/

		based on Systap Blazegraph [https://trademarkia.com/blazegraph-86498414.html] [https://news.ycombinator.com/item?id=15808379]


	* Stardog
		"You want to defer the schema, to partially define it incrementally, to enforce it, to infer from it. No technology offers more schema flexibility than RDF & OWL."

		http://slides.com/mhgrove/stardog-unleashed-in-nyc/
		http://slid.es/kendallclark/stardog-20
		http://presentboldly.com/kendall/stardog-21/7
		http://slid.es/mhgrove/semantic-graphs-are-for-everyone
		http://slides.com/mhgrove/fighting-sepsis

		very focused on query performance
			best results both on BSBM benchmark for OLTP (e-commerce use-case, 3M queries per hour on 100M triples, 500K on 1B and 20K on 10B)
			best results on SP2B benchmark for OLAP (bibliography use-case)
		very focused on storage scale-up
			support for 50B triples on machine with 256Gb memory and for 10B+ triples with 2Gb memory
			loading 100m triples in 3m, 1B triples in 30m, 20B triples in 20h
			around 300000 triples per second indexing speed for 20B dataset

		performance and scalability improvements (query, data loading, reasoning) in version 2.1
			http://weblog.clarkparsia.com/2014/01/10/scalability-improvements-in-stardog-21/
			http://highscalability.com/blog/2014/1/20/8-ways-stardog-made-its-database-insanely-scalable.html
		custom made memory management scheme out of JVM heap with pauseless garbage collection

		used by NASA -
			https://stardog.com/blog/nasas-knowledge-graph/
			https://blog.stardog.com/nasa-stardogs-going-to-mars/
			http://w3.org/blog/2011/05/semantic-web-its-not-rocket-sc/
		used by BestBuy for product search API - http://semanticweb.com/best-buy-releases-like-for-like-metis-api_b35328

		features - http://docs.stardog.com/timeline/ + http://docs.stardog.com/RELEASE_NOTES.txt
			* integrity constraints validation
				http://docs.stardog.com/icv/
				http://w3.org/2012/12/rdf-val/submissions/Stardog
				http://w3.org/2001/sw/wiki/images/6/61/Stardog_ICV_RDF_Validation_Workshop.pdf
				sample code - https://gist.github.com/mhgrove/1333767 + https://gist.github.com/evren/5612900

				either called on-demand for whole database or called automatically for updated data on transaction commit
				constraints defined using OWL axioms, SPARQL queries or SWRL rules (which are interpreted with closed-world assumption and weak unique-name assumption)
				possibility to translate and return all constraints as SPARQL queries
				possibility to return explanation and proof tree for each detected violation - http://docs.stardog.com/owl2/#sd-Proof-Trees
					"Supervisor subClassOf supervises some Employee" violated by "Alice a Supervisor" which is explained as
					"VIOLATED Supervisor subClassOf (supervises some Employee) ASSERTED Alice a Supervisor NOT_INFERRED x a Employee Alice supervises x"
				possibility to enable inference during validation
				"Stardog ICV isn't merely a system that tells a user that data is wrong in some way, but tells users why it's wrong and what they can do to repair it"
				"Stardog ICV can also work transparently with any SPARQL query answering system"
				constraint in natural language:
					"If a project is funded by only internal funding sources then it should be approved by the internal budget office"
				and corresponding constraint in OWL Manchester syntax:
					"Project and (fundedBy only InternalFundingSource) rdfs:subClassOf approvedBy value InternalBudgetOffice"
				sample OWL schema for validation - https://dropbox.com/s/k1x2g6tthq5ggce/ontology.manchester_syntax.txt

			* reasoning (outstanding support) - http://docs.stardog.com/owl2/
				reasoning defined using OWL axioms, user-defined SPARQL-based rules or SWRL rules, such as
					"IF { $x a :Person, :Male; :hasSibling/:isParentOf [a :Female] } THEN { $x a :UncleOfNiece . }"
				configurable levels of reasoning (per database and per session) - NONE, RDFS, QL, RL, EL, SL, DL
				backward-chaining reasoning through query rewriting
				possibility to find and return proof tree with steps for inferencing arbitrary given triples
				"Stardog can provide reasoning for any other SPARQL query answering system, transparently"

			* ACID transactions
			* full text, semantically typed search - http://docs.stardog.com/using/#sd-Searching
			* provenance
			* record-level access control with permissions assigned to user or role - http://docs.stardog.com/security/
			* graph version control (git-like history of revisions and reverting them)
			* high availability cluster - http://docs.stardog.com/cluster/
			* semi-automated repair plans for integrity constraint violations
			* reification (support for named statements in addition to named graphs)
			* named graph security (analogous to row-based and table-based security)
			* SPARQL Federated Query support
			* virtual graphs and R2RML support
			* property graph model, Gremlin query language and Apache TinkerPop 3 APIs support
			* graph analytics features (graph measures, clustering, path-finding) embedded into SPARQL - https://twitter.com/stardog_db/status/464772464686661632/photo/1 + https://gist.github.com/kendall/8423194

			client-server or embedded
			CLI and shell
			REST API - http://docs.stardog.apiary.io + bingings - https://github.com/antoniogarrote/stardog-rb
			Jena and Sesame APIs
			web front-end (console for administration and exploration) - http://docs.stardog.com/console/
			access and audit logging
			JMX Monitoring
			online/hot backups

			configuration options for database - http://docs.stardog.com/admin/#sd-Database-Admin

			no support for event listeners
			no support for stored procedures (in plans)

			features used for application in synthetic biology - https://plus.google.com/106211035436647659652/posts/LMGzmQaM62o

			poll for features - http://stardog.wufoo.com/forms/z7x3x5/
			advanced features in roadmap for near future (graph traversal, statistical/probabilistic inference) + for far future (machine learning, planning, ontology modularization) - http://clarkparsia.com/pellet/server/docs/features/

		"175kloc - 100kloc for reasoners, other bits + test suite 71kloc"
		10000+ autotests
		editions - enterprise commercial, developer commercial, restricted free
		closed-source
		developed in Java

		Stardog Web
			UI framework based on Backbone.js and Bootstrap for building client-side MVC applications that use RDF, SPARQL, rules, OWL, REST CRUD, Linked Data, JS visualization, authentication, authorization
			http://slid.es/kendallclark/introducing-stardog-web
			will be released in 2014

		client code samples in Java - https://github.com/Complexible/stardog-examples/

		OWL UML-style schema editor - http://owlgred.lumii.lv + http://owlgred.lumii.lv/publications/OWLGrEdS_-_a_Graphical_Schema_Editing_for_StarDog_OWL-RDF-Databases.pdf

		interview with creator - http://reddit.com/r/semanticweb/comments/1mhytv/ama_i_am_the_creator_of_stardog_empire_and_pelorus/
		in development since 2008


	* Systap Blazegraph (former Bigdata)
		http://blazegraph.com

		"Market leader since 2006 in providing high performance, scalable solutions for graphs. The Bigdata platform supports both Semantic Web (RDF/SPARQL) and Graph Database (tinkerpop, blueprints, vertex-centric) APIs. It features robust, scalable, fault-tolerant, enterprise-class storage and query, and high-availability with online backup, failover and self-healing. Bigdata® powers many high profile enterprise applications for customers including Syapse, EMC, AutoDesk, and Yahoo!7"

		https://vimeo.com/134042340

		selected as a store for Wikidata -
			http://blog.blazegraph.com/?p=826
			https://lists.wikimedia.org/pipermail/wikidata-tech/2015-March/000740.html
			http://mediawiki.org/wiki/Wikibase/Indexing
			http://mediawiki.org/wiki/Wikidata_query_service

			https://www.mail-archive.com/wikidata-l@lists.wikimedia.org/msg05601.html
			https://lists.w3.org/Archives/Public/public-sparql-dev/2015JanMar/0031.html

		introduction - https://groups.google.com/forum/#!msg/gremlin-users/hc3wo431JO0/RpHPLA98yfwJ
		APIs - http://wiki.bigdata.com/wiki/index.php/Main_Page
		architecture - http://bigdata.com/whitepapers/bigdata_architecture_whitepaper.pdf

		GPL2 without restrictions on commercial usage

		optional transactions with snapshot isolation (MVCC on single machine or replication cluster, two-phase commit on federation cluster)
		immortal database with data view at any point in history with configurable retention period
		very high concurrency
		very high aggregate IO rates
		scales to 50B triples and 50k-80k/s insert rate on single machine and to trillions on sharded cluster of 10s or 100s machines
		distributed processing offers greater throughput but does not reduce query or update latency

		- embedded database mode
		- single machine mode
		- highly available non-sharded replication cluster mode (with ACID, linear scaling of query and automatic failover)
		- horizontally sharded scaled-out cluster mode (with shard-wise ACID, dynamic partitioning of graph and incremental cluster size growth)

		support for extension of RDF data model (RDF*) and SPARQL algebra (SPARQL*) that reconciles RDF Reification with statement-level metadata (RDR ~ RDF Done Right)  - http://blog.bigdata.com/?p=716
		Blueprints API support
		graph analytics platform
		Gather Apply Scatter graph traversal API based on vertex-centric approach by Google Pregel - http://wiki.bigdata.com/wiki/index.php/RDF_GAS_API
		packaged with CPU-enabled version of massively parallel graph processing engine MapGraph (GPU-enabled and Multi-GPU version scheduled in next release) - http://mapgraph.io (up to 2B edges on single GPU)
		plans to enable world's fastest SPARQL end-point - http://blog.bigdata.com/?p=601

		full text search support
		SPARQL Federated Query support
		entailment through both materialization at load time (for RDF Schema) and at query time (for custom rules)
		IChangeLog interface for intercepting queries and transactions
		possibility to implement custom service to add application specific behaviors

		overview - http://snee.com/bobdc.blog/2016/05/trying-out-blazegraph.html


	* OpenLink Virtuoso
		introduction - https://plus.google.com/112399767740508618350/posts/LKbAU6JmZ6f
		features - http://virtuoso.openlinksw.com/rdf-quad-store/?gclid=CLn8jdun4LUCFat7cAodwU0AXQ
		open-source and commercial license - http://virtuoso.openlinksw.com/features-comparison-matrix/
		https://github.com/openlink/virtuoso-opensource
		performance of SPARQL in Virtuoso RDF store vs SQL in analytics benchmark - http://goo.gl/0Q38OV

		RDF database and relational database in one
		support for transient RDF views over internal relational model or over external SQL database (no support for the latter in open-source edition)
		clustered version - http://docs.openlinksw.com/virtuoso/clusteroperation.html + http://openlinksw.com/weblog/oerling/?id=1622
		graph-level security - http://virtuoso.openlinksw.com/dataspace/doc/dav/wiki/Main/VirtRDFGraphsSecurity
		possibility to use SPARQL and SQL together
		support for SPARQL Federated query
		no support for integrity constraints
		no support for OWL2 reasoning
		support only for reasoning over "subTypeOf, subPropertyOf, inverseOf (+ SymmetricProperty), InverseFunctionalProperty(+ inverseOf FunctionalProperty), TransitiveProperty"
		developed in C++

		support for 500B triples - http://openlinksw.com/dataspace/doc/oerling/weblog/Orri%20Erling's%20Blog/1767


	* GraphDB (former OWLIM)
		http://ontotext.com/owlim
		http://ontotext.com/owlim/editions
		http://owlim.ontotext.com/display/OWLIMv53/OWLIM-SE+Fact+Sheet
		http://ontotext.com/sites/default/files/owlim/OWLIM_FactForge_jul10.pdf

		OWLIM Enterprise | Replication Cluster (multiple master nodes which perform load balancing and orchestrate synchronization) - http://ontotext.com/owlim/replication-cluster
		OWLIM on Amazon Web Services - http://ontotext.com/owlim/owlim-in-the-cloud + http://slideshare.net/marin_dimitrov/owlimaws
		partner of FluidOps - http://ontotext.com/news/fluidOps_TeamUp

		based on Sesame library for API and storage
		APIs - http://ontotext.com/OWLIM/access-methods
		reasoning through materialization of inferred statements by OWLIM Reasoner
		async update events (clients can subscribe and react to addition/removal of triples matching given patterns and start/completion of transaction) both local and remote (JMX as transport) - http://owlim.ontotext.com/display/OWLIMv50/OWLIM-SE+Notifications
		higher levels of transaction isolation
		online backups
		nested repositories
		integration with Apache Jena
		full-text search via Lucene
		RDF rank (PageRank for nodes in graph)
		developed in Java


	* SPARQL City
		http://sparqlcity.com

		"SPARQL City is a provider of a Hadoop based graph analytics engine that brings to bear the performance and ease-of-use characteristics of massively parallel analytic databases on the world of graph data. The resulting product is built-around modern open standards and delivers orders of magnitude improvements in performance and scale over existing solutions while running on commodity hardware."

		http://sparqlcity.com/documentation/
		http://sparqlcity.com/why-sparql

		focused on OLAP scenarios and not on OLTP ones
		very high performance and highly scalable implementation of SPARQL 1.1
		scalability to hundreds of nodes
		ACID
		MongoDB or Cassandra as persistent storage back-end
		SPARQL extensions for analytics
		access control
		open-source
		predicate attributes
		from creators of Amazon Redshift - http://sparqlvillage.org/about/


	* Google's BadWolf
		temporal graph store abstraction layer

		https://github.com/google/badwolf

		http://go-talks.appspot.com/github.com/google/badwolf/docs/presentations/2016/06/21/ottawa-graph-meetup.slide


	* Google's Cayley
		https://github.com/cayleygraph/cayley/
		http://google-opensource.blogspot.ru/2014/06/cayley-graphs-in-go.html
		Gremlin query language as JavaScript code - http://sql2gremlin.com


	* LevelGraph
		https://github.com/mcollina/levelgraph
		https://github.com/mcollina/levelgraph-jsonld
		no support for SPARQL


	* BrightstarDB
		http://brightstardb.com
		ORM and LINQ provider for .NET applications
		support for arbitrary RFD storage as backend


	* Algebraix


	* Sesame
		SAIL API (which enables arbitrary storage backend, such as graph database via TinkerPop Linked Data Sail - https://github.com/tinkerpop/blueprints/wiki/Sail-Implementation such as Titan graph database)
		possibility to expose repository via servlet container
		possibility to use PostgreSQL, MySQL, Microsoft SQL Server, Oracle as backend
		support for RDFS reasoning, no support for OWL2 reasoning
		used by FluidOps
		open-source
		developed in Java


	* Apache Jena
		update events - http://jena.apache.org/documentation/notes/event-handler-howto.html
		support for relational database as storage backend
		support for JSON-LD - https://github.com/afs/jena-jsonld
		graph-level security - http://jena.apache.org/documentation/security/
		full-text search - http://jena.apache.org/documentation/query/text-query.html
		support for Hadoop - http://jena.staging.apache.org/documentation/hadoop/
		support for JDBC - http://jena.apache.org/documentation/jdbc/index.html
		transactions support - http://jena.apache.org/documentation/tdb/tdb_transactions.html
		developed in Java


	* YarcData Urika
		http://yarcdata.com
		hardware appliance by Cray - http://cray.com/Products/BigData/uRiKA.aspx




	[relational DBMS-backed stores]

	* Oracle 11g database
		http://download.oracle.com/otndocs/products/semantic_tech/pdf/12c/rdfsemanticgraph_12c_fo.pdf
		http://docs.oracle.com/cd/E16655_01/appdev.121/e17895/toc.htm


	* IBM DB2 10.5 Enterprise (RDF Store feature)
		http://www-01.ibm.com/software/data/db2/linux-unix-windows/features.html
		http://goo.gl/kcLGlN
		https://ibm.com/developerworks/community/blogs/nlp/resource/DB2_NoSQLGraphStore.pdf


	* RDFLib
		https://rdflib.readthedocs.org + https://github.com/RDFLib/rdflib/
		support for remote SPARQL endpoint as storage backend - https://github.com/RDFLib/rdflib-sparql
		support for PostgreSQL, MySQL, SQLLite as storage backend - https://github.com/RDFLib/rdflib-sqlalchemy
		support for LevelDB as storage backend - https://github.com/RDFLib/rdflib-leveldb
		support for JSON-LD - https://github.com/RDFLib/rdflib-jsonld + https://github.com/digitalbazaar/pyld
		FuXi reasoner - https://code.google.com/p/fuxi/ + https://code.google.com/p/fuxi/wiki/Tutorial
		ORM for RDF graph and SPARQL - http://openvest.com/trac/wiki/RDFAlchemy
		developed in Python
		BSD license


	* libRDF + RedStore
		http://librdf.org
		http://aelius.com/njh/redstore/
		support for PostgreSQL, MySQL, SQLLite as storage backend
		no native support for JSON-LD
		developed in C + bindings for Python
		LGPL 2.1, GPL 2, Apache license


	* D2RQ
		implementation of RDF wrapper for relational database with custom mapping
		http://d2rq.org + http://d2rq.org/d2r-server
		https://github.com/d2rq/d2rq
		own mapping language - http://d2rq.org/d2rq-language
		R2RML mapping language - https://github.com/brylevkirill/tech/blob/master/RDF/R2RML.txt
		developed in Java
		support for PostgreSQL, MySQL, SQL Server, Oracle


	* Arc2
		https://github.com/semsol/arc2/wiki
		RDF PHP library and RDF store over MySQL


	[NoSQL DBMS-backed stores]

	* Apache Tinkerpop / BlueprintsSail
		https://github.com/tinkerpop/blueprints/wiki/Sail-Ouplementation
		any graph database with support for Blueprints API

		- Microsoft Azure Cosmos DB
			https://docs.microsoft.com/en-us/azure/cosmos-db/gremlin-support

		- Neo4J
			http://neo4j.org/develop/linked_data

		- Cassandra
			CumulusRDF - http://code.google.com/p/cumulusrdf/

		- Titan distributed graph database (can be run over HBase or Cassandra)
			http://thinkaurelius.github.io/titan/
			https://groups.google.com/forum/#!topic/aureliusgraphs/Uzi6rilPF8s

			http://allthingsdistributed.com/2015/08/titan-graphdb-integration-in-dynamodb.html
			"The combination of Titan with DynamoDB is now powering Amazon’s fulfillment network, with a multi-terabyte dataset."


	* RDFstore-js
		https://github.com/antoniogarrote/rdfstore-js
		developed in JavaScript (NodeJS and browser)
		https://dropbox.com/s/ig3o4gelyksigfl/RDFStore-JS.pdf
		events listener API (node changes and query result set changes)
		MongoDB or HTML5 LocalStorage as backend
		native support for JSON-LD
		support for latest draft of JSON-LD via https://github.com/digitalbazaar/jsonld.js/
		LGPL 3 license


	"NoSQL Databases for RDF: An Empirical Evaluation"
		http://ribs.csres.utexas.edu/nosqlrdf/nosqlrdf_iswc2013.pdf
		- HBase with Jena for querying
		- HBase with Hive as the query engine (Jena ARQ -> HiveQL)
		- CumulusRDF (Cassandra with Sesame)
		- CouchbaseRDF (Jena ARQ)


	SHARD (HDFS-based triple store)
		http://avometric.com/shard.shtml




[RDF libraries and tools]

	http://w3.org/2001/sw/wiki/Tools
	http://goo.gl/MnKdAS
	http://mkbergman.com/sweet-tools/

	[Java]
		http://w3.org/2001/sw/wiki/Java

		Pinto - Java beans mapper into RDF and back
			https://github.com/Complexible/pinto
			https://github.com/Complexible/pinto/blob/develop/test/src/com/complexible/pinto/RDFMapperTests.java
		Empire - JPA ORM layer for RDF and SPARQL
			https://github.com/mhgrove/Empire
			http://slideshare.net/candp/sem-tech-empirepresentation2
			http://weblog.clarkparsia.com/2010/05/07/rdf-for-fun-and-profit-using-empire
			sample annotations - https://github.com/mhgrove/Empire/tree/master/examples/src/com/clarkparsia/empire/examples

		OWL API - creating, manipulating and serialising OWL Ontologies
			http://owlapi.sourceforge.net/
			support for OWL Manchester syntax
		OWL2CVS - diff tool for OWL2 ontologies
			https://github.com/utapyngo/owl2vcs
			support for OWL Manchester syntax
		OpenRDF
			support for OWL - http://docs.stardog.com/java/snarl/com/complexible/common/openrdf/util/ExpressionFactory.html

		RDF API and web services - http://incubator.apache.org/clerezza/

	[Python]
		http://w3.org/2001/sw/wiki/Python
		http://michelepasin.org/blog/2011/02/24/survey-of-pythonic-tools-for-rdf-and-linked-data-programming/

		RDFLib - https://github.com/RDFLib/rdflib/wiki
			FuXi's InfixOwl module for OWL

		FuXi reasoning engine - http://code.google.com/p/fuxi/wiki/Overview
			support for logic programming (deduction, back-chaining - generating proof for given statement with inference rules)
			support for production systems (induction, forward-chaining - generating statements inferred by given rules from given statement)
				http://en.wikipedia.org/wiki/Production_system
				RETE-UL Network algorithm adopted for representation of facts as triples - http://en.wikipedia.org/wiki/Rete_algorithm
			support for non-monotonic reasoning (negated literals in the body and in the consequent) - possibility to cancel effect of particular rules
				* support for negation as failure (closed world assumption) - deriving "not P" (assuming P not to hold true) from failure to derive P
				* support for default logic (default negation) - "by default, P is true"
					reasoning often involves facts that are true in the majority of cases but not always -
						“birds typically fly" instead of "all birds that are not penguins and not ostriches and ... fly"
					it can be impractical or impossible to write down all the negative facts to take advantage of classical negation
					default logic aims at formalizing inference rules like this one without explicitly mentioning all their exceptions
			GMS (default), SLD and BFP strategies for inference
			user-specified rule prioritization
			integration with RDFLib - https://code.google.com/p/fuxi/wiki/Tutorial
			InfixOwl module
				constructing OWL model in pure Python and serializing into RDF or OWL Manchester Syntax
				https://code.google.com/p/fuxi/wiki/InfixOwl
				http://python-dlp.googlecode.com/files/infixOwl.pdf
				https://github.com/RDFLib/rdflib/blob/master/rdflib/extras/infixowl.py
			RDF as core knowledge representation of facts
			Datalog (Horn logic) rules as core representation both of description logic subset in OWL (OWL2 RL but not complete OWL DL) and of logic rules in RIF Core
			formal definitions and reasoning rules for RDFS and OWL description logics adopted by FuXi
				https://dropbox.com/s/cewl9ls41kmdmch/rdfs-definition.n3
				https://dropbox.com/s/4ksaj49yvt1o378/owl-definition.n3

		ORDF ORM - http://pythonhosted.org/ordf/
			based on modified FuXi's InfixOwl module
			object-description mapper
			revision history, provenance, graph difference
			namespace library

		Object Linked Data Mapper with support for Hydra and JSON-LD - https://github.com/oldm/OldMan

		RDFAlchemy ORM - http://openvest.com/trac/wiki/RDFAlchemy

		Telescope SPARQL query builder - https://bitbucket.org/exogen/telescope/wiki/SPARQLBuilder

		projects:
			https://github.com/mmlab/eice (Tornado, NetworkX)

	[Scala]
		https://github.com/w3c/banana-rdf

		https://github.com/w3c/banana-rdf/tree/series/0.8.x/rdf-test-suite/common/src/main/scala/org/w3/banana
		https://github.com/w3c/banana-rdf/blob/series/0.8.x/rdf-test-suite/common/src/main/scala/org/w3/banana/diesel/DieselOwlPrimerTest.scala

	[JavaScript]
		http://www.w3.org/community/rdfjs/wiki/Main_Page
		https://w3.org/community/rdfjs/wiki/Comparison_of_RDFJS_libraries

		RDF JavaScript Libraries W3C Community Group -
			http://w3.org/community/groups/proposed/#rdfjs
			http://lists.w3.org/Archives/Public/public-rdfjs

		wrapper/ORM for JSON-LD - https://github.com/bergos/rdf-ext
		RDF and SPARQL library - https://github.com/linkeddata/rdflib.js#readme
		Turtle/Notation3 and RDF store library - https://github.com/RubenVerborgh/node-n3
		Turtle parser - http://ruben.verborgh.org/blog/2013/04/30/lightning-fast-rdf-in-javascript/
		building linked data applications in JavaScript - http://notes.3kbo.com/node-js + http://notes.3kbo.com/javascript-sparql

	[UI frameworks]
		Stardog Web - http://slid.es/kendallclark/introducing-stardog-web
			UI framework based on Backbone.js and Bootstrap for building client-side MVC applications that use RDF, SPARQL, rules, OWL, REST CRUD, Linked Data, JS visualization, authentication, authorization
		LDApp - https://bergnet.org/people/bergi/files/documents/2014-02-14/index.html
		Backbone.js with Linked Data extension - https://github.com/antoniogarrote/backbone

		semantic Web Components - http://video.dataversity.net/video/semantic-web-components/

	[Go]
		https://github.com/linkeddata/gold

	[PHP]
		RDF PHP library and RDF store over MySQL - https://github.com/semsol/arc2/ + https://github.com/semsol/arc2/wiki

	[R]
		SPARQL package for R - http://linkedscience.org/tools/sparql-package-for-r/linked-open-piracy-tutorial/

	converters of multiple data formats into RDF - http://w3.org/wiki/ConverterToRdf

	[IDEs]
		TopBraid Composer plug-in for Eclipse - http://topquadrant.com/products/TB_Composer.html
		VIM plugin - https://github.com/seebi/semweb.vim
		Sublime SPARQL plugin - https://github.com/cezarsa/sublime-sparql-runner

	[documentation]
		DocuSPeaKr documentation for OWL ontology - https://github.com/alangrafu/docuspeakr
		JavaDoc style HTML page documentation for OWL ontology - http://co-ode.org/downloads/owldoc/

	[visualization]
		http://vowl.visualdataweb.org
		http://w3.org/wiki/SemWebGraphicalNotation
		http://composing-the-semantic-web.blogspot.com.au/2012/06/graphical-ontology-editing-with.html




[articles about RDF]

	courses
		http://euclid-project.eu
		https://coursera.org/course/metadata
		http://cambridgesemantics.com/semantic-university (including webinars)

	lectures
		http://videolectures.net/Top/Computer_Science/Semantic_Web/

	state of things - http://semanticweb.com/keep-on-keepin-on_b41339

	"The Semantic Web Doesn't Exist Because Everyone's Doing it Wrong" - https://t.co/F2gFh8o6PM

	original vision - http://www.cs.umd.edu/~golbeck/LBSC690/SemanticWeb.html + http://ted.com/talks/tim_berners_lee_on_the_next_web.html
	updated vision - http://blog.primal.com/2013/08/the-history-of-the-semantic-web-tells-us-about-its-future/
	vision by experts - http://youtube.com/watch?v=rVAmC4AzdjA + http://vimeo.com/11529540

	criticism
		http://www.well.com/~doctorow/metacrap.htm
		http://semanticweb.com/nova-spivack-new-era-semantic-web-history_b45420
		"Is the semantic web still a thing?" - https://news.ycombinator.com/item?id=8510401
		http://manu.sporny.org/2012/nuclear-rdf/
		"The Semantic Web Doesn't Exist Because Everyone's Doing it Wrong" by Kendall Clark - http://goo.gl/t57TPc
		http://lists.w3.org/Archives/Public/public-lod/2014Apr/0180.html
		'"Why the Semantic Web will never work"' by Jim Hendler - http://youtube.com/watch?v=oKiXpO2rbJM
		http://lemire.me/blog/archives/2014/12/02/when-bad-ideas-will-not-die-from-classical-ai-to-linked-data/ (comment #16)
		http://gigaom.com/2013/11/24/lets-build-a-semantic-web-by-creating-a-wikipedia-for-relevancy/

		"I think this is a very small use case and there's not enough critical mass behind it. The main reason being that even if you were able to aggregate all the different API together to build something new and bold, it's such a one off idea that is specific to a developer that it really wouldn't be of a much use investing huge amounts of time and money towards building a consolidated API that would serve multiple masters. The rise of AI and machine learning really puts into doubt the economic feasibility of spending money and time on a service that focuses purely on aggregating disparate islands of data unless the payoff existed in that particular market. You don't see a major API provider that provides data to everything, instead you see small enclaves of niche businesses that focus and specialize in their specific consolidation efforts and get paid for it. All in all, I think the semantic web will become more of a private endeavor, at least for proprietary commercial goals. As AI gains more ground, the need for such a central API or the need to unify all the different data together will slowly die off."

	"Linked Data: Evolving the Web into a Global Data Space" - http://linkeddatabook.com/editions/1.0/
	"pattern catalogue for modeling, publishing and consuming Linked Data" - http://patterns.dataincubator.org/book/
	"Linked Data - Structured data on the Web" - http://manning.com/dwood/

	http://planetrdf.com/guide/ - huge collection of publications




<brylevkirill@gmail.com>
