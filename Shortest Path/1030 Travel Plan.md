#### [1030 Travel Plan](https://pintia.cn/problem-sets/994805342720868352/exam/problems/994805464397627392)

A traveler's map gives the distances between cities along the highways, together with the cost of each highway. Now you are supposed to write a program to help a traveler to decide the shortest path between his/her starting city and the destination. If such a shortest path is not unique, you are supposed to output the one with the minimum cost, which is guaranteed to be unique.

### Input Specification:

Each input file contains one test case. Each case starts with a line containing 4 positive integers *N*, *M*, *S*, and *D*, where *N* (≤500) is the number of cities (and hence the cities are numbered from 0 to *N*−1); *M* is the number of highways; *S* and *D* are the starting and the destination cities, respectively. Then *M* lines follow, each provides the information of a highway, in the format:

```
City1 City2 Distance Cost
```

where the numbers are all integers no more than 500, and are separated by a space.

### Output Specification:

For each test case, print in one line the cities along the shortest path from the starting point to the destination, followed by the total distance and the total cost of the path. The numbers must be separated by a space and there must be no extra space at the end of output.

### Sample Input:

```in
4 5 0 3
0 1 1 20
1 3 2 30
0 3 4 10
0 2 2 20
2 3 1 20
```

### Sample Output:

```out
0 2 3 3 40
```

---

Dijkstra算法：边有两种代价的情况，另外再使用一个数组记录最小代价的路径，`a[2] = 3` 意为最短路径是由节点 `3` 指向节点 `2` 的，采用方式是因为在求最小代价时**一个点可以有多条出边，但是只能有一条入边**。得到最小代价后深度优先搜索即可。

```java
import java.util.*;
public class Main{
    private static final int INF = Integer.MAX_VALUE / 2;
    private static int[] dis;
    private static int[][] g;
    private static int[][] cost;
    private static int[] sum_cost;
    private static int[] a;
    private static boolean[] visited;
    private static ArrayList<Integer> arraylist = new ArrayList<>();
    
    public static void dfs(int d, int s){
        if(d == s){
            arraylist.add(s);
            return;
        }
        dfs(a[d], s);
        arraylist.add(d);
    }
    
    
    public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        int N = scanner.nextInt(), M = scanner.nextInt(), S = scanner.nextInt(), D = scanner.nextInt();
        dis = new int[N];
        g = new int[N][N];
        cost = new int[N][N];
        sum_cost = new int[N];
        visited = new boolean[N];
        a = new int[N];
        for(int i = 0; i < N; i++){
            Arrays.fill(g[i], INF);
            Arrays.fill(cost[i], INF);
        }
        Arrays.fill(dis, INF);
        Arrays.fill(sum_cost, INF);
        
        for(int i = 0; i < M; i++){
            int temp1 = scanner.nextInt(), temp2 = scanner.nextInt(), temp3 = scanner.nextInt(), temp4 = scanner.nextInt();
            g[temp1][temp2] = temp3;
            g[temp2][temp1] = temp3;
            cost[temp1][temp2] = temp4;
            cost[temp2][temp1] = temp4;
        }
        
        dis[S] = 0;
        sum_cost[S] = 0;
        for(int i = 0; i < N; i++){
            int cur = -1, min = INF;
            for(int j = 0; j < N; j++){
                if(!visited[j] && dis[j] < min){
                    min = dis[j];
                    cur = j;
                }
            }
            if(cur == -1) return;
            visited[cur] = true;
            for(int j = 0; j < N; j++){
                if(visited[j] == false && g[cur][j] != INF){
                    if(g[cur][j] + dis[cur] < dis[j]){
                        dis[j] = dis[cur] + g[cur][j];
                        sum_cost[j] = cost[cur][j] + sum_cost[cur];
                        a[j] = cur;
                    }
                    else if(g[cur][j] + dis[cur] == dis[j] && cost[cur][j] + sum_cost[cur] < sum_cost[j]){
                        sum_cost[j] = cost[cur][j] + sum_cost[cur];
                        a[j] = cur;
                    }
                }
            }
            
        }
        dfs(D, S);
        for(int i = 0; i < arraylist.size(); i++) System.out.print(arraylist.get(i) + " ");
        System.out.println(dis[D] + " " + sum_cost[D]);
        
    }
}
```

