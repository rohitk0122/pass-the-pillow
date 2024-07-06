# pass-the-pillow
class Solution {
    public int passThePillow(int n, int time) {
        int cycleLength = 2 * (n - 1);

        // Find the effective time by taking time modulo cycleLength
        int effectiveTime = time % cycleLength;

        // Determine the direction and position
        if (effectiveTime < n) {
            // Pillow is moving forward
            return 1 + effectiveTime;
        } else {
            // Pillow is moving backward
            return 2 * n - 1 - effectiveTime;
        }
    }

    public static void main(String[] args) {
        Solution solution = new Solution();
        int n = 5;
        int time = 7;
        System.out.println(solution.passThePillow(n, time)); // Output: 4
    }
}
