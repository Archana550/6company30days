# 1. [Trim a binary search tree](https://leetcode.com/problems/trim-a-binary-search-tree/description/)

# 2. [Construct the longest new string](https://leetcode.com/problems/construct-the-longest-new-string/description/)

# 3. [Short encoding of words](https://leetcode.com/problems/short-encoding-of-words/description/)

# 4. [Constrained subsequence sum](https://leetcode.com/problems/constrained-subsequence-sum/description/)

# 5. [Special permutations](https://leetcode.com/problems/special-permutations/description/)

# 6. [Matrix cells in distance order](https://leetcode.com/problems/matrix-cells-in-distance-order/description/)

```java
  class Solution {
    public int[][] allCellsDistOrder(int rows, int cols, int rCenter, int cCenter) {
        int[][] arr = new int[rows*cols][2];
        // variable to traverse through the array
        int cntr = 0;
        //  STEP-1
        for(int i = 0; i < rows; i++){
            for(int j = 0; j < cols; j++){
                arr[cntr][0] = i;
                arr[cntr++][1] = j;
            } 
        }
        // STEP-2
        insertionSort(arr, rCenter, cCenter);
        return arr;
    }

    public void insertionSort(int[][] arr, int rC, int cC){
        for(int i = 0; i < arr.length - 1; i++){
            for(int j = i + 1; j > 0; j--){
                // STEP-3
                if((Math.abs(arr[j][0] - rC) + Math.abs(arr[j][1] - cC)) < (Math.abs(arr[j - 1][0] - rC) + Math.abs(arr[j - 1][1] - cC))){
                    swap(arr, j, j - 1);
                }
            }
        }
    }

    public void swap(int[][] arr, int n1, int n2){
        int[] temp = arr[n1];
        arr[n1] = arr[n2];
        arr[n2] = temp;
    }
}
```

# 7. [The skyline problem](https://leetcode.com/problems/the-skyline-problem/description/)

# 8. [Minimum cost of paths with special roads](https://leetcode.com/problems/minimum-cost-of-a-path-with-special-roads/description/)

# 9. [Largest word in dictionary through deleting](https://leetcode.com/problems/longest-word-in-dictionary-through-deleting/description/)

# 10. [Find players with 0 or 1 looses](https://leetcode.com/problems/find-players-with-zero-or-one-losses/description/)

# 11. [Cinema seat alocation](https://leetcode.com/problems/cinema-seat-allocation/description/)

# 12. [Airplane seat assignment probablity](https://leetcode.com/problems/airplane-seat-assignment-probability/description/)

# 13. [Erect the fence](https://leetcode.com/problems/erect-the-fence/description/)

# 14. [Get equal substring within budget](https://leetcode.com/problems/get-equal-substrings-within-budget/description/)

# 15. [Last moment before all ants fall into a plank](https://leetcode.com/problems/last-moment-before-all-ants-fall-out-of-a-plank/description/)
