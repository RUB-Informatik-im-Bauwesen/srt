Markdown documentation created by [pyLODE](http://github.com/rdflib/pyLODE) 2.8.3

# Ontology for Spatial Reasoning in Tunnel Projects

## Metadata
* **URI**
  * `http://w3id.org/srt#`
* **Publisher(s)**
  * Chair of Computing in Engineering, Ruhr University Bochum
* **Creators(s)**
  * Marcel Stepien, Ruhr University Bochum
* **Modified**
  * 2021-09-29
* **Version Information**
  * 0.1
* **Ontology RDF**
  * RDF ([turtle](https://github.com/RUB-Informatik-im-Bauwesen/srt/blob/main/Ontology_for_Spatial_Reasoning_in_Tunnel_Projects_(srt).ttl))
  * RDF ([XML](https://github.com/RUB-Informatik-im-Bauwesen/srt/blob/main/Ontology_for_Spatial_Reasoning_in_Tunnel_Projects_(srt).rdf))

### Description
<p>A ontology for creating a unified knowledge base as rdf graph containing geometric WKT profile representations of elements from a BIM and GIS ingetrated environment for spatial reasoning. The ontology also provides descriptors to add personal project information and generic resources to handle geolocalization and projection informations of the wktLiterals.</p>

## Table of Contents
1. [Classes](#classes)
1. [Object Properties](#objectproperties)
1. [Datatype Properties](#datatypeproperties)
1. [Namespaces](#namespaces)
1. [Legend](#legend)

## Classes
[ProjectMeta](#ProjectMeta),
[RelationContainer](#RelationContainer),
[SpatialObject](#SpatialObject),
### ProjectMeta
Property | Value
--- | ---
URI | `http://w3id.org/srt#ProjectMeta`
Description | <p>A class for describing relevant context used in the creation of the instance RDF graph.</p>
Restrictions |[srt:environmentVersion](http://w3id.org/srt#environmentVersion) (op) **exactly** 1<br />[srt:user](http://w3id.org/srt#user) (op) **exactly** 1<br />[srt:globalReference](http://w3id.org/srt#globalReference) (op) **exactly** 1<br />[srt:title](http://w3id.org/srt#title) (op) **exactly** 1<br />[srt:environment](http://w3id.org/srt#environment) (op) **exactly** 1<br />[srt:projection](http://w3id.org/srt#projection) (op) **exactly** 1<br />[rdfs:label](http://www.w3.org/2000/01/rdf-schema#label) **min** 1<br />
In domain of |[srt:globalReference](http://w3id.org/srt#globalReference) (op)<br />[srt:title](http://w3id.org/srt#title) (op)<br />[srt:environment](http://w3id.org/srt#environment) (op)<br />[srt:projection](http://w3id.org/srt#projection) (op)<br />[srt:environmentVersion](http://w3id.org/srt#environmentVersion) (op)<br />[srt:user](http://w3id.org/srt#user) (op)<br />
In range of |[srt:hasMeta](http://w3id.org/srt#hasMeta) (op)<br />
### RelationContainer
Property | Value
--- | ---
URI | `http://w3id.org/srt#RelationContainer`
Description | <p>Represents a collection of registered objects (SpatialObject). The collection require a unique identifier to enable management of different instances for comparison and reasoning among collections.</p>
Restrictions |[rdfs:label](http://www.w3.org/2000/01/rdf-schema#label) **min** 1<br />[srt:hasMeta](http://w3id.org/srt#hasMeta) (op) **exactly** 1<br />[srt:identifier](http://w3id.org/srt#identifier) (dp) **exactly** 1<br />[srt:hasObject](http://w3id.org/srt#hasObject) (op) **min** 0<br />
In domain of |[srt:hasObject](http://w3id.org/srt#hasObject) (op)<br />[srt:identifier](http://w3id.org/srt#identifier) (dp)<br />[srt:hasMeta](http://w3id.org/srt#hasMeta) (op)<br />
### SpatialObject
Property | Value
--- | ---
URI | `http://w3id.org/srt#SpatialObject`
Description | <p>A spatial object that is derived form BIM and GIS planning data. Contains a WKT profile representation and references its origin by resource or identifier.</p>
Restrictions |[srt:dataType](http://w3id.org/srt#dataType) (dp) **exactly** 1<br />[geo:asWKT](http://www.opengis.net/ont/geosparql#asWKT) **exactly** 1<br />[srt:sourceItentifier](http://w3id.org/srt#sourceItentifier) (op) **exactly** 1<br />[srt:hasWKTType](http://w3id.org/srt#hasWKTType) (op) **exactly** 1<br />[rdfs:label](http://www.w3.org/2000/01/rdf-schema#label) **min** 1<br />[srt:sourceRelation](http://w3id.org/srt#sourceRelation) (op) **min** 0<br />
In domain of |[srt:dataType](http://w3id.org/srt#dataType) (dp)<br />[srt:hasWKTType](http://w3id.org/srt#hasWKTType) (op)<br />[srt:sourceItentifier](http://w3id.org/srt#sourceItentifier) (op)<br />[srt:sourceRelation](http://w3id.org/srt#sourceRelation) (op)<br />
In range of |[srt:hasObject](http://w3id.org/srt#hasObject) (op)<br />

## Object Properties
[environment](#environment),
[environmentVersion](#environmentVersion),
[globalReference](#globalReference),
[hasMeta](#hasMeta),
[hasObject](#hasObject),
[hasWKTType](#hasWKTType),
[projection](#projection),
[sourceItentifier](#sourceItentifier),
[sourceRelation](#sourceRelation),
[title](#title),
[user](#user),
[](environment)
### environment
Property | Value
--- | ---
URI | `http://w3id.org/srt#environment`
Description | The environment the project was generated from.
Domain(s) |[srt:ProjectMeta](http://w3id.org/srt#ProjectMeta) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](environmentVersion)
### environmentVersion
Property | Value
--- | ---
URI | `http://w3id.org/srt#environmentVersion`
Description | The version of the environment the project was generated from.
Domain(s) |[srt:ProjectMeta](http://w3id.org/srt#ProjectMeta) (c)<br />
Range(s) |[xsd:integer](http://www.w3.org/2001/XMLSchema#integer) (c)<br />
[](globalReference)
### globalReference
Property | Value
--- | ---
URI | `http://w3id.org/srt#globalReference`
Description | Generic placeholder for the global reference point. Usually providing the location of the coordinate system default origin.
Domain(s) |[srt:ProjectMeta](http://w3id.org/srt#ProjectMeta) (c)<br />
Range(s) |[rdfs:resource](http://www.w3.org/2000/01/rdf-schema#resource) (c)<br />
[](hasMeta)
### hasMeta
Property | Value
--- | ---
URI | `http://w3id.org/srt#hasMeta`
Description | A generic resource containing project meta data of the originating planning environment.
Domain(s) |[srt:RelationContainer](http://w3id.org/srt#RelationContainer) (c)<br />
Range(s) |[srt:ProjectMeta](http://w3id.org/srt#ProjectMeta) (c)<br />
[](hasObject)
### hasObject
Property | Value
--- | ---
URI | `http://w3id.org/srt#hasObject`
Description | Lists of all relevant spatial objects assigned to the relation container.
Domain(s) |[srt:RelationContainer](http://w3id.org/srt#RelationContainer) (c)<br />
Range(s) |[srt:SpatialObject](http://w3id.org/srt#SpatialObject) (c)<br />
[](hasWKTType)
### hasWKTType
Property | Value
--- | ---
URI | `http://w3id.org/srt#hasWKTType`
Description | Classification of the wkt literals contained by the spatial object. Known type resources of the gml specification are recommended to be used.
Domain(s) |[srt:SpatialObject](http://w3id.org/srt#SpatialObject) (c)<br />
Range(s) |[gml:AbstractGeometry](http://www.opengis.net/ont/gml#AbstractGeometry) (c)<br />
[](projection)
### projection
Property | Value
--- | ---
URI | `http://w3id.org/srt#projection`
Description | Generic placeholder for projection informations to enable correct geometry transformation.
Domain(s) |[srt:ProjectMeta](http://w3id.org/srt#ProjectMeta) (c)<br />
Range(s) |[rdfs:resource](http://www.w3.org/2000/01/rdf-schema#resource) (c)<br />
[](sourceItentifier)
### sourceItentifier
Property | Value
--- | ---
URI | `http://w3id.org/srt#sourceItentifier`
Description | Includes an identifier that should pointing to the source object and used for referencing if a srt:sourceRelation can not be provided in RDF.
Domain(s) |[srt:SpatialObject](http://w3id.org/srt#SpatialObject) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](sourceRelation)
### sourceRelation
Property | Value
--- | ---
URI | `http://w3id.org/srt#sourceRelation`
Description | Provides a connection to the originating source of information that has been derived into a spatial object. Can be used to access meta information for querying by linking a resource containing additional information about the spatial object. Only necessary if a source object exists.
Domain(s) |[srt:SpatialObject](http://w3id.org/srt#SpatialObject) (c)<br />
Range(s) |[rdfs:resource](http://www.w3.org/2000/01/rdf-schema#resource) (c)<br />
[](title)
### title
Property | Value
--- | ---
URI | `http://w3id.org/srt#title`
Description | The title of the project in the context of which the srt:RelationContainer was created.
Domain(s) |[srt:ProjectMeta](http://w3id.org/srt#ProjectMeta) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />
[](user)
### user
Property | Value
--- | ---
URI | `http://w3id.org/srt#user`
Description | The user managing or owning the created srt:RelationContainer.
Domain(s) |[srt:ProjectMeta](http://w3id.org/srt#ProjectMeta) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Datatype Properties
[dataType](#dataType),
[identifier](#identifier),
[](dataType)
### dataType
Property | Value
--- | ---
URI | `http://w3id.org/srt#dataType`
Description | A type hint describing the origin of the spatial resource. Such as Alignment, Cadastral or Buildingd from CityGML. If none of the listet types apply, Unknown should be used and a custom type can then be references using srt:sourceRelation instead.
Domain(s) |[srt:SpatialObject](http://w3id.org/srt#SpatialObject) (c)<br />
[](identifier)
### identifier
Property | Value
--- | ---
URI | `http://w3id.org/srt#identifier`
Description | The identification of the relation container as text information. Must be unique within the register. It is recomended to insert a GUID.
Domain(s) |[srt:RelationContainer](http://w3id.org/srt#RelationContainer) (c)<br />
Range(s) |[xsd:string](http://www.w3.org/2001/XMLSchema#string) (c)<br />

## Named Individuals
## Namespaces
* **dc**
  * `http://purl.org/dc/elements/1.1/`
* **dct**
  * `http://purl.org/dc/terms/`
* **foaf**
  * `http://xmlns.com/foaf/0.1/`
* **geo**
  * `http://www.opengis.net/ont/geosparql#`
* **geof**
  * `http://www.opengis.net/def/function/geosparql/`
* **gml**
  * `http://www.opengis.net/ont/gml#`
* **owl**
  * `http://www.w3.org/2002/07/owl#`
* **prov**
  * `http://www.w3.org/ns/prov#`
* **rdf**
  * `http://www.w3.org/1999/02/22-rdf-syntax-ns#`
* **rdfs**
  * `http://www.w3.org/2000/01/rdf-schema#`
* **sdo**
  * `https://schema.org/`
* **skos**
  * `http://www.w3.org/2004/02/skos/core#`
* **srt**
  * `http://w3id.org/srt#`
* **vann**
  * `http://purl.org/vocab/vann/`
* **xsd**
  * `http://www.w3.org/2001/XMLSchema#`

## Legend
* Classes: c
* Object Properties: op
* Functional Properties: fp
* Data Properties: dp
* Annotation Properties: dp
* Properties: p
* Named Individuals: ni
