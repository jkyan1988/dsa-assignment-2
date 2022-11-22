<strong><h2>Week 2 Assignment</h2></strong>

<b><h3>Problem #1: Multiple Pointers Pattern</h3></b>

Write a function called subsequence which takes in two strings and checks whether 
the characters in the first string form a subsequence of the characters in the second string. 
In other words, the function should check whether the characters in the first string 
appear somewhere in the second string, without their order changing.
Write your solution with time complexity O(n) and space O(1)


    const subsequence = (str1, str2) => {
    let arr1 = str1.split("");
    let arr2 = str2.split("");
   
    if (arr1.length === 0 || arr2.length === 0) {
        return false;
    }
    let Index = 0;
    for (let i = 0; i < arr2.length; i++) {
        if (arr2[i] === arr1[Index]) {
            Index++;
            if (Index === arr1.length) {
                return true;
            }
        }
    }
    return false;
    };


Test Cases:

subsequence('hello', 'hello world') true

subsequence('sing', 'sting') true

subsequence('abc', 'abracadabra') true

subsequence('abc', 'acb') false


<b><h3>Problem #2: Sliding Window Pattern</h3></b>

Write a function called longestSubstringInString, which accepts a string and 
returns the length of the longest substring with all distinct characters.
Please write in time complexity of O(n)



    const longestSubstringInString = (str) => {
    let set = new Set(); 

    let j = 0; 
  
    while (j < str.length) {
        if (!set.has(str[j])) {
            set.add(str[j])
            j++
        } else {
            return set.size
        }
    }
    }





Test Cases:

longestSubstringInString('') 0

longestSubstringInString('rithmschool') 7

longestSubstringInString('thisisawesome') 6

longestSubstringInString('thecatinthehat') 7

longestSubstringInString('bbbbbb') 1

longestSubstringInString('longestsubstring') 8

longestSubstringInString('thisishowwedoit') 