## Brainstorming:

### Topics

* defining the field(s): Digital Humanities, Digital Classics
* versioning, writing, annotating, encoding
* reading, editing, translating, collating

### Overview

0. technical prologue (find a better name)

	**Goal**: introduce the students to the main technical concepts/tools that will be used during the course.

	1. managing data (i.e. files) in the XXI century
		* version control
		* GIT
			* cfr. <https://betterexplained.com/articles/aha-moments-when-learning-git/>
		* GIT and GitHub
		* practical exercise
			* create a github account
			* fork the course repo on github
	2. text editor
		* installation of Atom
		* installation of atom plugins: git/github, markdown
		* edit in Atom a given document (e.g. each student adds her own interests to a common file)

1. reading & annotating
	1. tools and resources to read Greek/Latin texts
	2. text analysis => Voyant
	3. annotations:
		- web annotations: hypothesis.js
		- annotations of texts with Recogito
		- <https://twitter.com/JD_PhD/status/915928777674383361>
2. writing
	1. academic writing
		* managing bibliographies => Zotero
		* Pandoc, an alternative to MS Word
		* markdown, as a gentle introduction to the concept of markup  
			- syntax(es)
			- tools
			- things you can do with markdown
				- MD in Authorea for publishing
				- MD + pandoc as an alternative to Word
				- one step further: [CiteDown 2 MarkDown](https://github.com/neelsmith/cd2md)
	2. writing => editing
		- TEI/XML from Atom (cfr. <https://github.com/neelsmith/atomic-tei>)
		- <http://tei-web-editor.herokuapp.com/>
3. translating
	- Ugarit: translation alignment
4. collating
	- not sure


## Software required for the course

- internet browser: Firefox, w/ plugins:
	- Zotero
	- Alpheios tools
	- hypothesis plugin for FF
- text/code editor: Atom, w/ plugins
	- git
	- markdown
	- TEI validation (?) << install in classroom
- VisualConc (?)

## Links

###

what is DH: <http://www.digitalhumanities.org/dhq/vol/8/1/000172/000172.html>

### TEI & Markup

- <https://en.wikipedia.org/wiki/Comparison_of_document_markup_languages>
- critical apparatus, franz fischer, mqdq
- diplomatic transcription, critical edition

### Epidoc:

- https://digicademy.github.io/2017-EpiDoc-WS/#/step-28
- http://epidoc.dainst.org/
- http://www.stoa.org/epidoc/gl/latest/intro-eps.html

### data and Version control:

- https://xkcd.com/1459/

## Notes about lecture 1

- GIT commands:
	* `git init`
	* `git status` (and explain `.gitignore`)
	* `git log` 
	* `git add`
	* `git commit`
	* `git pull/push/branch`
- GIT concepts:
	* concept of diff
	* pulling
	* pushing
	* branches
- GitHub concepts:
	* pull request
	* cloning a repo
	* forking a repo
	* issues (opening/closing)

## Notes about lecture 4 (annotating)

* from human readable to machine readable annnotations
* machine-readable annotations => RDF as a form of annotation
* Annotation Collaboration Ontology
* introduction to SW and LOD
	- main principles of LOD and SW (URIs)
	- serialization formats
	- content negotiation and ser. formats

```

curl --header "Accept: application/json" https://pleiades.stoa.org/places/570028

curl --header "Accept: text/turtle" https://pleiades.stoa.org/places/570028

curl --header "Accept: application/rdf+xml" https://pleiades.stoa.org/places/570028

```
	
* example from Pelagios

```
@prefix xsd: <http://www.w3.org/2001/XMLSchema> . 
@prefix pelagios: <http://pelagios.github.io/vocab/terms#> . 
@prefix relations: <http://pelagios.github.io/vocab/relations#> . 
@prefix dcterms: <http://purl.org/dc/terms/> . 
@prefix foaf: <http://xmlns.com/foaf/0.1/> . 
@prefix pleiades: <http://pleiades.stoa.org/vocabularies/time-periods> . 
@prefix oa: <http://www.w3.org/ns/oa#> . 
@prefix cnt: <http://www.w3.org/2011/content#> . 
@prefix svcs: <http://rdfs.org/sioc/services#> .

<http://edh-www.adw.uni-heidelberg.de/edh.inscriptions.n3#HD019985> a pelagios:AnnotatedThing ;
 dcterms:title "votive inscription of Bostra, bei (modern Il-Kefr) HD019985" ;
 dcterms:identifier <http://edh-www.adw.uni-heidelberg.de/edh/inschrift/HD019985> ;
 foaf:homepage <http://edh-www.adw.uni-heidelberg.de/edh/inschrift/HD019985> ;
 dcterms:language "la" .

<http://edh-www.adw.uni-heidelberg.de/edh.inscriptions.n3#HD019985/annotations/1> a oa:Annotation ;
 oa:hasTarget <http://edh-www.adw.uni-heidelberg.de/edh.inscriptions.n3#HD019985> ;
 oa:hasBody <http://pleiades.stoa.org/places/678073> ;
 oa:hasBody [ cnt:chars "POINT (32.517831000 36.483690000)"; dcterms:format "application/wkt" ] ;
 pelagios:relation relations:foundAt ;
 oa:annotatedBy <http://edh-www.adw.uni-heidelberg.de/edh/bearbeiter/grieshaber> ;
 oa:annotatedAt "2017-11-01:17:45:00Z"^^xsd:date .
```

* <del>IIIF and annotations</del>
* Pelagios and its tools


## Notes about lecture 5 (Dig. Ed. + TEI)

- what is a bit missing:
	* distinction of types of digital editions (diplomatic, philogenetic, etc.)
	* Epidoc and Epidoc-related projects
	* Papyrological navigator (editorial model, integration w/ github)


## TEI exercise:

- https://www.youtube.com/watch?time_continue=18&v=CJ4oAp176dE
- https://github.com/DigitalLatin/training
- https://digitallatin.github.io/guidelines/LDLT-Guidelines.html
- TEI web editor:
	* login with github account
	* load and display example data
	* show that