OWL
	http://w3.org/2007/OWL/wiki/Primer
	http://w3.org/TR/owl-ref/
	http://w3.org/TR/owl2-syntax/
	http://w3.org/TR/owl2-mapping-to-rdf/

	http://cambridgesemantics.com/semantic-university/owl-reference-for-humans

	diagram and overview for entity types in RDF/RDFS/OWL - http://infowebml.ws/website/graphical-representations.htm

	use-cases and requirements - http://w3.org/TR/2004/REC-webont-req-20040210/

	http://semanticweb.com/the-business-value-of-reasoning-with-ontologies_b38364
	http://blog.mynarz.net/2014/07/methods-for-designing-vocabularies-for.html

	ontology for real-world entities developed by Google, Microsoft, Yahoo and Yandex - http://schema.org + http://schema.org/docs/schemaorg.owl
	ontology for products and services - http://heppnetz.de/projects/eclassowl/
	ontology for software projects - https://github.com/edumbill/doap
	ontology for Internet of Things - https://iotdb.org
	ontology for enterprise cloud services management by FluidOps - http://fluidops.com/ontologies/ + http://fluidops.com/download/eCloud_Ontology

	comprehensive introduction - https://dropbox.com/sh/674ht9t5whehoht/_euaaD0ubz + http://orm.net/pdf/OntologicalModeling{1,15}.pdf


	publishing OWL ontology as part of JSON-LD context
		Activity Streams 2.0 - http://asjsonld.mybluemix.net
		schema.org - https://github.com/ruby-rdf/json-ld/blob/develop/etc/schema.org.jsonld

	Manchester syntax (human-friendly)
		samples - https://dropbox.com/s/k1x2g6tthq5ggce/ontology.manchester_syntax.txt
		http://protegewiki.stanford.edu/images/5/5f/Owled2008dc_paper_11.pdf
		can be used as DL query language - http://protegewiki.stanford.edu/wiki/DLQueryTab
		SPARQL extension to query OWL ontology - http://weblog.clarkparsia.com/2010/04/01/pellet-21-introducing-terp + http://slideshare.net/candp/owled-2010-terp


	complete human-readable definition of OWL semantics - http://w3.org/2007/OWL/wiki/FullSemantics
	OWL reasoning capabilities - http://ksl.stanford.edu/software/jtp/doc/owl-reasoning.html

	formal computer-readable definitions and reasoning rules for RDFS and OWL description logics -
		https://dropbox.com/s/cewl9ls41kmdmch/rdfs-definition.n3
		https://dropbox.com/s/4ksaj49yvt1o378/owl-definition.n3

	tools
		validation
			Jena Eyeball -
				http://jena.apache.org/documentation/tools/eyeball-guide.html
				http://jena.apache.org/documentation/tools/eyeball-manual.html
		visualization
			http://owlgred.lumii.lv/online_visualization/org.owl
			http://vowl.visualdataweb.org
		Java
			OWL API (with support for Manchester Syntax) - http://owlapi.sourceforge.net/
			OpenRDF - http://docs.stardog.com/java/snarl/com/complexible/common/openrdf/util/ExpressionFactory.html
			OWL ontologies difference -
				https://github.com/rsgoncalves/ecco
				https://github.com/utapyngo/owl2vcs

		Python
			RDFLib with InfixOWL module for OWL Manchester Syntax support
				https://github.com/RDFLib/rdflib/blob/master/rdflib/extras/infixowl.py
				http://ceur-ws.org/Vol-432/owled2008eu_submission_19.pdf

	several profiles for reasoning over ontologies - http://w3.org/TR/owl2-profiles/
		RDFS (simplest)
		OWL-QL (large number of instances, limited expressivity, log space)
		OWL-RL (tradeoffs between QL and EL)
		OWL-EL (large number of classes/properties, polynomial time)
		OWL-DL (most rich expressivity, intractable)

	constructor for classes of description logic and evaluator of complexity of reasoning over them - http://cs.man.ac.uk/~ezolin/dl/

	probabilistic reasoning over semantic web ontologies with uncertainty (Pronto extension for Pellet)
		http://weblog.clarkparsia.com/2007/09/27/introducing-pronto/
		http://weblog.clarkparsia.com/2007/10/02/using-pronto/
		http://clarkparsia.com/files/pdf/Pronto-SemTech08.pdf

	missing parts:
	- Modules and Imports
		The importing facility of OWL is very trivial: It only allows importing of an entire ontology, not parts of it
		Modules in programming languages based on information hiding: state functionality, hide implementation details
	- Defaults
		Many practical knowledge representation systems allow inherited values to be overridden by more specific classes in the hierarchy
		treat inherited values as defaults
	- Closed World Assumption
		OWL currently adopts the open-world assumption: A statement cannot be assumed true on the basis of a failure to prove it
		On the huge and only partially knowable WWW, this is a correct assumption
		Closed-world assumption: a statement is true when its negation cannot be proved
	- Unique Names Assumption
		Typical database applications assume that individuals with different names are indeed different individuals 
		OWL follows the usual logical paradigm where this is not the case
		Plausible on the WWW 
		One may want to indicate portions of the ontology for which the assumption does or does not hold
	- Rules for Property Chaining
		OWL does not allow the composition of properties for reasons of decidability
		In many applications this is a useful operation
		One may want to define properties as general rules (Horn or otherwise) over other properties 
		Integration of rule-based knowledge representation and DL-style knowledge representation is currently an active area of research

	advanced overview of OWL - http://youtube.com/watch?v=EXXIIlfqb0c + http://youtube.com/watch?v=UQ0wKix4RYQ


	first sample ontology in Manchester syntax:

		Class: Person
			Annotations: rdfs:label "Person"@en, rdfs:label "Человек"@ru
			SubClassOf: owl:Thing that hasFirstName exactly 1 and hasFirstName only string[minLength 1]
			SubClassOf: hasAge exactly 1 and hasAge only integer[>= 0]
			SubClassOf: hasGender exactly 1 and hasGender only {female, male}
			SubClassOf: hasMother exactly 1 Woman and hasFather exactly 1 Man
			SubClassOf: inverse hasChild max 2 and inverse hasGrandChild max 4
			SubClassOf: not hates Self

			ObjectProperty: hasChild
				Domain: Person
				Range: Person
				Characteristics: Asymmetric, Irreflexive

			ObjectProperty: hasMother
				Domain: Person
				Range: Woman
				SubPropertyOf: inverse hasChild
				Characteristics: Functional, Asymmetric, Irreflexive
				DisjoinWith: hasFather

			ObjectProperty: hasOffspring
				Domain: Person
				Range: Person
				SubPropertyOf: hasChild
				SubPropertyChain: hasChild o hasChild
				Characteristics: Transitive

			ObjectProperty: hasSibling
				Domain: Person
				Range: Person
				Characteristics: Transitive, Symmetric, Irreflexive

			ObjectProperty: hasBrother
				Domain: Person
				Range: Man
				SubPropertyOf: hasSibling
				Characteristics: Transitive, Asymmetric

		Class: Man
			EquivalentTo: Person that hasGender value male
			ObjectProperty: hasWife
				Domain: Citizen, Man
				Range: Citizen, Woman
				SubPropertyOf: hasSpouse, loves
				Characteristics: Functional, InverseFunctional,	Asymmetric, Irreflexive

		Class: Woman
			EquivalentTo: Person that hasGender value female
			DisjoinWith: Man							

		Class: Parent
			EquivalentTo: Person that hasChild min 1 Person

		Class: HappyFather
			SubClassOf: Man and Parent that hasChild min 1 Female
	
		Class: Teenager
			EquivalentTo: Person that hasAge some integer[>= 13 , < 20]
	
		Class: Narcissist
			EquivalentTo: Person that loves Self

		Individual: Jeff
			Annotations: rdfs:comment "Jeff is not a narcissist"
			Types: Person,
				hasChild exactly 2
			Facts: hasWife Emily,
				hasChild Ellen,
				hasAge 77,
				not loves Jeff

	second sample ontology in Manchester syntax:

		Class: Translator 
			EquivalentTo: Person and speaks min 2 Language 

		Class: Supervisor
			SubClassOf: Employee and supervises some Employee

		Class: Project
			SubClassOf: number some integer[> 0, < 5000]

		Class: Employee
			SubClassOf: works_on max 3 Project

		Class: Department
			SubClassOf: inverse works_in min 2 Employee

		Class: Manager
			SubClassOf: Employee and manages exactly 1 Department

		DataProperty: name
			Characteristics: Functional

		ObjectProperty: manages
			SubPropertyOf: works_in

		ObjectProperty: is_supervisor_of
			SubPropertyChain: manages o inverse works_in

		Class: Employee
			SubClassOf: Person and
				works_on some Project or
				supervises some (Employee and works_on some Project) or
				manages some Department

		Class: Project and receives_funds_from some US_Government_Agency
			SubClassOf: inverse works_on only (Employee and nationality value "US")

		class: CongenitalAtrialSeptalDefect
			EquivalentTo: AtrialSeptalDefect that hasAcquisitionMode some
				(AcquisitionMode that hasAbsoluteState value congenital)

		class: AtrialSeptalDefect
			EquivalentTo: PlanarDefect that hasSpecificLocation some InteratrialSeptum

		class: PlanarDefect
			SubClassOf: NonnormalBodyCavity that hasTopology some
				(Topology that hasAbsoluteState value tubular)


	visualized sample ontology - http://owlgred.lumii.lv/online_visualization/org.owl


	"Ontology Development 101: A Guide to Creating Your First Ontology" - http://protege.stanford.edu/publications/ontology_development/ontology101.pdf

	"Ontology Representation - Design Patterns and Ontologies that Make Sense" book by Rinke Hoekstra
		http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.173.6192


	OWL to natural language translation - http://robertdavidstevens.wordpress.com/2014/01/28/generating-natural-language-from-owl-and-the-uncanny-valley/


	difference between OWL2 and OWL1
		http://semantic-web-grundlagen.de/wiki/Guide_to_OWL_2_for_OWL_1_users
		http://w3.org/TR/owl2-new-features/

		OWL 1 was mainly focused on constructs for expressing information about classes and individuals, and exhibited some weakness regarding expressiveness for properties.
		OWL 2 offers new constructs for expressing additional restrictions on properties, new characteristics of properties, incompatibility of properties, property chains and keys.

	OWL history:

		Description Logics is a family of languages which correspond to (decidable) fragments of first-order logic (FOL).
		DLs offer a variable-free syntax designed for expressing knowledge about structured concepts and relations between them.
		They found their primary application in designing ontologies, conceptual structures for modeling domain knowledge, and reasoning about them.
		Modeling background knowledge has occupied one of the central places in AI since 60s.
		The approaches can be roughly classified into two major categories: those using FOL as a formal tool enabling automated reasoning, and other systems which often intuitively understandable object-oriented representation but lack formal semantics.
		Prime examples of the latter are semantic nets and, later, frames.
		The categories are in some sense complementary: strengths of one approach correspond to weaknesses of the other and vice versa.
		DLs emerged in the 80s as a bridge for taking the best from both worlds.
		It was realized that giving formal semantics to semantic nets and frames was possible without necessity to use complete proof systems for FOL.
		The first system which proposed a DL-like language with a FOL-like semantics was the famous KL-ONE.
		It suggested that the language is to be used for controlling domain terminology which is still one of the central use cases for DL, thus sticking the name "terminological languages" to early DLs.
		One especially attractive feature of semantic nets is visualization.
		The knowledge is represented as a graphical conceptual model with nodes and arcs.
		This seems to be more illustrative than a set of formulas in FOL.
		The syntax of DLs, however, allowed for expressing structured concepts and axioms in a form that was easier to analyze in order to reconstruct the diagram than FOL theories.
		Early DL systems used so called structural subsumption algorithms to derive new knowledge from explicitly represented.
		They were computationally tractable but often incomplete for many DLs, i.e., not all true statements could be derived.
		The next generation of systems started to appear in the early 90s with emergence of tableaux algorithms, which were complete proof systems for DLs.
		Unfortunately, it turned out that complete reasoning in propositionally closed DLs is PSPACE-complete.
		However, as is often the case, theoretical complexity was not the last word.
		The first DL reasoners, which demonstrated acceptable performance on real knowledge bases were KRIS, FaCT and HAM-ALC.
		They were followed by modern, highly optimized tableau reasoners, namely, FaCT++, Pellet, RACER and HermiT.
		The success of ontologies in a range of disciplines instigated standardization work on an ontology language.
		The growing popularity of DL made it the primary candidate for the logical basis of such a language.
		Two separate developments focused on OIL (Ontology Inference Layer) and DAML (DARPA Agent Markup Language) eventually led to the standardization of OWL (Web Ontology Language) under W3C.
		OWL originally appeared as three languages (OWL Lite, OWL DL, and OWL Full).
		The design and the chosen trade-off between expressivity and reasoning complexity were not flawless and it took several more years to standardize OWL 2.
		It comes as several profiles, each of which corresponds to a carefully selected DL.


<brylevkirill@gmail.com>
