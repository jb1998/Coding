public class Subset_sum_k {

    public static void printSubsetsSumTok(int input[], int k) {
     int arr[]=new int[0];
        helper(input,0,k,arr);
    }

    private static void helper(int[] input,int position, int k, int[] arr) {
       if(position>=input.length) {

           if (k == 0) {
               for (int i = 0; i < arr.length; i++) {
                   System.out.print(arr[i] + " ");
               }
               System.out.println();
               return;
           }
           else
               return;
       }
        int arr2[]=new int[arr.length+1];
        int j=0;
        for(;j<arr.length;j++){
            arr2[j]=arr[j];
        }

        arr2[j]=input[position];
        helper(input,position+1,k,arr);
        helper(input,position+1,k-input[position],arr2);
    }

    public static void main(String args[]){
        int temp[]={5, 12, 3 ,17 ,1 ,18 ,15 ,3 ,17};
        printSubsetsSumTok(temp,6);
    }
}
