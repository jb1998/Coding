public class MinSteps {
    public static int countStepsTo1(int n){

     int a1=Integer.MAX_VALUE,a2=Integer.MAX_VALUE,a3=Integer.MAX_VALUE;
     a1=1+countStepsTo1(n-1);
     if(n%2==0)
         a2=countStepsTo1(n/2);
     if(n%3==0)
         a3=countStepsTo1(n/3);
     return Math.min(Math.min(a1,a2),a3);
    }

}
