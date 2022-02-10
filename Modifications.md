# Updating the Utility Network ADE to comply with CityGML 3.0

CityGML 3.0 introduces several new concepts, amongst others a new Space concept, a revised Level of Detail (LOD) concept, the concept of top-level feature types, and a revised concept for defining Application Domain Extensions (ADEs). All these concepts are of relevance to the CityGML Utility Network ADE as well. To make use of these concepts in the ADE, several modifications have been applied to the UML model of the [CityGML 2.0 Utility Network ADE](https://github.com/TatjanaKutzner/CityGML-UtilityNetwork-ADE). In the following, information is provided on these modifications to adapt the ADE to the new CityGML version 3.0.

The UML diagrams of the CityGML 3.0 Utility Network ADE, which contain the modifications described here, can be found in this [PDF](UML/UML_diagrams_CityGML_3.0_UtilityNetworkADE.pdf) and [Enterprise Architect project](UML/CityGML_3.0_UtilityNetworkADE.eap).

## Top-level feature types

CityGML 3.0 introduces the concept of top-level feature types. Top-level feature types represent the main components of the conceptual model and may be further semantically and spatially decomposed and substructured into parts. In the CityGML 3.0 UML model, UML classes representing top-level feature types are marked by the UML stereotype «TopLevelFeatureType».

In the CityGML 3.0 Utility Network ADE, the UML class _Network_ repesents the main component of a utility network which can be decomposed into subnetworks and individual network components; thus, this class receives the UML stereotype «TopLevelFeatureType».

## ADE features types

The CityGML Utility Network ADE defines several feature types.
As specified in the CityGML 3.0 standard, feature types in an ADE shall be derived from the most suitable CityGML feature type. This can be the root feature type _AbstractFeature_ or a subclass thereof, such as _AbstractFeatureWithLifespan_ or _AbstractCityObject_. Feature types representing objects with geometry shall be derived from _AbstractSpace_ or _AbstractSpaceBoundary_ or from one of their subclasses. The CityGML 3.0 Space concept distinguishes feature types into _spaces_ and _space boundaries_ depending on whether the objects have a volumetric extent (e.g. buildings, bodies of water, trees) or an areal extent and delimit and connect spaces (e.g. wall and roof surfaces, water surface). Depending on whether the space objects are bounded by physical or virtual spatial boundaries, they can also be derived from the classes _AbstractPhysicalSpace_ or _AbstractLogicalSpace_. Furthermore, physical spaces can be derived from the classes _AbstractOccupiedSpace_ or _AbstractUnoccupiedSpace_, depending on whether they occupy space in the urban environment or not.

Based on these rules, the CityGML 3.0 Utility Network ADE has been adapted in such a way that the ADE feature types are derived from the following CityGML 3.0 UML classes:

- The class _Network_ remains a subclass of _AbstractCityObject_ as in the CityGML 2.0 Utility Network ADE. Network features represent city objects, but they do not have spatial properties. Spatial properties are only defined for the individual network features of which the network is composed.

- The class _AbstractNetworkFeature_ becomes a subclass of _AbstractOccupiedSpace_. All network features represent objects that occupy space and have spatial properties.

- The classes _NetworkGraph_, _FeatureGraph_, _AbstractLink_, _Party_, _Construction_, _MaterialLayer_, _Material_, _RoleInNetwork_, and _AbstractMedium_ become subclasses of _AbstractFeatureWithLifespan_. These classes define features in the sense of abstractions of real-world phenomena, but these features do not represent city objects and, thus, neither represent spaces nor space boundaries.

- The class _SupplyArea_ remains a subclass of _CityObjectGroup_ as in the CityGML 2.0 Utility Network ADE. Since _CityObjectGroup_ has become a subclass of _AbstractLogicalSpace_ in CityGML 3.0, also the supply area represents now a logical space.

## Spatial properties of ADE feature types

By deriving a feature type from one of the space or space boundary classes, the feature type automatically inherits the predefined spatial properties as well. In addition, an ADE can define additional spatial properties for its feature types. Property names should then start with the prefix _lod0_, _lod1_, _lod2_, or _lod3_ to indicate the Level of Detail this spatial property represents.

The CityGML 2.0 Utility Network ADE defines various spatial properties for the network features. By making the class _AbstractNetworkFeature_ a subclass of _AbstractOccupiedSpace_ in the CityGML 3.0 Utility Network ADE, several of these spatial properties are now automatically inherited and have, thus, been removed from the CityGML 3.0 Utility Network ADE. These spatial properties are: _lod0Point_, _lod0MultiSurface_, _lod2MultiSurface_, _lod3MultiSurface_, _lod1Solid_, _lod2Solid_, _lod3Solid_, _lod1ImplicitRepresentation_, _lod2ImplicitRepresentation_, and _lod3ImplicitRepresentation_.

Since the class _AbstractNetworkFeature_ also inherits some geometries that are not intended for the ADE, an OCL contraint was defined that prohibits the use of these geometries. These geometries are _lod0MultiCurve_, _lod2MultiCurve_, _lod3MultiCurve_, _lod1TerrainIntersectionCurve_, _lod2TerrainIntersectionCurve_,  and _lod3TerrainIntersectionCurve_.

The other spatial properties that have been defined in the CityGML 2.0 Utility Network ADE are also included in the CityGML 3.0 Utility Network ADE, which are _lod0Curve_, _lod2SweepGeometry_, and _lod3SweepGeometry_.

## ADE properties

The CityGML Utility Network ADE also adds properties (attributes and associations) to predefined CityGML feature types.

Using CityGML 2.0, a new ADE feature type had to be defined as subclass of the predefined CityGML class and the properties had to be added to this subclass.

CityGML 3.0 provides a more convenient solution for adding properties to CityGML feature types. Each CityGML feature type defines a specific attribute with the name _adeOfFeatureTypeName_ and type _ADEOfFeatureTypeName_ (the suffix _FeatureTypeName_ being a placeholder for the class name in which the attribute is defined). In the ADE, a subclass is defined for the type _ADEOfFeatureTypeName_ and the ADE properties are defined as attributes of this new subclass.

Regarding the CityGML Utility Network ADE, this affects the properties _mediumSupply_ and _roleInNetwork_ which are defined as additional properties of the CityGML feature type _AbstractCityObject_. As described above, _AbstractCityObject_ contains now an attribute _adeOfAbstractCityObject_ of type _ADEOfAbstractCityObject_ in CityGML 3.0. Thus, in the CityGML 3.0 Utility Network ADE, a new class _CityObjectMediumSupply_ is defined as subclass of _ADEOfAbstractCityObject_ which defines the properties _mediumSupply_ and _roleInNetwork_.

In the CityGML 2.0 Utility Network ADE, _occupancy_ was defined as another ADE property for the class _AbstractBuilding_. Since CityGML 3.0 already defines an identical property as part of the class _AbstractConstruction_ from which the class _AbstractBuilding_ is a subclass of, the property was not included in the CityGML 3.0 Utility Network ADE and also the classes _Occupancy_, _IntervalValue_, and _OccupantTypeValue_ are no longer required.

## Further information on CityGML 3.0

Please refer to the following publications for more details on CityGML 3.0:
- OGC City Geography Markup Language (CityGML) Part 1: Conceptual Model Standard: https://docs.ogc.org/is/20-010/20-010.html
- Kutzner, T., Chaturvedi, K. & Kolbe, T. H., 2020: New Functions Open Up New Applications. PFG 88, 43–61: https://doi.org/10.1007/s41064-020-00095-z
