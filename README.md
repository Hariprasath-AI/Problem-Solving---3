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
## ME :loudspeaker: : 
<h3>Okay, I'll optimize it..</h3><br/>

# My Approach (Logical Thinking by Incorporating Mathematical Knowledge):

## 1) Static start and dynamic stop:

For Instance, taking Example 1. Initially 1 is there, next I've to add 2 with existing 1. Then 3 with existing sum (1 + 2 = 3). And goes on... And finally, we got 15 (1 + 2 + 3 + 4 + 5). 
How should I produce mathematicaaly proven formula for this problem. My ultimate target is to get the output/result in milliseconds or less than that for any input (start and stop).

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/eeaf48bc-fa51-4825-881d-bbbc4fc7c0e1)
The above sheet shows how the traditional approach will return the result after each iteration.

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/f03e89df-cf57-4c9c-bddd-76b46315208b)
In the above sheet I just placed 1's in every cell with 'n' columns and 'n' rows. Whereas, 'n' is the stop and start as 1. <br/>
NOTE :pencil2: : There is no relation between the 1's placement and start. For understanding purpose I put 1's in each 'n' columns. So, don't confuse. <br/>
At 1st iteration what I need is 1, 2nd is 2, and 3rd is 3 right!. So, I just marked how many ones I need at each iteration. Please consider index of the sheet as iteration. <br/>
After marking, how many ones I need at each iteration from 'n' ones. Look at the latest sheet, and if we sum all the marked ones (1's), we'll get the desired output.<br/>
NOTE :pencil2: : Just count number of ones (1's). You'll get N ** 2 value which is 25 (5 ** 2). <br/>
No change, we're just marking diagonal 1's in different color and we'll see it....

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/ca62e0b5-ea4e-42ce-b9bf-7475d1d63f4b)
NOTE :pencil2: : There will be a diagonal for all values. Let's check with even stop as 4 and with same start of 1.

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/b09021b7-7ee3-4afa-8fab-b247956feb00)
This is how it will look for stop value of 4 and start of 1. 

We know that, there will be diagonal for all 'n' values(stop). 
So, just seperate the upper and lower part of the diagonal in the above sheet. <br/>
NOTE :pencil2: : The 'white' colored 1's belongs to the upper part and 'green' colored 1's belongs to the lower part. <br/>
After seperation, just look at the sheet what values we want. Simple, we need diagonal part and lower part. Am I right!!! <br/>
NOTE :pencil2: : The sum of upper 1's and lower 1's will always same. Don't ask me why?.. That's math :laughing: <br/>
We need diagonal and lower part right!!! What actually diagonal mean....
NOTE :pencil2: : Start and stop value considered from example 1. 
1) Sum of diagonal is nothing but the stop or 'n'.
2) To get lower part and upper part, we've to reduce stop value from total 1's which is the square of stop. ((stop ** 2) - stop ---> ((5 ** 2) - 5) ---> (25 - 5) ---> 20).
3) 20 is the total 1's excluding diagonal. Lower part is nothing but the half of square of stop excluding diagonal which is half of 20.
   So, just simply divide it by 2. you'll get sum of lower part 1's (20/2 = 10).
5) Finally, add it with stop (n). 10(lower part) + 5(stop) = 15.
6) Hurray, we got it... :sparkles: :star:

### Discovered Formula : ((((max ** 2) - max) / 2) + max)
NOTE :pencil2: : max is nothing but the stop value

We've to prove with time consumption. So, look at the upcoming image...
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/f7e0e954-2d5f-4e62-81b0-41251ac71e2a)
NOTE :pencil2: : datetime module is used to compute the running time. Here, the format is Hour:Minute:Second.Microsecond. <br/>
0 difference, the time in microsecond which is lesser than millisecond. <br/> 
NOTE :pencil2: : 1 second = 1000 millisecond, 1 millisecond = 1000 microsecond, 1 microsecond = 1000 nanosecond). <br/>
Not even 1 microsecond. Just think about the time taken in traditional approach which took around 70 hours(approx).  

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/1f8ec94b-8fff-4eba-bc4d-78fa851a8ce0)
I just pasted the input value of stop 2 times which is ~ square of previous stop value. Just look at the time difference ---> 0 microsecond. May be it took few nanoseconds :laughing:. 
Here, the mathematical approach is insane. :sunglasses:

## 2) Moving to the next phase of the approach (Dynamic start and dynamic stop):

The approach above is for static start and dynamic stop value. Just think about it, what we have to do in the case of dynamic start and dynamic stop. 
The constraint are same the start and stop should be greater than zero and stop should be greater than start value.
For instance (example 1), start = 3 and stop = 7. I need sum of series/sequence which is 3 + 4 + 5 + 6 + 7 = 25. 

We're not going to think too much. Just considering 1 as temporary start which is nothing but the minimum possible start according to constraint. Just look at the below image.
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/a9281c13-c661-4652-868d-87b634ec62c6)

The sheet show what we want to consider to get the desired sum of series. 
NOTE :pencil2: : 1 is the temporary start.
We know that start is 3, we have to consider from the index 3 of the above mentioned sheet to get desired output, right!!!. Ok, check the below image.
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/52f26e27-403e-4f03-9ad6-40eff04bb4fd)

I just marked the desired sum that we want in red colored grid lines. Now you'll understand what I mean.
Then we can mark the sum that we don't want also right!!!! which is the 1's of rest of the red grid lines. ok, I'll mark it in blue line. Look at the below image.
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/2f879831-94e7-4a86-8032-76e12d70c05a)

Now, we observed that the desired sum of series(dynamic start/stop) is within the static start & dynamic stop, right! 
ok, what will the output for start = 1 and stop = 7. It will be the sum of 1's present in the red and blue grid lines. 
And we know that the formula for static start(1st approach). We just want to exclude the rest 1's. 
So, we need to modify the formula of 1st approach to get formula for this approach.

NOTE :pencil2: : max is nothing but the stop value and min is the start value.

###RULE :
1) First, we need to sum the series from static 1 to dynamic stop value.
2) After that we need calculate the sum of 1's that we want to exclude.
3) If we reduce the sum value of '2)' from '1)', we'll get desired output.

###The formula for above rule:
1) ((((max ** 2) - max) / 2) + max), same formula that we discovered from 1st approach.
2) Here, we need to replace 'max' with (min - 1) ---> (((((min - 1) ** 2) - (min - 1)) / 2) + (min - 1))
3) Just reducing 2) from 1) ---> ((((max ** 2) - max) / 2) + max) - (((((min - 1) ** 2) - (min - 1)) / 2) + (min - 1))

### Discovered Formula : ((((max ** 2) - max) / 2) + max) - (((((min - 1) ** 2) - (min - 1)) / 2) + (min - 1))

Yeah, it's time to find out the time complexity for worst case. Considering min = 100, max = 100000000000000.
First, we will check this input with traditional approach.....

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/08ab07de-360d-489c-b7eb-7de745a292a8)
Around 7000 hours in the traditional approach. How it will be in mathematical approach? Let's check it...

![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/1fa32a24-0394-442e-8241-8d24dde273e3)
Uffff..... Again 0 microsecond which means less than a microsecond. The difference is very huge, from 7000 hours to less than a microsecond(may be few nanoseconds) which is insane.

## 3) Moving to the next phase of the approach (Dynamic start, dynamic stop and dynamic step):

What we do if I need sum of series with desired interval.
For example, min = 3, max = 7 and interval = 2 ---->  3 + 5 + 7 = 15
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/0619b730-4c42-4af6-83db-be305d50ea11)

The sum that we want is shaded in green color in the above sheet.
Here, the approach is slightly different from what we did in the last two approach.
We're going to remove rest of the rows which unshaded and looking at the sheet.
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/85687206-1281-4f7a-8bb0-98616df7239b)

### NOTE :pencil2: : The number of rows and columns will be different for interval > 1 for 1's placement table. Here the interval is 2. 
### Simply we can't reduce the unshaded part from total sum(min = 1, max = 7). Because, the shaded one is followed by unshaded with particular frequency.
