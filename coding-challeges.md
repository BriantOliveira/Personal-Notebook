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

6 - Given a array of numbers, output the array like this: a1 &lt;= a2 &gt;= a3 &lt;= a4 &gt;= a5.

When we encounter the ith number, if i is even, then if ai ai-1, swap ai and ai-1.

---

You are given a license key represented as a string S which consists only alphanumeric character and dashes. The string is separated into N+1 groups by N dashes.

Given a number K, we would want to reformat the strings such that each group contains exactly K characters, except for the first group which could be shorter than K, but still must contain at least one character. Furthermore, there must be a dash inserted between two groups and all lowercase letters should be converted to uppercase.

Given a non-empty string S and a number K, format the string according to the rules described above.

**Example 1:**

```
Input:
 S = "5F3Z-2e-9-w", K = 4


Output:
 "5F3Z-2E9W"


Explanation:
 The string S has been split into two parts, each part has 4 characters.
Note that the two extra dashes are not needed and can be removed.
```

**Example 2:**

```
Input:
 S = "2-5g-3-J", K = 2


Output:
 "2-5G-3J"


Explanation:
 The string S has been split into three parts, each part has 2 characters except the first part as it could be shorter as mentioned above.
```

**Note:**

1. The length of string S will not exceed 12,000, and K is a positive integer.
2. String S consists only of alphanumerical characters \(a-z and/or A-Z and/or 0-9\) and dashes\(-\).
3. String S is non-empty.

   ```
   Step 1 - Check if string is has continues dashes like "----" and if so, return empty string
   Step 2 - If the string S contains only 1 character, return that character in uppercase.
   Step 3 - If the string S doesn’t contain any character, return invalid.
   Step 4 - Check if string length is equal to 1, and if true check if the value is not a single dash "-" and
   return string to upperCase
   Step 5 - If the string S doesn’t consists only of alphanumerical characters (a−z and/or A−Z
    and/or 0−9) and/or dashes (-), return invalid.
   Step 6 - Second, I must take all of dashes out of the string S. And I could transform the string to uppercase at this point also
   Step 7 - Third, loop through the string and add “-” where it should be, depend on variable K
   Step 8 - Lastly, return the finished String.
   ```

`function isAlphaNumeric(char) {  
    var code = char.charCodeAt();  
    if (  
      !(code > 47 && code < 58) &&  
      !(code > 64 && code < 91) &&  
      !(code > 96 && code < 123) &&  
      !(code === 45 || code === 47)  
    ) {  
      return false;  
    }  
    return true;  
  }`

`/**`

* `@param {string} S`
* `@param {number} K`
* `@return {string}  
  */  
  var licenseKeyFormatting = function(S, K) {`

  `const exp = ([\-]){${S.length}, ${S.length}}  
  const regex = new RegExp(exp)  
  if (S.search(regex) == 1)  
   { return ""}`

  `if (S.length < 1) return "invalid";  
  if (S.length == 1 && S[0] !== '-') return S.toUpperCase();  
  if (K < 0) return "invalid";`

  `for (let k in S) {  
   if (!isAlphaNumeric(S[k])) return "invalid";  
  }  
  let key = 0;  
  let strObj = {};  
  for (let c of S) {  
   if (c != "/" && c != "-") {  
     strObj[key] = c.toUpperCase();  
     key++;  
   }  
  }  
  let newStr = "";  
  let counter = key - 1;`

  `for (let k in strObj) {  
   newStr += strObj[k];  
   if (counter !== 0 && counter % K === 0) {  
     newStr += "-";  
   }  
   counter--;  
  }  
  return newStr;  
  };`



