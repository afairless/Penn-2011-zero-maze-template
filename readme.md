NoldusFreeInteractionScoring
Andrew Fairless, November 2009
This program was modified slightly from the July 2009 version.  Specifically, some of the information is not outputted back onto the spreadsheet, as this information is not necessary for current purposes.

Andrew Fairless, July 2009
This program takes Noldus data as input, totals its events, and re-arranges it for graphing into an event timeline.
This program was subsequently expanded to arrange the event totals into a single row for easy transferral to another spreadsheet that compiles all the data for a particular experiment.

More specifically, this data takes a Noldus data table as its input.
The Noldus data table lists the start and stop times of the events that were recorded in the Noldus Observer software.
The Noldus data table may also include who/what ("Subject") performed an action ("Behavior") in what way ("Behavior Modifier 1", "Behavior Modifier 2", etc.).  This program can classify and subclassify only 3 of these attributes (e.g., it can handle "Subject", "Behavior", and "Behavior Modifier 1", but not "Behavior Modifier 2").
NOTE:  If fewer than 3 of these attributes are present, the program code must be adjusted.  See NOTE below preceding "Column1Name = ".
The Noldus data table should be in chronological order (i.e., the event times should proceed from lowest to highest as one moves from the top to the bottom of the table.

This program hierarchically re-sorts the Noldus data table by the 3 attributes and places this re-arranged data to the right of the original data.

This program calculates the duration of each event and displays this information to the right of the re-sorted data (in the re-sorted sequence).
This program calculates the total durations and numbers of events for each attribute -- which is its own category -- and displays this information to the right of the event durations.
This program displays a final column to the right of the prior calculations.  This column is formatted so that the events can be graphed on a timeline (using a separate macro/program).

This program calls the functions "CountUniqueValues" and "ColumnIndexByName".

This program was expanded to do the following:  compile the latencies, number of times, and durations of the subcategories of the Column2 events (usually "Behavior") into a compact table displayed to the right of prior output; display a timeline of the "stimulussniffstest" and "testsniffsstimulus" (or any other two events as defined by the programmer) events to the right of prior output; calculate the duration of these two events without counting time when they overlapped twice; and re-arrange these data into a single row displayed above the original Noldus data table.
