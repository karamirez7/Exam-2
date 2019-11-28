1. if (currChain in lengthChainsStored):
      return lengthChainsStored[currChain]
   if there is no available chain to extend: return 1 and store the mapped list and value
   lengthChainsStored[currChain] = chainLength(validChainFound) + 1 // lengthChainsStored[currChain] will be replaced with
                                                                       the best chain length found from all options
   
   //is performed on every list
   
2. This problem will use a hashmap to store previous solutions. These values mapped are of a list from the given input 
and the best chain length that can be obtained for that list. When we see a list we have already visited, it should not be necessary
to perform the operations to calculate the best chain length for that pair as it should have been determined previously. To find the
best chain length we look at every possible option to take from a pair within the given list. Once all options have been checked, the best
chain length is stored for future possible chains that may link up to that pair.


3. The key step to coming up with this idea was working the problem out by hand and noticing that I had to find the longest chain length
again for a pair I had already looked at. For example if the original list was [[1,2][3,7][3,6][2,5][7,8]], I would see that [1,7] was a
possible pairing, and that [3,7] had no chain beyond that. So, if I remembered that best chain length for that pair, I wouldnt have to
go through the whole list again and find chains for it and instead add that chain length to the current list I was working on.
