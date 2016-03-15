############################################################################
###     BandUP: Band Unfolding code for Plane-wave based calculations             
############################################################################
###### Copyright (C) 2013-2016 Paulo V. C. Medeiros - pvm20@cam.ac.uk
##### Please visit http://www.ifm.liu.se/theomod/compphys/band-unfolding

BandUP is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

BandUP is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with BandUP.  If not, see <http://www.gnu.org/licenses/>.

<!-- ============================================================================= -->
#### Plane-wave codes currently supported by BandUP
--------------------------------------------------------------------------------------
    * At the moment, BandUP can parse wavefunctions generated by: 
        * VASP
        * Quantum ESPRESSO
        * ABINIT
    * Feel free to contact me if you use another plane-wave code and would like to have 
      support to it added in BandUP
        * As usual, I'll do my best to help you out.
        * Of course, you can also collaborate by writing/sending me a routine to read 
          the wavefunctions produced by your code. If you already have a routine, then
          we'd only need to write an interface to it :)

<!-- ============================================================================= -->
#### How to compile BandUP
--------------------------------------------------------------------------------------
    * Run the "build.sh" script: ./build.sh
    * A directory named "BandUP_bin" will be created.
        * You'll find the executable for BandUP in it.
    * This should work in most Unix environments with up-to-date Intel or GNU compilers 
      installed. 
        * Do check, however, the system requirements below if you have any problem.

<!-- ============================================================================= -->
#### System requirements:
--------------------------------------------------------------------------------------
    * Preferably Linux
        * Might work in other environments based on Unix
    * Fortran 95 and C compilers
        * Preferably Intel compilers (ifort and icc), version 12.1.4 (or higher)
        * Should also work with GNU compilers (gfortran and gcc), version 5.2 (or higher)
    * Python 2.7 (or higher) for the post-processing utilities
        * You will need to have the following packages installed 
          (you probably already have most of them):
            * numpy 
            * scipy
            * matplotlib
        * Please let me know if I've forgotten to list any other package!
    * Optional: PyQt4
            * PyQt4 is needed only if you want to use the graphical user interface 
              (GUI) version of the plotting tool.
            * If the GUI doesn't work with you, you can keep using the plotting tool 
              in the command line, just as usual.
            
<!-- ============================================================================= -->
#### Publications:
--------------------------------------------------------------------------------------
    * If you use BandUP (or any part or modified version of it) in your work, you should:
          * State EXPLICITLY that you've used the BandUP code (or a modified version of it).
          * Read and cite the following papers (and the appropriate references therein):

            >>> Phys. Rev. B 89, 041407(R) (2014) <http://dx.doi.org/10.1103/PhysRevB.89.041407>

            >>> Phys. Rev. B 91, 041116(R) (2015) <http://dx.doi.org/10.1103/PhysRevB.91.041116>

      * An appropriate way of acknowledging the use of BandUP in your publications would be, 
        for instance, adding a sentence like 
                "The unfolding has been performed using the BandUP code",
        followed by the citation to our papers.


<!-- ============================================================================= -->
#### Tips:
--------------------------------------------------------------------------------------
    * BandUP accepts some optional command line arguments and flags. To find out more
      about them, run the code with the flag '-help'.
    * Since the plotting tool has a lot of different options, I've given it a GUI:
          utils/post_unfolding/plot/plotting_tool_GUI/BandUP_plot_GUI.pyw
      You'll find a symlink to it (bandup_plot) in the BandUP_bin directory.
      * The GUI requires that you have PyQt4 in you python install.
      * If you move the BandUP_plot_GUI.pyw file, move the BandUP_plot_GUI.ui too.
    * It might be handy to include the directory BandUP_bin in your PATH. By doing so,
      you'll be able to use BandUP in whataver directory you're working at.


<!-- ============================================================================= -->
#### Please mind that:
--------------------------------------------------------------------------------------
    * Although I've tried to make the compilation as simple as possible - and it has 
      indeed worked fine so far with many combinations of compilers, computers, and 
      operating systems, I cannot guarantee that it will always work smoothly. 
      You might eventually need to play a bit with the scripts and, very rarely, 
      with the Makefiles and source code.
    * In the calculations and tests I've performed with BandUP so far, I've mostly 
      used intel compilers (v. 12.1.4) and, a few times, GNU compilers (v. 5.2). 
      I *believe* that you should have no problems using other versions of ifort/icc 
      (and *maybe* even other non-intel compilers), as well as more recent versions 
      of gfortran/gcc. Mind, however, that I cannot guarantee that it will work in 
      100% of the cases.
    * Of course, I'll try my best to help you out in case you do have problems.
      Before writing to me asking for support, however, do make sure that (i) you are 
      using the latest version of BandUP, and (ii) your system complies with what is 
      described in the "system requirements" section of this file. 
    * Last, but not least: Always check the results with a critical eye, specially 
      if they don't look the way you think they are supposed to. Please notify me if 
      weird stuff happens and you think it's the code's fault (but do double-check first)!
 

Have fun! 
Let us know if you have problems! 
