Version 2.2
- Fixed the import from file function. It takes a .csv file and not a .dat file. Some checks are performed during file parsing. A progress bar has been added to display operation status. If File Dialog is closed by user, it was not handled.
- On different User Interfaces Panels: disabled all controls, everything must go through File. The only exception is that we can delete an existing DMA Block.
- Moved all operations performed at beginning (Initialization) of RT VI to an Action VI OnCompile. It's only faster but it is performed only at Sysdef Compilation (which only happens if there is a modification).
- Changed the way we parse Configuration at Compilation to improve performances.
- Changed how we store VISA Resource used from Binary String to String.
- For Main Page, for String Control, limit to single line.
- For Main Page, a Path indicator added to display the path of the CSV File used.

Version 2.3



