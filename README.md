# GMXU

This repository contains the source code for a Command-Line Interface (CLI) that can be used along side GameMaker Studio 2 to automatically truncate project scripts, and manage and manipulate extension data. This is useful for large packages where it would be a waste of time to manually add help information for every script after every new build.

## Converting Project Scripts Into Standalone *.gml Files
```
Syntax:
compile <directory> [destination]

 <directory>
  The directory the scripts you want to compile are located in.
  
 [destination]
  An optional argument you can supply if you want to define an output path, otherwise the result will be output one directory above the supplied directory.
```
Perhaps you want to store all your useful scripts in an extension to keep your project nice and tidy, but you have too many to count and don't want to manually compile a *.gml file to import into an extension, this command has you covered.
```
Example:
compile C:\Users\User\Projects\Platformer\scripts C:\tmp\compiledProjectScripts.gml
```
This example command will compile all scripts located at the path "C:\Users\User\Projects\Platformer\scripts" and store the final file in the tmp directory with a file name of "compiledProjectScripts.gml"

## Updating Extension Help Information
```
Syntax:
amend <filepath>

 <filepath>
  The file path that of your *.yy extension file you want to update the help information for.
```
We all know how tedious it is to add help information manually when creating *.gml extensions, especially if you have to keep looking back at the parameter names in the source file. This command hopes to alleviate that burden.
```
Example:
amend C:\Users\User\Projects\ZombieGame\extensions\windowControl\windowControl.yy
```
This example command will update all help information in the supplied *.yy extension file per script, by referencing the source files for JSDoc argument information.