## Chap 2 | Two pointers

Algorithm ➡️ It involves having two integer variables that both move along an iterable

2 pointers Variation 1 ➡️ Start the pointers at the edges of the input .Move them towards each other until they meet

Time Complexity : We will never have more than O(n) iterations for the while loop because the pointers start n away from each other and move at least one step closer in every  iteration. Therefore, if we can keep the work inside each iteration at O(1), this technique will result in a linear runtime, which is usually the best possible runtime 

