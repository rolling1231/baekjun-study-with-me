### DFS(깊이 우선 탐색)
재귀를 통해 구현
방문한 노드를 체크하여 재방문 하지 않음

 
``` C++
void dfs(int from) {
	cout << from << " ";
	visited[from] = 1;
	for (int i = 1; i <= N; i++) {
		if (graph[from][i] == true && visited[i] == 0) {
			//cout << i << ' ';
			visited[i] = 1;
			dfs(i);
		}
	}
}
```
