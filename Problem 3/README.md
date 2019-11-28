    //after looking at one character(simplest case)
1. while (i(left of current char), j(right of current char) is in range of string)
      NumPalindromes += 1 if character at j,i are equal to each other, else we are done looking
      i++, j++
       
    (looking at the String "abaa" and character b as simplest case)
     the next substring "aba" is still a substring since the string before was a palindrome
     and the start and end characters are equal
     
     // the other simplest case to check would be every pair of adjacent characters performing the same idea as above

2. There is no specific data structure used to store previous solutions. Instead the idea comes from the fact that a single character
   is a palindrome and subsequent strings can be checked only looking at the surrounding characters as the the smaller string before it was
   a palindrome. If the growing string stops being a palindrome, then there is no need to continue checking at that starting character
   (Every character of the string is eventually treated as the starting point). Since there are 2 different cases when it comes to checking
   palindromes, even and odd length strings, every adjacent pair of characters within that string is also treated as a starting point to a
   palindrome.

3. Examples of palindromes were worked out by hand, including the simplest case of one letter. The pattern recognized was that palindromes
typically require 2 additional letters to remain a palindrome. It is assumed that a string previously a palindrome would remain a palindrome
by following the necessary requirements of adding 2 exact characters at the ends of the string. It was first tested with the idea that one
character is enough to check every possible palindrome with a string, but the case "abba" made it clear that 2 characters was also another
base case when dealing with palindromes.

