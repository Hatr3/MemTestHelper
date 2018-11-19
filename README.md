# MemTestHelper
AutoIT GUI to automate HCI MemTest

![Screenshot](https://github.com/integralfx/MemTestHelper/raw/master/memtest_helper.jpg)

## Usage
* Download my [modfied version](https://github.com/integralfx/MemTestHelper/raw/master/memtest_6.0_no_nag.exe) of HCI MemTest
* Download memtest_helper from [releases](https://github.com/integralfx/MemTestHelper/releases)
* Run memtest_helper

## Settings
### RAM to test
Exactly as its name implies. This number will be divided by the number of threads and then input in each HCI MemTest instance.
Clicking on it will automatically input the amount of free RAM your computer has.

### Number of threads
How many HCI MemTest instances to run and hence the amount of CPU threads to use.

### Number of rows
By default, MemTestHelper will use all of your CPU threads. Say your CPU has 8 threads, so there will be 8 HCI MemTest instances running. They will be centered on the primary monitor. Number of rows changes how those 8 instances are centered. If it's 2, it will put 4 instances on each row. It's best to play around with it to understand how it works.

### X/Y offset
By default, the 8 instances will be centered, but you can move them around using X and Y offset. Note that higher Y values will move the instances down.

### X/Y spacing
Spacing between each of the MemTest windows.

### Stop at
* #### Coverage %
  * Automatically stop each instance as they hit the coverage number entered in the textbox.
  * Checking "Total" will use the total coverage rather than each MemTest instance's coverage.
* #### Error count
  * Same as coverage % but with error count.

Checking both will stop if either of the above conditions are met.

### Update interval
How often to update the coverage and error info list. Lower values mean the list will be updated more often. Note that higher values might cause the GUI to become unresponsive. This is because AutoIT will [never support multi-threading](https://www.autoitscript.com/trac/autoit/wiki/AutoItNotOnToDoList)

## To-do
* Allow arbitrary number of rows
  * If number of rows doesn't divide evenly into number of threads
    * Center last row
    * Start last row where the previous row starts
* Layout grid to allow the user to choose how they want MemTest to be layed out
