public class Countways {
    public static int countWaysToMakeChange(int denominations[], int value) {

        return helper(denominations, value, 0);
    }

    private static int helper(int[] denominations, int value, int i) {
        if (value == 0)
            return 1;
        if(value<0)
            return 0;
        if (i >= denominations.length && value>0) {
            return 0;
        }

        int r1 = 0, r2 = 0;
            r1 = helper(denominations, value - denominations[i], i );
            r2 = helper(denominations, value, i + 1);

        System.out.println(r1 + " " + r2);
        return (r1 + r2);
    }

    public static void main(String args[]) {
        int arr[] = {1, 2, 3};
        System.out.println(countWaysToMakeChange(arr, 4));
    }
}
