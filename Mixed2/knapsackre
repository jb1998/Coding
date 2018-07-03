public class Knapsnack {
static int[][] dp;
    public static int knapsack(int[] weight, int value[], int maxWeight) {
        dp = new int[maxWeight+1][value.length+1];
        for(int i=0;i<dp.length;i++){
            for(int j=0;j<dp[0].length;j++){
                dp[i][j]=-1;
            }
        }
        int ans = helper( weight, value, maxWeight,value.length);
        return ans;
    }

    private static int helper(int[] weight, int[] value, int maxWeight,int current) {
        if(current<=0 || maxWeight<=0){
            return 0;
        }
        int including=0;
        int excluding=0;
        if(dp[maxWeight][current]==-1) {
            if (maxWeight - weight[current - 1] >= 0)
                including = value[current - 1] + helper(weight, value, maxWeight - weight[current - 1], current - 1);

            excluding = helper(weight, value, maxWeight, current - 1);

            dp[maxWeight][current]=Math.max(including,excluding);
        }

        return dp[maxWeight][current];
    }
    public static void main(String args[]){
     int arr1[]={1,2,4,5};
     int arr2[]={5,4,8,6};
        System.out.println(knapsack(arr1,arr2,5));
    }
}
