******# Stan
- has its own structure and syntax
- interface for R python 
- very well documented [[mc-stan.org]]
# Stan Installation 
- we use rstan 
- need to have the C++ toolchain
- C++ toolchain configuration 
	- many R packages needs to be compiled 
	- stan dynamically generates C++ so you need to compile the code 
	- follow the guide on slides to install rtools 
# Stan Basic Syntax 
a stan model is defined by .stan file 
- is a strongly typed language (have to be specific about types)
- note the ending ; on each line you nee to have those 
- indentation doesn't matter 