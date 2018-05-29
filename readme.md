# gfm7

## Getting a copy of the code
Make sure you have Git installed on your local computer. Use the following command to download a copy of the git repository.
````
git clone https://github.com/jonlighthall/gfm7.git
````
Use Git to track changes in your local copy of the code and to receive updates.
## Compiling the code
The executable is compiled using the commands in the makefile. Run these commands using the command `make`.
The Fortran files used in compiling the executable are located in the [src](src) directory.
A working example of the Windows executable `gfm7.exe` is included for reference.
## Running the code
After the code has been compiled, run the program with the command `./gfm7`.
The program takes user input to provide the name of input file.
The extension of the filename must be included.
### Input
The following file is provided as an example input.
`27Al.dat`
### Output
The following output files are generated
 * `27Al.plt` Not used.
 * `27Al.grf` Graphical output: prints the z-value of a 2D histogram of the focal plane.
 * `27Al.mca` Five rows are output for each event: the x- and y-position of the particle in the focal plane in cm; the final partical energy in MeV; the final charge state; and the time-of-flight in ns.
 * `27Al.lis` Not used.

The output files will have the same base filename as the input file.

## Viewing the output
The macro `mca2root.C` has been included to convert a `.mca` file to a `.root` file populated with a TTree.
The macro expects a file name `output.mca`.
The file `ren.bat` has been included to rename the file.
The To run the macro, use the following command.
````
root -l mca2root.C
````
This will creat a ROOT file named `output.root` with a TTree named `t`.
