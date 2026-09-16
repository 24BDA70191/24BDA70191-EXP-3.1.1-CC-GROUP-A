# 24BDA70191-EXP-3.1.1-CC-GROUP-A
class Solution {
public:
    int climbStairs(int n) {
        if (n <= 2) return n;

        int prev2 = 1; // Base case for n = 1
        int prev1 = 2; // Base case for n = 2

        for (int i = 3; i <= n; ++i) {
            int curr = prev1 + prev2;
            prev2 = prev1;
            prev1 = curr;
        }

        return prev1;
    }
};
