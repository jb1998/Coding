import java.util.Arrays;

public class MinAbsDif {

    public static int minAbsoluteDifference(int input[]) {

        Arrays.sort(input);
        int min=Integer.MAX_VALUE;
        for(int i=0;i<input.length-1;i++){
            if(input[i+1]-input[i]<min){
                min=input[i+1]-input[i];
            }
        }
        return min;
    }
}
