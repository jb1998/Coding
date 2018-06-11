//Given an integer n, using phone keypad find out all the possible strings that can be made using digits of input n.
//        Return empty string for numbers 0 and 1.

public class Return_keypad {
    static String[] help={"","","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};
    public static String[] keypad(int n){
     if(n==0){
         String str[]=new String[1];
         str[0]="";
         return str;
     }
     String small_output[]=keypad(n/10);
     String fetch=help[n%10];
     String big_output[]=new String[small_output.length*fetch.length()];
     int k=0;
     for(int i=0;i<small_output.length;i++){
         for(int j=0;j<fetch.length();j++){
             big_output[k]=small_output[i]+fetch.charAt(j);
             k++;
         }
     }
     return big_output;
    }

    public static void main(String args[]){
        String str[]=keypad(483);
        for(int i=0;i<str.length;i++){
            System.out.println(str[i]);
        }
    }
}
