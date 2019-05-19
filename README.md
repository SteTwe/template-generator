# Template-generator
## Overview
A program that can generate new files with user input, based on predefined templates.

## Dependencies
* python >= 3.5
* pickle
* pathlib
* re
* sys
* os

## Installation
Currently only manual installation available.
```
git clone https://github.com/SteTwe/template-generator.git
  OR
git clone https://gitlab.com/SteTwe/template-generator.git
```
Move `/src/py/template-generator` to a folder that has been added to path.

Create config file that contains your templates. See Configuration down below.

## Usage
```
$ template-generator -l                           # List all templates, with possible arguments.
$ template-generator -u                           # Update database, based on config file.
$ template-generator -g <template> <arguments>    # Generate template with given arguments.

$ template-generator -h                           # Display help message.
$ template-generator -v                           # Display version.

```

## Configuration
Program has to be modified a lot according to your own configuration, a lot is still hard coded. This will be changed in the future.
Default config location is `~/.config/template-generator/config`.
```
[template_name1]
argument1
argument2
argument3
end
[template_name2]
argument1
argument2
```

Default template location is `~/templates/`. Arguments should be marked in the template, `*ARGUMENT`.


## Examples
### LaTeX
`$ template-generator -g latex Example SteTwe "Demonstration of template-generator" "$(date '+%d %B %Y')"`
![LaTeX](https://github.com/SteTwe/template-generator/blob/master/examples/latex/latex.png)

`$ template-generator -g notes "Stef Tweepenninckx" "Lesson 15: notes" `
![notes](https://github.com/SteTwe/template-generator/blob/master/examples/notes/notes.png)

Full examples available in `/examples/`
