import java.util.Scanner;

public class SubsetSum {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        int k=sc.nextInt();
        boolean dp[][]=new boolean[arr.length+1][k+1];
        for(int i=0;i<dp[0].length;i++){
            dp[0][i]=false;
        }
        for(int i=0;i<dp.length;i++){
            dp[i][0]=true;
        }
        for(int i=1;i<dp.length;i++){
            for(int j=1;j<dp[0].length;j++){
                dp[i][j]=dp[i-1][j];
                if(arr[i-1]<=j){
                    dp[i][j]=dp[i][j] || dp[i-1][j-arr[i-1]];
                }
            }
        }
        if(dp[arr.length][k])
        System.out.println("YES");
        else
            System.out.println("NO");
    }

}
