public class parenthesis {
public static void main(String args[]){
    printWellFormedParanthesis(3);
}
    public static void printWellFormedParanthesis(int n) {

       helper(n,n,"");
    }

    public static void helper(int n1,int n2, String path) {
     if(n1==0 && n2==0){
         System.out.println(path);
         return;
     }
     if(n1>0){
         helper(n1-1,n2,path+"(");
     }
     if(n1<n2){
         helper(n1,n2-1,path+")");
     }
    }
}
