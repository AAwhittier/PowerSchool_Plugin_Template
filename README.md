# PowerSchool_Plugin_Template
This is a template for a plugin to create named power queries and expose them for access on the Power School SIS API.

# Structure
The plugin follows reverse domain namespace rules for named queries.
- `com.<domain>.<area>.<action>.<variant>`
- This will be the endpoint name for the API.

Arguments are supported by the API and are useful for filtering the data returned by the query.
- Declare the argument inside of an `<args>` tag.
```
<arg name="paramName"
    description="Description of the parameter and expected format."
        type="primitive"
        required="true" />
```

- Reference the argument with `:paramName` in the query.


## Building The Plugin
To package the plugin place it in a zipped folder ensuring `plugin.xml` is at the root level.
