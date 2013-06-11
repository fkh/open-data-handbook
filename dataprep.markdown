---
layout: default
previous: prepublication.html
next: termsofuse.html
---

V.    Data Preparation, Publication and Access
=========

The Open New York Data platform provides an open, standards-based, RESTful application programming interface  to provide automatic access to the publicly published datasets within the open data catalogue.  The platform will be optimized towards the developer community, technical users, and researchers and enable programmatic reuse.  

###A.  Standardization

The way data consumers interact and use the Open Data Platform is greatly influenced by the way the data is published. The Open Data Platform requires the data publishers to present the data in a machine-readable format to enable software tools, applications & systems to process it.  Instead of preprocessing the data, data consumers can directly access the raw data and customize the data for their own consumption needs. 

Standardizing the data publishing model on the platform in a machine readable format enables automation leading to the development of new, friendly analysis tools. The same data can be reused for another business use case without extra processing.

As part of the standardization process, the Open New York Data platform has identified the following minimum requirements:

* **Standardized Metadata Attributes**

####Common Metadata

The platform will support a common and fully described core metadata scheme for each hosted dataset and API within the data catalogue. The metadata scheme would allow data publishers to classify selected contextual fields or elements within their dataset as well as adhere to common Meta attributes identified platform-wide empowering the data consumers to build automated discovery mechanisms at a granular-level.  Using a common metadata taxonomy will allow Open New York to convey and increase discoverability of high-value datasets

* **Standardized Machine-Readable File Formats**

In order to facilitate automatic processing of the data, make it easily accessible and available in machine-readable formats, standardized open data file formats for data publishers and data consumers would be made available so that they can be uploaded, retrieved, indexed and searched.

Datasets published to the Open New York platform are machine-readable and have a clear separation of metadata from the original source data.  Data Consumers will be able to automate the process of discovery, accessibility and ingestion by using the uniform open data formats supported by the platform.

* **Standardized Domain Categories**

####Common Domain

The platform supports a common domain model that allows data publishers to identify, transform and anchor datasets in a particular domain. Using a common scheme based on categories and tags, Open New York standardizes the available domains within the platform, thus helping data consumers to retrieve datasets readily and uniformly using either the standard core metadata or extending the search using domain-specific metadata

###B.	Dataset Metadata 

Open.ny.gov adheres to core components of the Dublin Core standard for metadata ([http://www.dublincore.org/documents/dces/](http://www.dublincore.org/documents/dces/).   The ability to search and find information is enhanced by the adherence to metadata standards required with each dataset.  In addition, metadata is linked to subject categories which provides for more precise searching and document management.  

Adoption of the Dublin Core, together with standards for Open Data, maximizes adaptability and interoperability.   

####Metadata elements and definitions

The Dublin Core Metadata Initiative (DCMI) is incorporated as a non-profit organization hosted at the National Library Board of Singapore.  Its lists of elements, glossary, and FAQs were last revised in 2005, but an effort to update its User Guide is being developed at the wiki page http://wiki.dublincore.org/index.php/User_Guide.  OPEN-NY uses the current set of elements, which are required to accompany each dataset and are incorporated as follows: 

![Metadata Table](http://nys-its.github.io/open-data-handbook/img/MetadataTable.png "Metadata Table")

###C.  Datasets 

The Open Data Platform supports two classifications of datasets: tabular and geospatial.  A tabular dataset is a flat file that conforms to a predefined schema.  The schema defines the characteristics of a fixed number of columns, including the column name and data type.  A geospatial dataset contains information that can be readily rendered on an underlying map.  Examples of geospatial features include points (buildings), polylines (bus routes), and polygons (school districts), along with attribute information that describes characteristics of each spatial feature.

###Tabular Datasets

**Input File Formats**

The current Open Data Platform supports a variety of popular and standard tabular input file formats.
* CSV & TSV: Comma/Tab Separated Values
* XLS & XLSX: Microsoft Excel Formats

**Export File Formats**

Datasets can be exported for download in popular human-readable formats, machine-readable standards and streamable file formats.  The Open Data Platform currently supports the following exportable tabular file formats:
* CSV
* JSON
* PDF
* RDF
* RSS
* XLS
* XLSX
* XML

**Large File Support**

Public data often consists of historical archives, comprised of potentially millions of records collected over an extended period of time. The Open Data Platform supports the loading, exporting and visualization of large datasets (> 1GB). 

**Geocoding**

The Open Data New York Platform supports geocoding services which convert human-readable address information into mappable coordinates (Latitude/Longitude).  


###Geo-Spatial Datasets

**Input File Formats**

The Open Data Platform supports two data formats for geospatial information.  The appropriate format is dependent on the specific characteristics of the underlying geographic data.
* Points: All Tabular File Formats or Shapefile
* Polylines:  Shapefile
* Polygons: Shapefile

Point data can be stored in either tabular or shapefile format.  Tabular formatting of points requires either columns for latitude and longitude, or complete address information that can be geocoded.  In contrast, polylines and polygons define complex geometric structures that are not easily defined as column attributes.  Therefore, shapefile format is a preferred format for these complex geographic structures.  

Each shapefile (at a minimum) should contain the following files:
* .shp: Defines the geometry (shapes)
* .dpf: Defines the attribute table 
* .prj: Projection, ensures the feature locations are accurately rendered on the map
* .shx: Shape indexing file, for efficient processing	

Other supported geospatial formats may include KML, KMZ.

Geospatial data is usually organized as a collection of features that define a layer.   Layers can be overlaid on top of one another, allowing visualization spatial relations, spatial queries, and analysis.  

**Export File Formats**

Geospatial data contains geographic features and attribute data that defines the properties of geographic features.   Attributes are stored in a tabular format with unique key references to the associated geographic features.   Two export methodologies are supported for exporting geographic information:  geospatial and attribute.  Attribute layers can be exported as tabular data export file formats as identified earlier.  

Geospatial information can be exported in the following formats:   
* Shapefile
* KML
* KMZ


####D.  Application Program Interface (API)

All data on the platform can be consumed via an Application Program Interface (API) which provides direct access to the raw data for developers. 

#####Access to Datasets

The Open New York Platform supports the existence of an API Strategy that allows the developer community to dynamically query a dataset within the data catalogue. Each hosted dataset within the data catalogue will:

* Be readily and uniformly accessible.
* Be available for automated processing by applications and systems
* Have a standard API Endpoint

The Endpoint points to a RESTful implementation of the underlying dataset that has been accessed.  All communication with the API is done through an HTTPS protocol. The platform provides the following preferred response types which are made available by the “extension” of the API or by HTTP “Accepts” headers:

* JSON 
* XML
* CSV
* RDF


#####Featured API Catalog

Additionally, the Open New York Platform supports the creation of a featured API Catalog that provides custom endpoints to the developer community to dynamically query the raw dataset based on “specified” dataset elements. The featured API Catalog is categorized and tagged using the common domain and metadata schema identified in Section A and Section B.1.  

####E.	Data Refresh Process

Specific guidance regarding refresh will be addressed in technical and working documents previously referenced.  Four mechanisms are supported for refreshing a dataset:
* Replace: All existing records are removed and new records are inserted.
* Append: New dataset records are inserted
* Update: Existing records are modified 
* Delete: Existing records are removed

The frequency of updates is included in the metadata each provides with each dataset (see metadata posting frequency).


