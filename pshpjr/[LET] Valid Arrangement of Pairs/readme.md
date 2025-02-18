[Valid Arrangement of Pairs](https://leetcode.com/problems/valid-arrangement-of-pairs/description/?envType=daily-question&envId=2025-02-03)

## 문제 유형

오일러 경로 (한붓 그리기)

## 배울점

- 오일러 경로 찾는 알고리즘. dfs로 탐색하면서 사용한 엣지를 지우고, 지금 노드의 엣지가 0이 되면 그 노드를 경로에 넣는다. 오일러 경로는 같은 노드가 2개 이상 들어갈 수 있다. 이후 경로를 뒤집는다.
- 경로에 들어가는 애는 탐색이 완료된 애. 시작 노드가 가장 마지막에 들어감. 
- 처음에 해밀턴 경로 (모든 노드를 한 번만 방문) 문제로 생각했는데, 해밀턴 경로는 np 완전 문제라고 함. 어지간해선 못 볼 듯? 나오면 완전탐색
- 방향 그래프와 무방향 그래프의 시작 노드 찾는 방법이 다름. 방향에선 진입이 진출보다 1개 많으면 출발점임. 무방향에선 엣지 개수가 홀수인 애.
- 이 문제는 오일러 경로 보장하지만, 보장하지 않는 경우 무방향에선 엣지 개수가 홀수인 애 2개 초과 / 방향에선 출발점 후보가 2개 이상 / 목적지 후보가 2개 이상 있으면 안 됨
- HashMap 순회하는 방법에 관한 부분도 알아 둘 것. for(int i = 0 ; i< map.size())는 올바른 탐색 방법이 아님. 