# Problem-Solving---3

# Description :
My Problem is to solve sum of series of numbers. 
# Input Constraints :
Given inputs are, start and stop. <br/>
The start is an any value greater than zero and stop must be greater than start. <br/>
# Example 1 -> Input :
start = 1, stop = 5 <br/>
# Example 1 -> output :
15<br/>
# Example 1 -> Explanation :
1 +..+..+ 5 -> 1 + 2 + 3 + 4 + 5 = 15 <br/>
This is what we need.. <br/>
# Traditional Programmer's Approach (Python Code) : 
start_input, stop_input = int(input()), int(input()) <br/>
count = 0 <br/>
for i in range(start_input, stop_input + 1): <br/>
&nbsp;&nbsp;&nbsp;&nbsp;count += i <br/>
print(count) <br/>
## TRADITIONAL PROGRAMMER :loudspeaker: : <h3> Hey Mr..., that's it.... take it... :smirk: </h3>
## SOMEONE :loudspeaker: : <h3>Okay, fine :smiley:. What you will do if I need to sum the series with distance:grey_question::exclamation: <br/>For example, distance = 2 (1 + 3 + 5 = 9). </h3>
## TRADITIONAL PROGRAMMER :loudspeaker: : <h3> Hey,  just change the step value from 1 to 2 in the 'range' function of the 'for' loop. </h3>
## SOMEONE :loudspeaker: : <h3> Okay, that's fine. If my start and stop value are too low, your running time of code will not be noticeable which means that we can't observe the time difference in seconds. Our modern day CPU's will handle easily. What you will do if I gave 1 as start and 1 lakh million as stop or 1000 lakh million as stop value. For 1 lakh million, my PC will take around 70 hours to compute. This is not a small amount of time. So, how you will approach :grey_question: Here, I've attached the proof for running time of input - 1 lakh million</h3>
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/9844b3ac-06b2-4720-8979-db7fd590206a)
## TRADITIONAL PROGRAMMER :loudspeaker: : <h3>what :grey_question::exclamation::disappointed:</h3>

# My Approach (Logical Thinking by incorporating Mathematical Knowledge):

For Instance, taking Example 1. Initially 1 is there, next I've to add 2 with existing 1. Then 3 with existing sum (1 + 2 = 3). And goes on... And finally, we got 15 (1 + 2 + 3 + 4 + 5). 
How should I produce mathematicaaly proven formula for this problem. My ultimate target is to get the output/result in milliseconds or less than that for any input (start and stop).

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/eeaf48bc-fa51-4825-881d-bbbc4fc7c0e1)
The above sheet shows how the traditional approach will return the result after each iteration.

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/f03e89df-cf57-4c9c-bddd-76b46315208b)
In the above sheet I just placed 1's in every cell with 'n' columns and 'n' rows. Whereas, 'n' is the stop and start as 1. <br/>
NOTE : There is no relation between the 1's placement and start. For understanding purpose I put 1's in each each. So, don't confuse. <br/>
At 1st iteration what I need is 1, 2nd is 2, and 3rd is 3 right!. So, I just marked how many ones I need at each iteration. Please consider index of the sheet as iteration. <br/>
After marking how many ones I need at each iteration from 'n' ones. Look at latest sheet, and if we sum all marked ones (1's), we'll get the desired output.<br/>
Just count number of ones (1's). You'll get N ** 2 value which is 25 (5 ** 2).<br/>





