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

# 1) Static start and dynamic stop:

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

## Discovered Formula : ((((max ** 2) - max) / 2) + max)
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

# 2) Moving to the next phase of the approach (Dynamic start and dynamic stop):

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

### RULE :
1) First, we need to sum the series from static 1 to dynamic stop value.
2) After that we need calculate the sum of 1's that we want to exclude.
3) If we reduce the sum value of '2)' from '1)', we'll get desired output.

### The formula for above rule:
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

# 3) Moving to the next phase of the approach (Dynamic start, dynamic stop and dynamic interval):

What we do if I need sum of series with desired interval.
For example, min = 3, max = 7 and interval = 2 ---->  3 + 5 + 7 = 15
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/0619b730-4c42-4af6-83db-be305d50ea11)

The sum that we want is shaded in green color in the above sheet.
Here, the approach is slightly different from what we did in the last two approach.
We're going to remove rest of the rows which unshaded and looking at the sheet.
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/85687206-1281-4f7a-8bb0-98616df7239b)

### NOTE :pencil2: : The number of rows and columns will be different for interval > 1 for 1's placement table. Here the interval is 2. 
Simply we can't reduce the unshaded part from total sum(min = 1, max = 7). Because, the shaded one is followed by unshaded with particular frequency.
So, we need look at the 1's placement table closely after removing unshaded rows. The table is given below...
![image](https://github.com/Hariprasath-AI/Problem-Solving---3/assets/74598275/d8d7af07-be68-42d1-9fe6-f371a803c310)

First, we have to know the count of possible numbers in the particular range(Here, row count). Here, 3, 5 and 7 are the possible values taken into account for summation.
Dividing the difference of min and max with interval will gives us the count of possible values for summation (Considering only whole number for division.. so, floor division is used).  
After that, we need to consider the initial value also which is min --> 3, So, 1 will be added to the count that we calculated in the previous line.  
Then, the formula will be, row count = (((max-min) // interval) + 1)
Let's check... Here, row_count = (((7 - 3) // 2 ) + 1) = (4 // 2) + 1 = 2 + 1 = 3.

For column count, 
1) We know that min number of columns possible for any input is given minimum. Here, for sure there will 3 columns, no doubt in that.. (NOTE:pencil2:: Anyhow min will be taken into summation for any input)<br/>
2) Right now we know the minimum possible sum is 'min'. To know the maximum value in the series, first we've to calculate 1st possible number after initial.<br/>
   Which is nothing but 'min' + interval. So generally this is the 2nd possible number in the series. Here, min is 3, max is 7 and interval is 2. so 2nd possible is 3 + 2 = 5.<br/>
   After calculating 2nd possible value in the series, we can easily find out the maximum possible value of the series.<br/>
3) Right now, we know the 1st number and 2nd number of the series. It will be increasing right. <br/>
   I'm writing like this, --> min + (min + interval) + ..... + (previous value + interval) <br/>
   Next, we have to know the bias value. You can ask, what actually the 'bias' is!!! Bias is the excluded value from each number in the series. Just look at the calculation below,
   Considering the same input values for min, max and interval.
   1st value in the series ---> 3  (We already know this value will be considered for summation. So, nothing to do in this stage) <br/>
   2nd value in the series ---> 5  <br/>
   From 2nd possible value, we have to know what actually the value is(Here, 5)! How many intervals are there in the number 5. (5 // 2 = 2) 2 right!!!, <br/>
   Ok, we know 2 intervals are there in the 2nd possible. So, just multiplying interval with no. of interval which is 2 are,2 * 2 = 4. <br/>
   But, the 2nd possible number is 5, right. Here, we got 4. Then where is that 1 and what it mean. Simple, that's bias. (NOTE:pencil2::Here I'm calling it as bias value)
   So, (Number of interval * interval) + bias gives us the desired value of the series.
4) After calculating the bias, we have to know the how many intervals that the number holds which is count of intervals for 2nd possible number (5 // 2 = 2).
5) Then, add that number of intervals of 2nd number with row count excluding 1st number and 2nd number --> no of intervals(2nd) + (row count - 2) = (2nd number // interval) +((((max-min) // interval) + 1) - 2 ) = (2nd number // interval) + (((max-min) // interval) - 1)
6) The above expression will gives the count of intervals in the maximum possible number. <br/>
   The above expression * interval + bias gives the col count which is the maximum possible number in the series. <br/>
 
3 <br/>
5  = (no of interval * interval) + bias = (2 * 2) + 1 <br/>
7  = (no of interval * interval) + bias = (3 * 2) + 1 <br/>
Then, the expression will be... 3 + ((2*2)+1)) + ((3*2)+1)). From the expression we observed that the common values are the bias and interval. <br/>
Then, min + (interval * (sum of series --> whereas, no of interval in 2nd number = min, no of intervals in last number = max) ) + (row count excluding 1st number * bias) will be the formula to find out sum of the series. <br/>
Here, (2+3) part will be substituted in the formula from 2nd approach whereas 2 will be the start and 3 will be the stop. <br/>
After computing sum of the series part, we're substituting in the above formula to get sum of the series.


## :one: Total possible count excluding min value (Row count excluding 1) = ((max-min) // interval)
## :two: Second possible number = min + interval
## :three: bias = second possible number % interval
## :four: second number interval count = second possible number // interval
## :five: total interval count till minimum = min // interval
## :six: last possible = ( (total interval count till minimum + Total possible count excluding min value ) * interval) + (Total possible count excluding min value * bias)
## :seven: second number interval count = second_possible_number // interval
## :eight: last possible interval count = last_possible // interval

try:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  sec_num_inter_count = row_excluding_1st_no * sec_num_inter_count / row_excluding_1st_no<br/>
except:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  sec_num_inter_count = 0<br/>
try:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  last_possible_inter_count = row_excluding_1st_no * last_possible_inter_count / row_excluding_1st_no<br/>
except:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  last_possible_inter_count = 0<br/>

### NOTE :pencil2: : Again, we're doing correction in interval count in second number and last number. Why we're doing this.. This is just an exception handling to avoid an error when the second possible number is greater than the input 'max'. In that case 'Total possibles count excluding min value' will be zero. Then, the 'second number interval count' should also be 0. Because there is nothing to compute. That value will be passed to compute upcoming series sum. So, here we're multiplying interval counts of second and last number with Total possible count excluding min value. Then, we are dividing it with Total possible count excluding min value. There will be no change in the interval counts, if those are greater than zero. If 'Total possible count excluding min value' is zero, the the expression will be like this 0 / 0 and this is nothing. Error will be thrown for this calculation 'Divide by zero'. For this situation, we're assigning zero for second and last number interval counts. So, the series sum be zero.

## :nine: series_sum = ((((Total possible count excluding min value ** 2) - Total possible count excluding min value) / 2) + Total possible count excluding min value) - (((((second number interval count - 1) ** 2) - (second number interval count - 1)) / 2) + (second number interval count - 1))
### NOTE :pencil2: : Substituting 'second number interval count' as 'min' and 'Total possibles count excluding min value' as 'max' in the formula from approach - 2 "((((max ** 2) - max) / 2) + max) - (((((min - 1) ** 2) - (min - 1)) / 2) + (min - 1))" which is series sum.
## :one::zero: sum of bias = Total possibles count excluding min value * bias

## NOTE :pencil2: : All above 10 steps should be done one by one and finally substitute in the below given formula. 
# Discovered Formula : min + (interval * (series sum)) + sum of bias

## Python code for Approach - 3:
min_input, max_input, interval = int(input()), int(input()), int(input())<br/>
start_time = datetime.datetime.now()<br/>

row_excluding_1st_no = ((max_input-min_input) // interval)<br/>
second_possible_number = min_input + interval<br/>
bias = second_possible_number % interval<br/>
total_inter_count_till_min = min_input // interval<br/>
last_possible = ( (total_inter_count_till_min + row_excluding_1st_no ) * interval) + (row_excluding_1st_no * bias)<br/>

sec_num_inter_count = second_possible_number // interval<br/>
try:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;    sec_num_inter_count = row_excluding_1st_no * sec_num_inter_count / row_excluding_1st_no<br/>
except:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;    sec_num_inter_count = 0<br/>
    
last_possible_inter_count = last_possible // interval<br/>
try:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;    last_possible_inter_count = row_excluding_1st_no * last_possible_inter_count / row_excluding_1st_no<br/>
except:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;    last_possible_inter_count = 0<br/>

series_sum = ((((last_possible_inter_count ** 2) - last_possible_inter_count) / 2) + last_possible_inter_count) - (((((sec_num_inter_count - 1) ** 2) - (sec_num_inter_count - 1)) / 2) + (sec_num_inter_count - 1))<br/>
sum_bias = row_excluding_1st_no * bias<br/>
final_output = min_input + ((interval * series_sum) + sum_bias)<br/>
print(final_output)<br/>
print("The end time is ", datetime.datetime.now() )<br/>
print("The start time is ", start_time )<br/>

