## Computed fields registry for pocketbase

This very minor abstraction exists for two purposes:

1. Computed fields all live in one place
2. Additional fields can be tied into typescript generation (package github.com/davenh99/pb-typescript)

Example of adding computed fields to typescript output:

```
gentypes.Register(app, gentypes.Config{
    FilePath:                   "ui",
    CollectionAdditionalFields: c.ComputedFieldsCfg.ExtractFields(),
    PrintSelectOptions:         true,
})
```
