# citygml3-utility-network-ade

The CityGML extension UtilityNetwork ADE defines concepts which allow for modelling different types of networks in the context of 3D city models, such as electricity, freshwater, wastewater, gas or telecommunication networks.
Please refer to https://github.com/TatjanaKutzner/CityGML-UtilityNetwork-ADE for general information on the Utility Network ADE.

**This repository provides the CityGML Utility Network ADE for CityGML 3.0.**

**Please note that this CityGML-3.0-compliant representation of the CityGML Utility Network ADE is a first draft and still may be subject to changes.**

The CityGML Utility Network ADE for CityGML 2.0 is available here: https://github.com/TatjanaKutzner/CityGML-UtilityNetwork-ADE.

# Updating the CityGML Utility Network ADE to CityGML 3.0

The new version 3.0 of the international OGC standard CityGML was published in September 2021 by the Open Geospatial Consortium (OGC). The  CityGML 3.0 standard is available here: https://docs.ogc.org/is/20-010/20-010.html. CityGML 3.0 introduces several new concepts, amongst others a new Space concept, a revised Level of Detail (LOD) concept, the concept of top-level feature types, and a revised concept for defining Application Domain Extensions (ADEs). All these concepts are of relevance to the CityGML Utility Network ADE as well.

To make use of the new CityGML 3.0 concepts in the ADE, several modifications have been applied to the UML model of the CityGML 2.0 Utility Network ADE. These modifications are described in more detail [here](Modifications.md).

# Resources

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

# Samples

Test data sets for the CityGML 3.0 Utility Network ADE will be provided in the future.

# CityGML

The [OGC CityGML](http://www.opengeospatial.org/standards/citygml) standard defines a conceptual model and exchange format for the representation, storage and exchange of semantic 3D city models. The current version CityGML 3.0 allows for exchanging 3D city models in various exchange formats including GML 3.2.1 and GML 3.3, whereas the version CityGML 2.0 uses GML 3.1.1 for data exchange. The aim of the development of CityGML is to reach a common definition of the basic entities, attributes, and relations of a 3D city model. By means of so-called Application Domain Extensions (ADEs), the core model of CityGML can be extended systematically by application-specific attributes and object types.

CityGML is an international OGC standard and can be used free of charge.
