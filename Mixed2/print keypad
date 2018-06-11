//Given an integer n, using phone keypad find out and print all the possible strings that can be made using digits of input n.

public class Print_keypad {
    public static void main(String args[]){
        printKeypad(34);
    }
    static String[] help={"","","abc","def","ghi","jkl","mno","pqrs","tuv","wxyz"};
    public static void printKeypad(int input){
     helper(input,"");

    }

    private static void helper(int input, String path) {
        if(input==0){
            System.out.println(path);
        }
        for(int i=0;i<help[input%10].length();i++)
        helper(input/10,help[input%10].charAt(i)+path);
    }
}
