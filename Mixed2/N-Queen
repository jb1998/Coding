//You are given N, and for a given N x N chessboard,
// find a way to place N queens such that no queen can
// attack any other queen on the chess board.
// A queen can be killed when it lies in the same row, or same column, or the same diagonal of any of the other queens.
// You have to print all such configurations.


public class NQueen {

    public static void placeNQueens(int n){
        int ans[][]=new int[n][n];
        helper(n,ans,0);
    }

    private static void helper(int n, int[][] ans, int row) {
        if(row==n){
            for(int i=0;i<n;i++){
                for(int j=0;j<n;j++){
                    System.out.print(ans[i][j]+" ");
                }
            }
            System.out.println();
            return;
        }
         for(int i=0;i<n;i++){
         if(isPossible(row,i,ans,n)){
             ans[row][i]=1;
             helper(n,ans,row+1);
             ans[row][i]=0;
         }
        }
    }

    private static boolean isPossible(int row, int i, int[][] ans, int n) {
        // in row
        for(int k=0;k<n;k++){
            if(ans[row][i]==1)
                return false;

        }
        // in column
        for(int k=0;k<n;k++){
            if(ans[k][i]==1)
                return false;
        }
        // main diagonal
        for(int k=row,l=i;k>=0;k--,l--){
            if(l<0)
                break;
            if(ans[k][l]==1)
                return false;
        }
        // other diagonal
        for(int k=row,l=i;k>=0;k--,l++){
            if(l>=n)
                break;
            if(ans[k][l]==1)
                return false;
        }
        return true;
    }

    public static void main(String args[]){
        placeNQueens(4);
    }
}
