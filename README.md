CE3
===

07 MAR 14


#Truth Table 
![truth table](https://github.com/Austinbolinger/CE3/blob/master/StateTable.JPG?raw=true "Truth Table")
#Output Table
![output table](https://github.com/Austinbolinger/CE3/blob/master/outputTable.JPG?raw=true "Output Table")


Testbench output: Moore
![Moore Testbench](https://github.com/Austinbolinger/CE3/blob/master/Moore_testbench_result.JPG?raw=true "testbench") 

Testbench output: Mealy
![Mealy Testbench.Part1](https://github.com/Austinbolinger/CE3/blob/master/Mealy_testbench_result1.JPG?raw=true "testbench") 
![Mealy Testbench.Part1](https://github.com/Austinbolinger/CE3/blob/master/Mealy_testbench_result2.JPG?raw=true "testbench") 

#Links
MooreElevatorController
https://github.com/Austinbolinger/CE3/blob/master/MooreElevatorController_Shell.vhd

MeallyElevatorController
https://github.com/Austinbolinger/CE3/blob/master/MealyElevatorController_Shell.vhd

Moore testbench
https://github.com/Austinbolinger/CE3/blob/master/Moore_testbench_Bolinger.vhd

Mealy testbench
https://github.com/Austinbolinger/CE3/blob/master/Mealy_testbench_Bolinger.vhd


#Analysis
Moore: The testbench out put results that match the given expected results. Also by analysizing each clock cycle, you can tell that the elevator starts at floor 1, waits with input "stop", goes up a floor when inputs are "go up", then waits at floor 2 with "stop" again. It then repeats the process when given "go up" again. It does this until it reaches floor 4. Then the code asks it to go down without stopping given the input "go down". The clock cycles through enough to allow the elevator to return to floor 1.

Mealy: The testbench out put results include a next floor now. Looking at the testbench, you can see that with the same test bench code, the elevator preforms the same functions as far as going up a floor waiting and continuing up. But, this code also allows for a prediction. The next floor is half a clock cycle ahead of the current floor. Meaning, when on floor one, the next floor reads "floor 2" as long as the "go up" command is next. When the current floor is, say 2, and the input is "stop", the next floor reads the current floor, like 2. This seems to make sense that the testbench has the next floor  a cycle ahead of the current floor.`


###Questions
--Question: is reset synchronous or asynchronous? 
 The synchronous because the reset only gets looked at if the clk changes.
 --Question: Will it(next-state process)  be different from your Moore Machine?
 No.
 --Question: What is the clock frequency? 
 100Mhz
 --Question: What value would we set to simulate a 50MHz clock?
 20ns


####Test



#####Documentation
C3C Pluger and I talked on the phone as to how to get some of the parts to work like the nextState output code. We also discussed what exactly we were asked to turn in for the testbench.
