Epsilon-ArgoUML Integration
===========

Eclipse plugins that extend Epsilon's Model Connectivity (EMC) layer with support for managing ArgoUML models (.zargo) using languages of the [Epsilon platform](http://www.eclipse.org/epsilon) to perform activities such as code generation, model validation and model-to-model transformation. The ArgoUML EMC driver supports both loading/querying and modifying/saving .zargo models.

Example
-----------
The following EOL snippet demonstrates iterating through all the classes in a .zargo model and printing their names and the names of their attributes.
```
for (c in Class.all) {
	c.name.println();
	for (a in c.feature.select(f|f.isTypeOf(Attribute))) {
		("-" + a.name).println();
	}
}
```

Update site
-----------
https://raw.githubusercontent.com/epsilonlabs/emc-argouml/master/org.eclipse.epsilon.argouml.updatesite/

**Important:** You will need to update to the latest interim version of Epsilon to use the ArgoUML driver.

Tips
-----------
To explore the exact version of the UML metamodel that ArgoUML models conform to, open Epsilon's EPackage Registry view, click the refresh button and look for the uml14 metamodel.
