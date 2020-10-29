# FortniteTypeMappings

Fortnite Type-Mappings for [FModel](https://github.com/iAmAsval/FModel).

### Contributing

We have some basic guidelines before creating a [PR](https://github.com/FabianFG/FortniteTypeMappings/pulls):

- the JSON format should be prettified with a tab space of 2
    - you can use [jsonformatter.org](https://jsonformatter.org/) if your editor cannot do that

- the additional `F` or `U` at the beginning of a struct/class name should be removed
    - e.g. `FFortItemEntry` -> `FortItemEntry` / `UFortHelpPanel` -> `FortHelpPanel`

- EnumProperties should have the right `enumName` and their values added in the [EnumMappings](https://github.com/FabianFG/FortniteTypeMappings/blob/master/EnumMappings.json) file

- engine/core structs such as `FVector` should not be added as a key in the [TypeMappings](https://github.com/FabianFG/FortniteTypeMappings/blob/master/TypeMappings.json) file as they are parsed sequential.
    - if you are not sure if FModel already has support for them, you can check if its present in FModel's [UScriptStruct.cs](https://github.com/iAmAsval/FModel/blob/master/FModel/PakReader/Parsers/Objects/UScriptStruct.cs) file