import java.util.*;

public class PermutationSwaps {

    static boolean[] Isvisited;

    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        int iterate = 0;
        while (iterate++ < t) {
            int n = sc.nextInt();
            int m = sc.nextInt();
            int arr1[] = new int[n+1];
            int arr2[] = new int[n+1];
            for (int i = 1; i <= n; i++) {
                arr1[i] = sc.nextInt();
            }

            for (int i = 1; i <= n; i++) {
                arr2[i] = sc.nextInt();
            }
            int gr[][] = new int[n+1][n+1];
            for (int i = 0; i < m; i++) {
                int start = sc.nextInt();
                int end = sc.nextInt();
                gr[start][end] = 1;
                gr[end][start] = 1;
            }
            Isvisited = new boolean[n+1];


            ArrayList<ArrayList<Integer>> ans = new ArrayList<>();
            for (int i = 1; i <= n; i++) {
                if (!Isvisited[i]) {
                    ArrayList<Integer> arr = getConnected(gr, i);
                    ans.add(arr);
                }
            }
            if(ans.size()>0) {


                boolean went = false;
                for (int i = 0; i < ans.size(); i++) {

                    HashMap<Integer, Integer> has = new HashMap<>();
                    for (int j = 0; j < ans.get(i).size(); j++) {
                        has.put(j, arr1[ans.get(i).get(j)]);
                    }
                    for (int j = 0; j < ans.get(i).size(); j++) {
                        if (!has.containsValue(arr2[ans.get(i).get(j)])) {
                            went = true;
                            break;
                        }

                    }
                    if (went)
                        break;
                }

                if (went)
                    System.out.println("NO");
                else
                    System.out.println("YES");
            }else{
                System.out.println("NO");
            }
        }
    }

    private static ArrayList<Integer> getConnected(int[][] gr, int start) {
        ArrayList<Integer> arrayList = new ArrayList<>();
        Queue<Integer> queue = new LinkedList<>();
        queue.add(start);
        arrayList.add(start);
        Isvisited[start] = true;
        while (!queue.isEmpty()) {
            int top = queue.peek();
            queue.remove(top);
            for (int i = 0; i < gr.length; i++) {
                if (gr[top][i] == 1 && Isvisited[i] == false) {
                    Isvisited[i] = true;
                    arrayList.add(i);
                    queue.add(i);
                }
            }
        }
        return arrayList;
    }
}
