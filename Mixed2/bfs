import java.util.*;

public class BFS {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int V = s.nextInt();
        int E = s.nextInt();
        int start=0;
        int end=0;
        int am[][]=new int[V][V];
        for(int i=0;i<E;i++){
            start=s.nextInt();
            end=s.nextInt();
            am[start][end]=1;
            am[end][start]=1;
        }
        printBFS(0,am);
    }

    private static void printBFS(int start, int[][] am) {

        boolean IsVisited[] = new boolean[am.length];
        Queue<Integer> queue = new LinkedList<>();
        queue.add(start);
        IsVisited[0]=true;
        while (!queue.isEmpty()){
            int top=queue.peek();
            queue.remove(top);
            System.out.print(top+" ");
            for(int i=0;i<am.length;i++){
                if(i==top){
                    continue;
                }
                if(am[top][i]==1 && IsVisited[i]==false){
                    queue.add(i);
                    IsVisited[i]=true;
                }
            }
        }
    }
}
