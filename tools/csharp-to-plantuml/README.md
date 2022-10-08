# csharp-to-plantuml README

Create class diagrams of PlantUML from C# source code.

Fork from [DrPepperBianco](https://github.com/DrPepperBianco/PlantUmlClassDiagramGenerator) and [pierre3](https://github.com/pierre3/PlantUmlClassDiagramGenerator). \

This version allow ignore some types in accessibility mode (include class fields of non-basic types as relations to these classes). *Useful for generic collections & Unity types (avoiding creating a lot of relations to this types).*

## Requirements

- .NET Core SDK 2.1 or newer.
- [.NET Core 3.1 Runtime](https://dotnet.microsoft.com/download/dotnet-core/3.1/runtime) 

## Extension Settings

- __csharp2plantuml.inputPath__  
  Specify a input folder (relative to workspace folder)
- __csharp2plantuml.outputPath__  
  Specify a output folder (relative to workspace folder)
- __csharp2plantuml.public__  
  Only public accessibility members are output.
- __csharp2plantuml.ignoreAccessibility__    
  Specify accessibiliies of members to ignore, with a comma separated list. (ex. 'private,protected,protected internal')
- __csharp2plantuml.excludePath__  
  Specify exclude file or directory paths (relative to the \"InputPath\"), with a comma separated list. (ex. 'obj,Properties\\AssemblyInfo.cs')
- __csharp2plantuml.createAssociation__  
  Create object associations from references of fields and properites.
- __csharp2plantuml.allInOne__  
  Copy the output of all diagrams to file include.puml (this allows a PlanUMLServer to render it).
- __csharp2plantuml.ignoreAccessibilityTypes__  
  List of types that will be ignored to create relation in accessibility mode. Separate with ';'.
- __csharp2plantuml.ignoreAccessibilityTypesStartWith__  
  List of types that start with this words that will be ignored to create relation in accessibility. Separate with ';' .\
  **Default value**: *"List<, Dictionary<, SortedList<, Queue< , Stack<, Hashset<"*

## Known Issues


## Release Notes
### 1.2.5
- Updated to .NET6.0
- Added config options to ignore specific members types to don't create as relation field in accessibility mode (specially for collections in C#)

### 1.2.4
- Updated to .NET5.0

### 1.2.3
- Fixed Issue: 
    - https://github.com/pierre3/PlantUmlClassDiagramGenerator/issues/34

### 1.2.2
- Updated to .Net Core 3.1.
- Fixed Issue: 
    - https://github.com/pierre3/PlantUmlClassDiagramGenerator/issues/32
    - https://github.com/pierre3/PlantUmlClassDiagramGenerator/issues/26

### 1.2.1  
- Updated to .Net Core 3.0.
- Add Feature that allows for Nullable (?) type syntax.
- Add all-in-one option.

### 1.0.0
Add Feature that create object associations from references of fields and properties. 

### 0.0.1 preview
Beta release.
