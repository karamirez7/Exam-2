1. numSequences[i] = numSequences[i-1] + 1 if the current position of the original numbers array is within sequence 

2. This problem will use an array to store When looking at the first valid sequence within the given array, subsequent values that are also part of the sequence grow by 1 more than the number of times from the previous valid sequence. If we look at the sequence 1,2,3,4 valid sequences include the intial 1,2,3 and the subsequent sequences 1,2,3,4 and 2,3,4 (1 more than the previous). Repetitive work would have been counting the number of valid sequences that exist in the longest one we may have found (eg. knowing we found the sequence 1,2,3,4,5 and still checking if 2,3,4, and 2,3,4,5 are valid sequences). Every index within the created array notes the number of sequences found at that point. We continue to add 1 to the previous as long as future values are part of the sequence we were checking.

3. By first working the problem out by hand, it became clear that repetitive work was checking for the number of sequences within a large sequence already found. It was noted that when looking at the sequence 1,3,5,7,9 as a whole, there were 3 possible answers within it [1,3,5], [1,3,5,7], [1,3,5,7,9].
We can then count the number of sequences by cutting out the left most value and know that all of those
values are still valid sequences [3,5,7,9] -> [3,5,7], [3,5,7,9] and decreaseas as so until there is 1 sequence left to count. Through some tests and examination of these potential values, it was examined that the same count can be applied in reverse (1->3 instead of 3->1) to perform calculations and sums in linear time.  


