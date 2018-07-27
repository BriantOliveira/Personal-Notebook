1- If you have an unsorted array of numbers from 1-100, except 1 of those numbers is missing, how do you determine which number is missing.

DM was nearly correct the but missed out the right operator Answer is 100\*\(100+1\)/2 - sum\(array\) Explanation: The series 1-100 is a arithmetic series therefore the sum of arithmetic series is n\*\(a1 + an\)/ 2 In this case n=100, a1\(first element\) = 1, and an\(last element\)=100. Therefore Sum of the series is 100\*\(100+1\)/2. To find missing number subtract the sum of the array with the arithmetic series sum.

2 - What is the output? int n = 1; puts\(\(\(char\*\)&n\)\[0\]==1?"Y":"N"\);

yes..depends on the system architecture whether it is big endian or little endian int n = 1; stores it in the following way in 4 bytes 00000000 00000000 00000000 00000001 \(increasing memory addresses\) \(char\*\)&n will make n de-reference to only 1 byte instead of 4 bytes. For big endian, \(char\*\)&n\[0\] will be 00000000 and for little endian it will be 00000001

3 - Out of 10 coins, one weighs less then the others. You have a scale. How can you determine which one weighs less in 3 weighs? Now how would you do it if you didn't know if the odd coin weighs less or more?

First Trial: 5 coins at each side of the scale. Exclude all the 5 coins in the heavy side. Now you have only 5 coins. Second Trial: Hold one coin in your hand and put 2 coins at each side of the scale. If the two sides weighs the same, then the lighter one is the one you are holding in your hand. If one side is heavier than the other, exclude the two coins in that side. Now you have only 2 coins and a scale to find out which is the lighter by using the scale for a third time.

4 - Explain in detail what happens when you click on a link in an html page. and how you determine if the link contains and image.

The **Multipurpose Internet Mail Extensions \(MIME\) type **is a standardized way to indicate the nature and format of a document. It is defined and standardized in IETF RFC 6838Internet Assigned Numbers Authority \(IANA\). The is the official body responsible for keeping track of all official MIME types, and you can find the most up-to-date and complete list at the Media Types page.

Browsers often use the MIME type \(and not the file extension\) to determine how it will process a document; it is therefore important that servers are set up correctly to attach the correct MIME type to the header of the response object.



5 - Given an array of int which represents a number. Write a function that and adds 1/2 this number.

```
[1,3,4] -> [1,3,5]
[1,9,9] -> [2,0,0]
[9,9,9] -> [1,0,0,0]

def add_one(given_array):
    carry = 1
    result = new int[given_array.length]
    for i from(given_array.length -1) down to 0:
        sum = given_array[i] + carry
        if sum == 10: carry = 1
        else: carry = 0 
        result[i] = sum % 10
    if carry == 1:
        result = new int[given_array.length +1]
        result[0] = 1
        return result
        
```



