1- If you have an unsorted array of numbers from 1-100, except 1 of those numbers is missing, how do you determine which number is missing.

DM was nearly correct the but missed out the right operator Answer is 100\*\(100+1\)/2 - sum\(array\) Explanation: The series 1-100 is a arithmetic series therefore the sum of arithmetic series is n\*\(a1 + an\)/ 2 In this case n=100, a1\(first element\) = 1, and an\(last element\)=100. Therefore Sum of the series is 100\*\(100+1\)/2. To find missing number subtract the sum of the array with the arithmetic series sum.



2 - What is the output? int n = 1; puts\(\(\(char\*\)&n\)\[0\]==1?"Y":"N"\);

yes..depends on the system architecture whether it is big endian or little endian int n = 1; stores it in the following way in 4 bytes 00000000 00000000 00000000 00000001 \(increasing memory addresses\) \(char\*\)&amp;n will make n de-reference to only 1 byte instead of 4 bytes. For big endian, \(char\*\)&amp;n\[0\] will be 00000000 and for little endian it will be 00000001

