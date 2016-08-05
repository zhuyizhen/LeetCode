# leetcode

## List
+ [338. Counting Bits](#338)
+ [344. Reverse String](#344)

## Detail
<h3 id="338">338. Counting Bits</h3>
**LeetCode Link:**  
[https://leetcode.com/problems/counting-bits/](https://leetcode.com/problems/counting-bits/)  
**Problem description:**  
Given a non negative integer number num. For every numbers i in the range 0 ≤ i ≤ num calculate the number of 1's in their binary representation and return them as an array.  
**Source code:**  
[https://github.com/zhuyizhen/LeetCode/tree/master/src/338_Counting_Bits](https://github.com/zhuyizhen/LeetCode/tree/master/src/338_Counting_Bits)  
**Detail:**  
\- My solution of JavaScript:  
```
	var countBits = function(num) {
		var bitsNumArray = [0];
		for (i = 1; i <= num; i++) {
			if (i % 2) {
				bitsNumArray[i] = bitsNumArray[Math.floor(i / 2)] + 1;
			} else {
				bitsNumArray[i] = bitsNumArray[Math.floor(i / 2)];
			}
		}
		return bitsNumArray;
	};
```
 Runtime: 257ms  
 **Explanation:**  
 \- This blog introduced a lot of related algorithms:  
[http://www.cnblogs.com/graphics/archive/2010/06/21/1752421.html](http://www.cnblogs.com/graphics/archive/2010/06/21/1752421.html)
 
<h3 id="344">344. Reverse String</h3>
**LeetCode Link:**  
[https://leetcode.com/problems/reverse-string/](https://leetcode.com/problems/reverse-string/)  
**Problem description:**  
Given s = "hello", return "olleh".  
**Source code:**  
[https://github.com/zhuyizhen/LeetCode/tree/master/src/344_Reverse_String](https://github.com/zhuyizhen/LeetCode/tree/master/src/344_Reverse_String)  
**Detail:**  
\- My solution of JavaScript:  
```
	var reverseString = function(s) {
	    return s.split("").reverse().join("");
	};
```
 Runtime: 180ms  
\- Sample C solution:
```
	char* reverseString(char* s) {
		int len = strlen(s);
		char* temp;
		for(int i = 0; i < len / 2; i++) {
			temp =  *(s + i);
			 *(s + i) =  *(s + len - 1 - i);
			 *(s + len - 1 - i) = temp;
		}
		return s;
	}
```
 Runtime: 4ms
 