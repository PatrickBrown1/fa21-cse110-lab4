1. Line 12 will print 3. Because we initialize i as a var in a function, we can access it throughout the rest of the function block. i increments in the for loop
   up until the length of prices, which is 3.
2. It will print 150. Again, because discounted price is instantiated as a var, we can access it throughout the rest of the function discountPrices. So, discountedPrice 
   will be equal to the last value of discountedPrice we calculated. This will be on i=2, so we calculate discountedPrice = prices[i] * (1 - discount) = 300 * (1-.5) = 150.
3. It will print 150. Similarly to the previous question, we instantiate finalPrice as a var within the discountPrice function, which means we can access it throughout the 
   rest of the function. Therefore, it will print the last value that finalPrice is set to. This will be when i=2, and will be equal to 
   Math.round(discountedPrice * 100) / 100 = Math.round(15000) / 100 = 150.
4. This function will return [50, 100, 150]. This is because it returns the discounted price for each of the values in prices. The discount for 100 is 50, for 200 is 100, 
   and for 300 is 150. Because we iterate and push in linear order, it will return values in the same order as the input list.
5. It will give an error because i is instantiated with the let keyword, and is only accessable in the for loop.
6. This will also give an error because discountedPrice is instantiated inside the for loop. Because the print statement is outside of the for loop, it loses scope of 
   discountedPrice, and therefore will not be able to print the variable as it doesn't exist within this scope.
7. This will print 150. This is because the finalPrice is initialized outside of the for loop, and in the same scope as the console.log statement. Therefore, it 
   exists when we try to print it. The value it holds will be the most recent value put into it, which will be for iteration i=2. From the previous question (question 3), we know that this value is 150.
8. This function will return [50, 100, 150], the same value as the previous function (question 4). The variable being returned, discounted, is initialized with the let 
   keyword at the top of the function, so it can be updated from any code blocks within the function, and can be access within the scope of the function as well. 
   Therefore, there are no issues updating or returning this value, so it returns the correct value, which is the same as the value from question 4.
9. Line 11 will error out because i is initialized with the let keyword within the for loop. This means it cannot be accessed from outside of the for loop, and cannot be accessed from line 11.
10. Line 11 will print 3. The length variable is initialized to the length of prices, which is 3. We never attempt to reassign it, so it does not error.
11. It will return [50, 100, 150]. We get the correct answer even though discounted is initialized with the const keyword. This is because the const keyword just makes sure that the reference of the variable never changes, however the value of the variable can change. Therefore, we can correctly push values into the array, and get the discounted values of 100, 200 and 300 in order, which are [50, 100, 150].
12. 
    A. Accessing the value of the name property in the student object
        student.name
    B. Accessing the value of the Grad Year property in the student object
        student['Grad Year']
    C. Calling the function for the greeting property in the student object
        student['greeting']()
    D. Accessing the name property of the object in the Favorite Teacher property in student
        student['Favorite Teacher'].name
    E. Access the first index in the array of the courseLoad property of the student object
        student.courseLoad[0]

13. Arithmetic
    ‘3’ + 2 = '32' because 2 maps to it's string representation, '2', and the + represents string concatenation
    ‘3’ - 2 = 1, '3' gets converted to a number as the minus represents a mathematical function
    3 + null = 3, null turns into a 0 in mathematical functions
    ‘3’ + null = '3null', null converts to 'null' during string concatenation
    true + 3 = 4, true converts to 1 during arithmetic
    false + null = 0, because neither of these values are strings, this gets treated as arithmetic addition, where false and null both convert to 0 
    '3' + undefined = '3undefined', because '3' is a string we are doing string concatenation, and undefined turns into 'undefined'
    '3' - undefined = NaN, we have a - so we must be doing arithmetic, so '3' converts to 3 and undefined converts to NaN, so we always get NaN.

14. Comparison
    ‘2’ > 1 = True. When comparing different types, js converts all of the types to integers, so '2' converts to 2, making this statement true.
    ‘2’ < ‘12’ = False. When comparing strings, we compare from left to right. Because the first character of '2' is greater than the first of '12', '2' > '12'
    2 == ‘2’ = True. '2' converts to an integer
    2 === ‘2’ = False. === compares without converting types. So 2 is not the same as '2' because they are different types.
    true == 2 = False. true is equivalent to 1 when converted to an integer 
    true === Boolean(2) = true. Any non-zero integer converted to an integer becomes true. So Boolean(2) becomes true, and now both sides are the same type and value.

15. The == and === operators differ in one major way. The == operator will attempt to convert the two values to be the same type (number if they are different), and then compare the two values. The === operator on the otherhand will not even attempt to convert the types. So if you are comparing two values of different types like '2' and 2, '2' === 2 will always return false because they are different types, but '2' == 2 will convert '2' to 2, and then 2 == 2 will be true.

17. This function returns [2,4,6].doSomething takes in a variable and returns that value multiplied by two. modifyArray creates a new array, pushes the result of callback with each value of the input array into this new array, and returns the new array. Combining these two functions, modifyArray([1,2,3], doSomething) returns [2,4,6] because it returns a copy of the old array where every value is multiplied by 2.

19. 
    1
    4
    3
    2

This is because the timeouts take longer to execute thant he regular console.logs. So 1 will execute first, then 4 (because we are traveling from top to bottom). Then 3 will execute because it has a timer of 0, and 2 will execute last 1s after the start of the program.