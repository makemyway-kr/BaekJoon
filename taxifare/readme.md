<h3>프로그래머스 합승택시요금 문제</h3><br>
<br>
사용 알고리즘: 다익스트라 알고리즘
<br>
다익스트라 알고리즘을 사용하여 각 노드까지 합승할떄까지의 요금과, 택시에서 내려 각자의 집까지 갈 떄의 최저비용(최단거리)를 합해가며 비교해주는 문제이다.<br>
문제 명세 참고:https://programmers.co.kr/learn/courses/30/lessons/72413
<br>
틀렸던 부분: 입력 요금이 100000까지 입력된다하여 max값을 100001로 두고 비교하도록 하였는데, 다시 생각해보니 여러 요금들이 더해질텐데(ex 100000+99000등등)<br>
이럴 경우 max값보다 커서 100001이 리턴되게된다. max를 여유있게 주었어야했다.<br>
입력받은 fares리스트를 가지고 graph 2차원배열을 만들어서 활용하였고, 각 지점까지 dijkstra알고리즘을 돌린 값(최저비용)과 해당 지점에서 각자의 집까지의 dijsktra값을 더해가며<br>
최저비용을 구했다.<br>
그런데 메인 그래프에서 연결되지않은 노드(길이 없는 곳)이 있을 수 있으므로 이를 예외처리 해주기 위하여 minnode에서 방문하지 않은 최단거리 노드가 존재하지 않을경우 ans값이 그대로 0으로 나오는점을<br>
이용하여 예외처리 해주었다.(이 경우, 연결된 모든 길을 검색했음에도 목적지까지의 경로를 구해내지 못하였으므로 최단거리가 존재하지않는, 도달할 수 없는 경로로 취급하여 답을 구하는 과정에서 제외)
<br>

**새로 배운 내용! 파이썬에서 배열을 동적 할당해줄때에는
아래와 같이 [[n(임의의 수) for i in range(column크기)]for k in range(row)]]이런 식으로 선언 해 주면 된다!**
