inSTREAM Version 6.0

Readme file revised 11 Jan 2013, SF Railsback

Version 6.0 of inSTREAM is a major update of version 3, also referred to as inSTREAM-SD. Versions 3 and 6.0 differ from other versions of inSTREAM in three major ways: (1) Some model actions, including habitat updates and fish habitat selection, growth, and survival operate at variable time steps that can be as short as an hour; (2) Differences in habitat and fish behavior between day and night are represented; and (3) Fish choose between two activities, feeding vs. hiding, in addition to selecting which cell to occupy for the selected activity.

Version 3 was documented in: 
Railsback, S. F., J. W. Hayes, and K. E. LaGory. 2006. Simulation analysis of within-day flow fluctuations on trout below Flaming Gorge Dam. Argonne National Laboratory, ANL/EVS/TM/06-01, Argonne, Illinois.
(also published as: Railsback, S. F., J. W. Hayes, and K. E. LaGory. 2006. Simulation analysis of within-day flow fluctuations on trout below Flaming Gorge Dam. EPRI, 1012855, Palo Alto, California.)

and in:
Railsback, S. F., B. C. Harvey, J. W. Hayse, and K. E. LaGory. 2005. Tests of theory for diel variation in salmonid feeding activity and habitat use. Ecology 86(4):947-959.
 
Version 6.0 differs from version 3 by including some characteristics of inSTREAM V. 5.0: (1) Habitat input is provided in a generic format typically generated in GIS, instead of using formats produced by a specific hydraulic model. (2) Multiple reaches can be simulated, with fish moving among reaches. (3) A few minor changes in fish actions made to reflect recent literature and modeling experience.

Software changes from version 3 to 6 include:

1) inSTREAM is now packaged with a graphical user interface for Windows users. This GUI supports assembly and checking of input sets, setup of simulation experiments, and automated sensitivity ("limiting factors") analysis.

2) The MinGW compiler is used to produce a Windows executable of the model. Hence, using inSTREAM no longer requires installation of Swarm on Windows computers. Installing the model either as a stand-alone executable or within the GUI requires only copying the necessary directories and files.

3) A new approach is used by the HabitatSpace class to identify cells within a specified distance (its method getNeighborsWithin: aRange). This method uses the KD-Tree data structure instead of simply calculating the distance to each cell, and should provide faster execution. 

4) Almost all input files (except Setup files) can now be in .CSV format, facilitating their preparation in Excel or other spreadsheet and statistical software. The EcoSwarm TimeSeriesInput manager was modified to read input files with values separated either by commas or white space.

5) The EcoSwarm BreakoutReporter that writes output files was modified to (a) produce output in .CSV format, and (b) write output in a format with fewer columns that is more convenient for analysis via Excel's "PivotTables" and statistical software.

6) Optional output is now controlled via (optional) parameters in the Model.Setup file instead of by code statements. Hence, optional output can be turned on and off without re-compiling the software.

Production of inSTREAM version 6.0 was funded by Argonne National Laboratory via their Contract No. 2F-32941 with Lang, Railsback & Associates. It was designed for analysis of effects of Flaming Gorge Dam power production operations on downstream trout fisheries in the Green River, Utah.

Many of the software improvements in inSTREAM 6.0 were originally made for the project "Improvement of Salmon Life-Cycle Framework Model (inSALMO)", Contract R09PS20027, conducted by Lang, Railsback & Associates and USDA Forest Service Redwood Sciences Lab, Arcata CA, for U. S. Bureau of Reclamation,  Mid-Pacific Regional Office. 

inSTREAM 6.0 was developed by Steven Railsback and Bret Harvey, and software development was by Colin Sheppard, Steve Jackson, and Charles Sharpsteen.


For information and assistance contact:
  Steve Railsback
	Lang, Railsback & Assoc.
	Arcata, CA, USA 95521
	info@LangRailsback.com

or:

  Kirk E. LaGory, Ph.D.
  Ecological Resources and Systems
	Environmental Science Division
	Argonne National Laboratory
	9700 S. Cass Ave., Building 240
	Argonne, Illinois 60439
	Office: 630-252-3169
	lagory@anl.gov

inSTREAM software and its documentation are copyright 2013 by Lang, Railsback & Associates, and distributed as free software under the GNU General Public License (see file LICENSE). 
