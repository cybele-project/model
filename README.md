# CYBELE Common Semantic Model v2.0

The CYBELE Semantic Model will serve as a common reference model (Figure 21) for the semantic annotation and sharing of data including sensor data, satellite and aerial image data, statistical data, streaming data, video data, weather & climate data, supporting the on-demand discovery and exploration.  This semantic model will be utilized in the semantic annotation, sharing and inter-connection of CYBELE datasets. In particular, it will be used to create metadata for the datasets (e.g. data theme, spatial/temporal coverage, data format, periodicity, licence). The semantic annotation of the data will facilitate:

- The discovery and exploration of the CYBELE datasets. The component “Query Builder” will use the semantic model to identify available datasets that cover the users’ needs (e.g. “data of area X at the time frame [2018 - 2019] that contain data for soya yield”.)
- Data interoperability. The data imported at the CYBELE platform will be aligned with the CYBELE Common Semantic Model. Specifically, the dimensions (e.g. time, geography) and the measures (e.g. temperature, weight) of the imported data will be aligned with the dimensions and measures defined by the model.
- Data access. The CYBELE Common Semantic Model contains structural and access metadata that enable the formulation of queries (e.g. SQL). Specifically, the model contains metadata describing the DB and Table where the dataset is stored. This information accompanied with the metadata for dimensions and measures enable the generation of queries.


The CYBELE Common Semantic Model will serve as a common reference model for the semantic annotation and sharing of CYBELE demonstrators data supporting the on demand data discovery and exploration. In particular, it will be used to create metadata for the datasets (e.g. data theme, spatial/temporal coverage, data format, periodicity, licence). The semantic annotation of the data will facilitate:

- The discovery and exploration of the CYBELE datasets. The component “Query Builder” will use the semantic model to formulate queries in order to identify available datasets that cover the users’ needs (e.g. "data of area X at the time frame [2018 - 2019] that contain data for soya yield".)
- The description of the data needs of CYBELE apps. CYBELE will produce apps that can be reused in different context using different data. The semantic model will describe the requirements that the data should match in order to be compatible with the created apps (e.g. the data should have a spatial and temporal dimension)

The design and implementation of the model is based on: i) the first version of the model described at D3.1, ii) the updated user stories and demonstrators’ requirements (functional and non-functional) documented in deliverable D1.2 and D1.3, iii) the new objectives of the model i.e. add cardinalities at the model, propose a set of code lists to be used with the model, define aspects related to the governance of the model and define an application profile of the model and iv) feedback received by the project’s demonstrators. The user stories and the requirements are further analysed and specialized for the needs of this deliverable. Additionally, the design of the CYBELE Common Semantic Model re-uses existing models and vocabularies such as DCAT, StatDCAT, GeoDATC, INSPIRE, SSN ontology, QB vocabulary and PROV-O. An application profile of the model is also defined to cover the needs of the agriculture and livestock farming domains.

### Model description

The main classes of the model are:
- The `Dataset` is a collection of data published by a specific publisher.
- The `Repository` is a collection of metadata about Datasets.
- The `Activity` represents the way/method the Dataset was generated. This activity may involve Agents e.g. human, sensor.
- The `Distribution` represents an accessible form of a Dataset e.g. downloadable file, Data Service, Database.
- The `Structure` include structural information of Datasets (including Dimensions and Measures). This information facilitates the access to the Dataset e.g. query the Dataset.

From a Dataset perspective the above main classes are related to the Dataset. So the Dataset: i) is part of a Repository that contains many datasets, ii) is published by a Publisher that can be a person or an organization, iii) is available through a Distribution, iv) is the result of an Activity that involves Agents and v) has a structure including Dimensions and Measures. Additionally, the Dataset has also properties including the Theme (a categorization of the data based on their domain), Language, Issuing/Modification date, Update frequency, Spatial/Temporal coverage, Spatial/Temporal resolution, Access rights, Standard and Web page. 

Regarding the other classes: i) the Dataset Distribution has properties including the License, Format, Size and Download URL, ii) the Data Service and Database has properties related to the access URL (Connection URL and Endpoint URL respectively), iii) the Measure has properties that define the Unit of measure and the Measure Range and iv) the Dimensions has a property for the Range.


<img src="/images/model_cybele.jpg"  width="800" >
