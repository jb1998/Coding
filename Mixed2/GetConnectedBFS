import java.util.*;

public class GetConnectedBFS {
    static boolean[] is_visited;
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int V = s.nextInt();
        int E = s.nextInt();
        int arr[][]=new int[V][V];
        for (int i=0;i<E;i++){
            int start=s.nextInt();
            int end=s.nextInt();
            arr[start][end]=1;
            arr[end][start]=1;
        }
        ArrayList<ArrayList<Integer>> final_arr=new ArrayList<>();
        is_visited=new boolean[V];
        for(int i=0;i<arr.length;i++){
            if(is_visited[i]==false){
                ArrayList<Integer> arrayLists=getConnected(arr,i);
                Collections.sort(arrayLists,Collections.reverseOrder());
                final_arr.add(arrayLists);
            }

        }
        for(int i=0;i<final_arr.size();i++){
            for(int j=final_arr.get(i).size()-1;j>=0;j--){
                System.out.print(final_arr.get(i).get(j)+" ");

            }
            System.out.println();
        }
    }
    private static ArrayList<Integer> getConnected(int[][] gr, int start) {
        ArrayList<Integer> arrayList = new ArrayList<>();
        Queue<Integer> queue = new LinkedList<>();
        queue.add(start);
        arrayList.add(start);
        is_visited[start] = true;
        while (!queue.isEmpty()) {
            int top = queue.peek();
            queue.remove(top);
            for (int i = 0; i < gr.length; i++) {
                if (gr[top][i] == 1 && is_visited[i] == false) {
                    is_visited[i] = true;
                    arrayList.add(i);
                    queue.add(i);
                }
            }
        }
        return arrayList;
    }
}
