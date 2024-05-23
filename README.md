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
## <u>TRADITIONAL PROGRAMMER :</u> ### Hey Mr., that's it.... take it...
## <u>SOMEONE :</u> Okay, Fine. what you will do if I need to sum of series with distance. For example, distance = 2 (1 + 3 + 5 = 9).  
## <u>TRADITIONAL PROGRAMMER :</u> Hey,  just change the step value from 1 to 2 in the 'range' function of the 'for' loop.
## <u>SOMEONE :</u> Okay, that's fine. If my start and stop value are too low, your running time of code will not be noticeable which means that we can't observe the time difference in seconds. <br/> Our modern day CPU's will handle easily. What you will do if I gave 1 as start and 1 lakh million as stop or 1000 lakh million as stop value. <br/> For 1 lakh million, my PC will take around 160 hours to compute. This is not a small amount of time. So, how you will approach???????


