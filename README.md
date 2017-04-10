# Codility
Lesson 3-1
[40%] PermMissingElem

class Solution {
    public int solution(int[] A) {
        // write your code in Java SE 8
        int sum = 0;
        int max = 0;
        int min = 100000;
        for (int i = 0; i < A.length; i++) {
            if (max < A[i])
                max = A[i];
            if (min > A[i])
                min = A[i];
            sum += A[i];
        }
        int area = ( (A.length + 1) * (A.length + 2) ) / 2;
        if (min != 1)
            area += (min-1) * (A.length + 1);
        int missingNum = area - sum;
        return missingNum;
    }
}
