<h2>프로그래머스 보석 쇼핑(카카오 코테 문제)</h2><br>
<br>
투 포인터 알고리즘에 대해서 배웠다.<br>
gemshop3가 정답!<br>
처음에 시도하였던 방식은, start(시작점)과 length(길이)를 다루는 두개의 반복문을 이용해서 해당 시작점에서 gems배열의 끝까지<br>
길이를 늘려가며 일일이 set로 변환하고, 이를 비교하여야 하였기에 복잡도가 컸다.<br>
하지만 이렇게 하지 않고, 시작점에서 점점 끝점을 증가시켜 나가다가, 모든 보석의 종류를 포함하는 지점이 나오면 잠시 중지하고,<br>
start지점을 뒤로 옮기고 보석들을 주머니에서(dictionary) 빼보며 한 종류의 보석이라도 개수가 0이 되는 지점까지 start지점을 옮긴다.<br>
이렇게하면 모든 보석들을 포함하면서도 가장 살 보석이 적은 지점을 찾을 수 있고, 이 길이(보석 수)가 여태까지 계산한 것중 가장 작은지 여부를 판단하여 전역변수에 반영하면된다<br>
이 과정을 거치고 나면, 다시 end지점을 끝까지 이동시켜가며 해당 과정을 반복하여 혹시 더 짧은(더 적은 보석을 사는)경우가 있는지 파악해 나가면 된다.
<br><br><br>
소요시간:엄청 오래걸림<br>
체감 난이도:
