# Part 1a

## `var` declaration

1. `values added: 20`
2. `final result: 20`

## `let` declaration

1. `values added: 20`
2. Error, because `result` is not defined in line 13. It is only defined in the scope of the `if` statement block due to the `let` declaration, so it cannot be called outside of it.

## `const` declaration

1. Error, because you cannot assign a new value to an already declared constant variable.
2. Error, because `result` is not defined in line 13. Since it was declared inside of the `if` statement block, its scope is limited to that block.

# Part 1b

1. The output will be `3` because `i` is declared with var, so its scope is the entire function. After 3 iterations of the `for` loop, `i` = 3 and the loop ends because it is no longer less than the length of the `prices` array (3). That value of `i` is then outputted.
2. The output will be `150` because the final iteration of the `for` loop updates `discountedPrice` to the last element in the `prices` array times `1 - discount`, which is `300 * (1 - 0.5)` = `150`. `discountedPrice` is declared with `var` declaration, so its scope is the entire function and thus can be called outside of the `for` loop.
3. The output will be `150` because the final iteration of the `for` loop updates `finalPrice` to `discountedPrice` rounded to the nearest hundredth, which is `Math.round(150 * 100) / 100` = `150`.
4. The function returns an array of the respective discounted prices of the input `prices` array (in this case, it returns `[50, 100, 150]`). Each iteration of the `for` loop pushes the final discounted price of a `prices` element in order, which is then returned at the end of the function.
5. There will be an error because `i` is not defined in the scope of the overall function. Because it was declared with `let` in the for loop, it cannot be called outside of the loop.
6. There will be an error because `discountedPrice` is not defined in the scope of the overall function. Because it was declared with `let` inside the for loop, it cannot be called outside of the loop.
7. The output will be `150` because the final iteration of the `for` loop updates `finalPrice` to `discountedPrice` rounded to the nearest hundredth, which is `Math.round(150 * 100) / 100` = `150`. The `let` declaration does not affect line 14 because the scope of `finalPrice` is the entire function so it can be called anywhere inside the function.
8. The function returns an array of the respective discounted prices of the input `prices` array (in this case, it returns `[50, 100, 150]`). Each iteration of the `for` loop pushes the final discounted price of a `prices` element in order, which is then returned at the end of the function. Nothing is accessed outside of its scope even with the `let` declarations, and the function runs as intended.
9. There will be an error because `i` is not defined in the scope of the overall function. Because it was declared with `let` in the for loop, it cannot be called outside of the loop.
10. The output will be 3 because `length` is declared as the length of the `prices` array, which is 3. There are no attempts to assign new values to it, and it was declared with the scope of the entire function, so there are no issues with the `const` declaration as well as calling `length` within the function.
11. The function returns an array of the respective discounted prices of the input `prices` array (in this case, it returns `[50, 100, 150]`). Each iteration of the `for` loop pushes the final discounted price of a `prices` element in order, which is then returned at the end of the function. Though `discounted` is declared as a `const` variable, it is never reassigned a different array, so there are no errors. Operations like pushing elements into the array are fine and do not conflict with the constant declaration.

## Data Types

12.
    A. `student.name`
    
    B. `student['Grad Year']`
    
    C. `student.greeting()`
    
    D. `student['Favorite Teacher'].name`
    
    E. `student.courseLoad[0]`

## Basic Operators & Type Conversion

13.
    A. `32`: 2 is converted to string and concatenated to 3 to form '32'
    
    B. `1`: '3' is converted to its numeric value (3) and 2 is subtracted from it to form 1
    
    C. `3`: null is converted to its numeric value (0) and added to 3 to form 3
    
    D. `3null`: null is converted to string and concatenated to 3 to form '3null'
    
    E. `4`: true is converted to its numeric value (1) and added to 3 to form 4
    
    F. `0`: both false and null are converted to their numeric value (0) and added to form 0
    
    G. `3undefined`: undefined is converted to string and concatenated to 3 to form '3undefined'
    
    H. `NaN`: undefined is converted to its numeric value (NaN), which forms NaN
    

14. 
    A. `true`: '2' is converted to numeric 2, which is greater than 1
    
    B. `false`: the strings '2' and '12' are compared, the first character '2' is greater than '1' so '2' is greater than '12'
    
    C. `true`: '2' is converted to numeric 2, which is equal to 2
    
    D. `false`: '2' is a different type from 2, so the strict === comparison returns false
    
    E. `false`: true is converted to numeric 1, which is not equal to 2
    
    F. `true`: Boolean(2) is converted to boolean true, which is equal to and same type as true
    
15. == compares values and may return true even if they are different types as long as they have the same values when converted, while === returns false if the values compared are of different types

## Loops

16. [part1b-question16.js](./part1b-question16.js)

## Functions

17. `modifyArray` will return an array containing `[2,4,6]`. `modifyArray` loops through each value in `array` (`[1,2,3]`), calling `doSomething` on each element and pushing that result to `newArr`. In this case, `doSomething` doubles the number inputted, so it ends up doubling each number in the array and pushing it to `newArr`. After each element is doubled and pushed, the array is returned.

## setInterval(), setTimeout(), clearTimeout()

18. [part1b-question18.js](./part1b-question18.js)
19. The code outputs:

    1
    
    4
    
    3
    
    2
    
    This happens since the lines that output 2 and 3 are attached to timers that tick down before they get outputted, while 1 and 4 are immediately outputted. 2 has the longest timer.
