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
## SOMEONE :loudspeaker: : <h3> Okay, that's fine. If my start and stop value are too low, your running time of code will not be noticeable which means that we can't observe the time difference in seconds. Our modern day CPU's will handle easily. What you will do if I gave 1 as start and 1 lakh million as stop or 1000 lakh million as stop value. For 1 lakh million, my PC will take around 160 hours to compute. This is not a small amount of time. So, how you will approach :grey_question: Here I've attached the proof for running time of the above input</h3>
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/9844b3ac-06b2-4720-8979-db7fd590206a)




