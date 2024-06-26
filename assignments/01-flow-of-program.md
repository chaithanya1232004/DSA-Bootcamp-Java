[Video Link](https://youtu.be/lhELGQAV4gg)

## Create flowchart and pseudocode for the following:

1. Input a year and find whether it is a leap year or not.
2. Take two numbers and print the sum of both.
3. Take a number as input and print the multiplication table for it.
4. Take 2 numbers as inputs and find their HCF and LCM.
5. Keep taking numbers as inputs till the user enters ‘x’, after that print sum of all.
1. Pseudocode:
start
input year
if ((year %% 4 == 0) && (year %% 100 == 0) || (year %% 400 == 0))
output "Leap Year"
else
output "Not Leap Year"
exit

2.Pseudocode:
start
input a,b
sum = a + b
output sum
exit

3.Pseudocode:
start
input num
for(i=1;i<=10;i++)
println(num + "*" + i + "=" + num*i)
exit

4.Pseudocode:
star
input num1,num2
temp1=num1
temp2=num2
while(temp2 != 0)
temp=temp2
temp2=temp1%temp2
temp1=temp
output hcf=temp1
output lcm=(num1*num2)/hcf
exit

5.Pseudocode:
start
input num
while(num!='x')
temp = num
output num
output num = num + temp
exit


