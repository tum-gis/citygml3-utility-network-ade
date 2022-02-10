# citygml3-utility-network-ade

The CityGML extension UtilityNetwork ADE defines concepts which allow for modelling different types of networks in the context of 3D city models, such as electricity, freshwater, wastewater, gas or telecommunication networks.
Please refer to https://github.com/TatjanaKutzner/CityGML-UtilityNetwork-ADE for general information on the Utility Network ADE.

**This repository provides the CityGML Utility Network ADE for CityGML 3.0.**

**Please note that this CityGML-3.0-compliant representation of the CityGML Utility Network ADE is a first draft and still may be subject to changes.**

The CityGML Utility Network ADE for CityGML 2.0 is available here: https://github.com/TatjanaKutzner/CityGML-UtilityNetwork-ADE.

<<<<<<< HEAD

# Updating the CityGML Utility Network ADE to CityGML 3.0
=======
## Updating the CityGML Utility Network ADE to CityGML 3.0
>>>>>>> origin/master

The new version 3.0 of the international OGC standard CityGML was published in September 2021 by the Open Geospatial Consortium (OGC). The  CityGML 3.0 standard is available here: https://docs.ogc.org/is/20-010/20-010.html. CityGML 3.0 introduces several new concepts, amongst others a new Space concept, a revised Level of Detail (LOD) concept, the concept of top-level feature types, and a revised concept for defining Application Domain Extensions (ADEs). All these concepts are of relevance to the CityGML Utility Network ADE as well.

To make use of the new CityGML 3.0 concepts in the ADE, several modifications have been applied to the UML model of the CityGML 2.0 Utility Network ADE. These modifications are described in more detail in ["Updating the Utility Network ADE to comply with CityGML 3.0"](Updating-to-CityGML3.0.md).

In addition, few further changes have been applied to the UML model, mainly because the current modelling in the CityGML 2.0 Utility Network ADE did not seem correct. These modifications are described in ["Changes"](CHANGES.md).

## Resources

The **UML model** of the CityGML 3.0 Utility Network ADE was created using the software Enterprise Architect.  
The UML folder provides
- the Enterprise Architect file that defines the UML model and
- a PDF file that depicts the UML diagrams as well.

The Enterprise Architect file defining the official CityGML 3.0 Conceptual Model (available under https://github.com/opengeospatial/CityGML-3.0CM/releases/download/3.0.0-final.2021.02.23/CityGML_3.0_Consolidated_Draft.eap) was used as basis for creating the UML model of the CityGML 3.0 Utility Network ADE.

The **XML Schema file** of the CityGML 3.0 Utility Network ADE was derived automatically from the UML model using the software ShapeChange.  
The XSD folder provides
- the derived XML Schema file and
- the derived code list dictionaries.

**ShapeChange** requires a configuration file to be able to derive the XML Schema file and code list dictionaries.  
The ShapeChange folder contains
- the ShapeChange configuration file that was used for the derivation.
For further information on how to use ShapeChange, please refer to http://shapechange.net/.

## Samples

Test data sets for the CityGML 3.0 Utility Network ADE will be provided in the future.

<<<<<<< HEAD
# CityGML Utility Network ADE

The following papers provide detailed information on the CityGML Utility Network ADE, use cases and projects that have applied the ADE:
- Becker, T., Nagel, C. & Kolbe, T. H., 2011: Integrated 3D Modeling of Multi-utility Networks and Their Interdependencies for Critical Infrastructure Analysis. Advances in 3D Geo-Information Sciences, Lecture Notes in Geoinformation and Cartography, Kolbe, T. H., König, G. & Nagel, C. (eds.), Springer, Berlin Heidelberg, 1-20: http://mediatum.ub.tum.de/doc/1145740/358854.pdf
- Becker, T., Nagel, C. & Kolbe, T. H., 2013: Semantic 3D Modeling of Multi-Utility Networks in Cities for Analysis and 3D Visualization. Progress and New Trends in 3D Geoinformation Sciences, Lecture Notes in Geoinformation and Cartography, Pouliot, J., Daniel, S., Hubert, F. & Zamyadi, A. (eds.), Springer, Berlin Heidelberg, 41-62: http://mediatum.ub.tum.de/doc/1145724/287720.pdf
- Kutzer, T. & Kolbe, T. H., 2016: Extending Semantic 3D City Models by Supply and Disposal Networks for Analysing the Urban Supply Situation. Publikationen der Deutschen Gesellschaft für Photogrammetrie, Fernerkundung und Geoinformation e.V., Volume 25, Kersten, T. P. (ed.), 36. Wissenschaftlich-Technische Jahrestagung der DGPF, June 7-9 in Bern, 382-394: http://www.dgpf.de/src/tagung/jt2016/proceedings/papers/36_DLT2016_Kutzner_Kolbe.pdf
- Hijazi, I., Kutzner, T. & Kolbe, T. H., 2017: Use Cases and their Requirements on the Semantic Modeling of 3D Supply and Disposal Networks. Publikationen der Deutschen Gesellschaft für Photogrammetrie, Fernerkundung und Geoinformation e.V., Volume 26, Kersten, T. P. (ed.), 37. Wissenschaftlich-Technische Jahrestagung der DGPF, March 8-10 in Wuerzburg, 288-301: http://www.dgpf.de/src/tagung/jt2017/proceedings/proceedings/papers/28_DGPF2017_Hijazi_et_al.pdf
- Kutzner, T., Hijazi, I. & Kolbe, T. H., 2018: Semantic Modelling of 3D Multi-utility Networks for Urban Analyses and Simulations – The CityGML Utility Network ADE. International Journal of 3-D Information Modeling (IJ3DIM), 7(2), 1-34: https://mediatum.ub.tum.de/doc/1475038/1475038.pdf
- Boates, I., Agugiaro, G., & Nichersu, A., 2018: Network Modelling and Semantic 3D City Models: Testing the Maturity of the Utility Network ADE for CityGML with a Water Network Test Case. ISPRS Annals of Photogrammetry, Remote Sensing and Spatial Information Science, IV-4, 13-20: https://doi.org/10.5194/isprs-annals-IV-4-13-2018
- den Duijn, X., Agugiaro, G. & Zlatanova, S., 2018: Modelling Below- and Above-Ground Utility Network Features with the CityGML Utility Network ADE: Experiences from Rotterdam. ISPRS Annals of Photogrammetry, Remote Sensing and Spatial Information Science, IV-4/W7, 43-50: https://doi.org/10.5194/isprs-annals-IV-4-W7-43-2018
- Ortega, S.; Wendel, J.; Santana, J.M.; Murshed, S.M.; Boates, I.; Trujillo, A.; Nichersu, A.; Suárez, J.P. Making the Invisible Visible—Strategies for Visualizing Underground Infrastructures in Immersive Environments. ISPRS Int. J. Geo-Inf. 2019, 8, 152: https://www.mdpi.com/2220-9964/8/3/152


# CityGML
=======
## CityGML
>>>>>>> origin/master

The [OGC CityGML](http://www.opengeospatial.org/standards/citygml) standard defines a conceptual model and exchange format for the representation, storage and exchange of semantic 3D city models. The current version CityGML 3.0 allows for exchanging 3D city models in various exchange formats including GML 3.2.1 and GML 3.3, whereas the version CityGML 2.0 uses GML 3.1.1 for data exchange. The aim of the development of CityGML is to reach a common definition of the basic entities, attributes, and relations of a 3D city model. By means of so-called Application Domain Extensions (ADEs), the core model of CityGML can be extended systematically by application-specific attributes and object types.

CityGML is an international OGC standard and can be used free of charge.
