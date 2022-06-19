###### File Structure ######

UseCasesAndDiagrams.pdf      -   contains use case model and diagrams
ClassDiagram.jpg                      -    Duplicate of class diagram in UseCasesAndDiagrams.pdf

/ProjectCode       -   Contains the following source files:
“History of Treatment” Folder	// This folder contains the text file that records sessions
Previous Session.txt 	
“Icons” folder		// This folder contains all the .svg and .png files used in the GUI
20min.svg
45min.svg
100hz.svg
Alpha.svg
Beta 1.svg
Beta 2.svg
customMin.svg
Delta.svg
Excellentconnection.svg
Fortyfivemin.svg
ic_decrease_intensity.svg
Ic_increase_intensity.svg
Ic_power.svg
Met.svg
Nobars.png
Noconnection.png
Okayconnection.png
Onebar.png
Sub-Delta.svg
Theta.svg
twentymin.svg
device.h			// header file for the device class
electode.h			// header file for electrode class
main.h				// header file for main class
mainwindow.h			// header file for mainwindow class
session.h			// header file for session
session.cpp			// Class file for session
mainwindow.cpp		// Class file for mainwindow
main.cpp			// Class file for main 
electrode.cpp			// Class file for electrode
device.cpp			// Class file for device
GroupProject 			// Shared Library
GroupProject.pro		// The .pro file for this QT Creator Project
GroupProject.pro.user	// The .pro.user file for this QT Creator Project
Previous Session.txt 		// Stores previous sessions that are recorded
Proj.qrc 			// The .qrc file for this QT Creator Project


###### Tested Scenarios ######
All Use Cases (from UC1 to UC6) work and all the simulation requirements work as well according to the
features of Oasis Pro that were required in the Team Project Specification document All the requirements
 as listed in the Traceability matrix have also been implemented.

Instructions:

UC1: Using the OasisPro device for a therapy session
- Turn on the device by pressing the power button
- Before the AFK timer (located above the power button) reaches 120 seconds, select your session length
  and session type from their respective dropdown lists (located on the left side of the UI).
- Adjust the intensity as you wish, this will provide the initial connection state (1-3 good, 4-6 okay,
  7-8 no connection)
- Once you have chosen your session length and session type, press the "Select Session" button located
  beneath the two dropdown lists.
- The connection test will be displayed (located in the bottom middle of the UI) 
- Once the session has started, the inactivity timer will stop and you can adjust the intensity mid
- session if you wish. The starting intensity will be the last saved intensity, if none was found it will
  default to 1. 
- You can either stop the session early by pressing the power button or wait the full length of the
  session for it to automatically terminate.
- If the session is not terminated early, once it finishes the device will power off

If a “user designated session” when choosing your session length, the QPlainTextField below it will be
changed from disabled to enabled and allowing you to input your custom integer session length. During
the middle of a session, you can press the “record session” button to have a backup made of that session.
You can also press the “previous session” button to view all previous sessions (if they exist). Session
connection status is determined by the intensity when starting the session and when reconnection. When
starting a session the resulting  intensities will be: 1-3 “Good connection”, 4-6 “Okay Connection”, 7-8
“No connection”. When reconnecting disconnected earclips an intensity of between 1-4 will result in “Good
connection” and 5-8 in “Okay connection”. 

***IMPORTANT NOTE*** All widgets on the UI are disabled except for the power button on start up, they
will be enabled as the simulation progresses and the majority will be enabled once the power is turned
on. 

