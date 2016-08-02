# leetcode

## List
+ [344. Reverse String](#344)

## Detail
<h3 id="344">344. Reverse String</h3>
**LeetCode Link:**  
[https://leetcode.com/problems/reverse-string/](https://leetcode.com/problems/reverse-string/)  
**Problem description:**  
Given s = "hello", return "olleh".  
**Source code:**  
[https://github.com/zhuyizhen/LeetCode/tree/master/src/344_Reverse_String](https://github.com/zhuyizhen/LeetCode/tree/master/src/344_Reverse_String)  
**Detail:**  
\- My solution with JavaScript:  
```
	var reverseString = function(s) {
	    return s.split("").reverse().join("");
	};
```
 Runtime: 96ms  
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
 