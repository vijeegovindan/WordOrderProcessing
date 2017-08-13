# WordOrderProcessing

For this activity one process will be creating work orders and writing them to disk. Another process will read the work orders and then process them.

The work order process is to first put the work order in the INITIAL pile. It next moves to the ASSIGNED pile (think of this as when the work order is assigned to someone). Next it moves to the IN_PROGRESS pile (when the person it was assigned to actually starts working on it.). And lastly it moves to the DONE pile (when the work is done).

Getting Started  

Open up a new project in IntelliJ.

Import the jackson library to convert java to/from JSON.

Create a Status enum with the following values

INITIAL
ASSIGNED
IN_PROGRESS
DONE
Create a WorkOrder class with the following fields

id (int)
description (String)
senderName (String)
status (Status)
Create a class named "Creator" to create work orders  

In Creator have a public static void main that creates an instance of Creator and calls the instance method that loops to get the user input and create work order files.

The processWorkOrders method should

Run forever in a loop. Have the loop sleep for a five seconds (or longer).
Have a map with Status as the key and a Set of work orders for the value
print out the map
move work orders from one map entry to the next (i.e., From IN_PROGRESS to DONE; from ASSIGNED TO IN_PROGRESS; from INITIAL to ASSIGNED). A work order should only transitioned once per loop.
print out the map
Check for new work orders (files). For each new work order
reads the file into a WorkOrder object
removes the file
print out the work order
puts the work order in the INITIAL map entry.
Here's the code to sleep for 5 seconds (5000 miliseconds)
