<h2>프로그래머스 여행경로 문제</h2>
<br>
DFS를 이용하여 해결. With python<br>
이 문제는 항공권 리스트가 주어졌을때, 처음 출발지에서 출발하여 모든 항공권을 사용할때 까지의 여행경로를 return 하는 문제이다.<br>
한 공항에서 출발할 수 있는 항공권이 두개 있을 때, 도착지의 알파벳 순서가 앞인 곳을 우선으로 하여 탐색한다.<br>
깊이우선 탐색을 이용하여 해결하였다. 시작하기 전에 항공권 도착지의 이름 알파벳을 기준으로 sort를 진행하였다(lambda이용)<br>
이후 next함수를 재귀적으로 실행해 나가게 되는데, 티켓 목록중에서 전역변수 used_ticket(사용한 티켓의 인덱스 번호 리스트)<br>
에 존재하지 않는 항공권을 순서대로 선택해가며 next함수를 실행하게 되고, 만약 실행하던 중 <br>항공권이 남아있음에도 불구하고 출발지에서 쓸 수 있는 항공권이 없다면 잘못된 경로임으로 -1을 리턴하고 나오도록 한다. -1을 return할 때에는 사용한 항공권 목록에서 도로 이를 지우고,<br>
다시 항공권을 탐색하도록한다. 만약 기존에 선택했던 항공권 말고 다른 사용가능한 항공권이 없다면, 이 또한 -1을 리턴하고 빠져나오도록 하였다.
