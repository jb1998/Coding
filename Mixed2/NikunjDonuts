import java.util.Arrays;
import java.util.Scanner;

public class NikunjDonuts {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n=sc.nextInt();
        int arr[]=new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        Arrays.sort(arr);
        int power=0;
        long ans=0;
        for(int i=n-1;i>=0;i--){
            ans+=Math.pow(2,power)*arr[i];
//            System.out.println(ans+ " "+Math.pow(2,power));
            power++;
        }
        System.out.println(ans);
    }
}
