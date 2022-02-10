### Changes to the initial upload

In addition to the modifications that have been applied to update the ADE to CityGML 3.0 and which are described in ["Updating the Utility Network ADE to comply with CityGML 3.0"](Updating-to-CityGML3.0.md), further changes have been applied to the UML model.

* Class "AbstractNetworkFeature":
  * The class contains the spatial properties lod2SweepGeometry and lod3SweepGeometry which were modelled with multiplicity [0..1]. This means that a network feature can only be represented by one Curve and one Polyon, making it impossible to model an Y-connector. Thus, the multiplicity was changed to [*].

* Class "SimpleFunctionalElement":
  * This class was modelled as abstract class, but was missing the prefix "Abstract". Thus, the class was renamed to "AbstractSimpleFunctionalElement".
