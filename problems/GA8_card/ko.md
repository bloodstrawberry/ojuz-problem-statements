<!-- 
여자친구가 없는 승현이는 여름방학을 혼자 쓸쓸히 보내다가 수찬이로부터 카드를 $n$장 받게 되었습니다.

이 카드들의 앞면에는 서로 다른 2,222 이하의 자연수가 적혀 있고 뒷면에는 아무 것도 없습니다. $i$($1 \le i \le n$)번째 카드에 적힌 수는 $c_{i}$입니다.

승현이는 이들을 바닥에 뒷면이 보이도록 엎어 놓습니다. 승현이는 바닥에 카드가 한 장이 남을 때까지 다음과 같은 행동을 반복합니다.

1. 승현이는 마음에 드는 카드 두 장을 뒤집어 봅니다. 이 때, 두 카드는 서로 달라야 합니다.
2. 승현이는 더 작은 수가 적힌 카드를 손으로 가져옵니다.
3. 손으로 가져오지 않은 카드는 다시 뒷면이 보이도록 뒤집어 놓습니다.

바닥에 카드가 한 장이 남게 되면, 승현이는 손에 들고 있는 카드들에 적힌 수의 합을 구합니다.

전혀 말도 안 되어 보이지만, 수찬이는 이 수들의 합이 승현이가 미래에 만들 여자친구와 보내게 될 초 수라고 말했습니다. 따라서 순진한 승현이는 합을 최대화하려고 합니다. 승현이를 도와주세요.
-->

승현이는 앞면과 뒷면이 있는 카드 $n$장을 가지고 있습니다. 각 카드의 앞면에는 1 이상 2222 이하의 정수가 적혀 있으며, 이 수는 카드마다 서로 다릅니다. 각 카드의 뒷면에는 동물 그림이 그려져 있으며, 이 그림 역시 카드마다 서로 다릅니다.

<div style="text-align: center;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/GA8_card/pic1.png">
 <p><small>가능한 카드의 예시입니다. 왼쪽 그림은 앞면, 오른쪽 그림은 뒷면입니다.</small></p>
</div>

승현이는 카드들을 바닥에 뒷면이 보이도록 일렬로 늘어 놓고, 차례대로 1 이상 $n$ 이하의 자연수 번호를 붙였습니다. 이 중 $i$번 카드의 앞면에 적혀 있는 수를 $c_{i}$로 둡시다. 승현이는 바닥에 카드가 정확히 한 장 남을 때까지 아래와 같은 행동을 반복합니다.

1. 승현이는 마음에 드는 서로 다른 카드 두 장을 앞면이 보이도록 뒤집어 봅니다.
2. 승현이는 앞면에 더 작은 수가 적혀 있는 카드를 주머니 속에 넣고, 더 큰 수가 적혀 있는 카드는 다시 바닥에 뒷면이 보이도록 내려놓습니다.
3. 카드가 두 장 이상 남았다면 1번으로 돌아갑니다. 카드가 정확히 한 장 남았다면, 승현이는 주머니 속에 있는 카드들을 꺼내 앞면에 적혀 있는 수들의 합을 구합니다.

승현이는 큰 수가 좋아서, 마지막에 주머니 속에 들어있는 카드들에 적혀 있는 수들의 합을 가능한 한 크게 하고자 합니다. (뒷면에 그려진 동물 그림이 서로 다르므로 방법만 알고 있다면 충분히 가능합니다!) 승현이를 도와주세요.

### 입력 형식

첫 번째 줄에 카드의 수를 나타내는 자연수 $n$이 주어집니다.

두 번째 줄에 $c_{1}, c_{2}, \cdots, c_{n}$이 공백을 사이에 두고 차례대로 주어집니다.

### 출력 형식

첫 번째 줄에 가능한 최대 합을 출력합니다.

### 부분문제

<div class='table-responsive'>
<table class='table table-condensed table-bordered'>
<thead>
 <tr>
  <th class="col-sm-2 col-md-2 col-lg-2">부분문제</th>
  <th class="col-sm-2 col-md-2 col-lg-2">점수</th>
  <th class="col-sm-3 col-md-3 col-lg-3">$n$</th>
  <th>추가 제약 사항</th>
 </tr>
</thead>
<tbody>
 <tr>
  <td>1</td>
  <td>5</td>
  <td>$n = 1$</td>
  <td>-</td>
 </tr>
 <tr>
  <td>2</td>
  <td>15</td>
  <td>$n = 2$</td>
  <td>-</td>
 </tr>
 <tr>
  <td>3</td>
  <td>10</td>
  <td>$n =$ $2,222$</td>
  <td>-</td>
 </tr>
 <tr>
  <td>4</td>
  <td>25</td>
  <td>$n \le$ $2,222$</td>
  <td>모든 $1 \le i \le n$에 대하여 $c_{i} = i$</td>
 </tr>
 <tr>
  <td>5</td>
  <td>45</td>
  <td>$n \le$ $2,222$</td>
  <td>-</td>
 </tr>
</tbody>
</table>
</div>

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 1</th>
   <th style="width: 50%;">출력 1</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">2<br>3 4</td>
   <td class="code-font">3</td>
  </tr>
 </tbody>
</table>

이 예제에서 가능한 경우는 한 가지 뿐입니다.

승현이는 3이 적힌 카드와 4가 적힌 카드를 뽑게 되고, 3이 적힌 카드를 갖고 나면 남은 카드가 한 장밖에 없으므로 답은 3이 됩니다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 2</th>
   <th style="width: 50%;">출력 2</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">3<br>1 3 5</td>
   <td class="code-font">4</td>
  </tr>
 </tbody>
</table>

이 예제에서 가능한 경우는 세 가지입니다.

* 승현이가 처음에 1이 적힌 카드와 3이 적힌 카드를 뽑고, 다음에 3이 적힌 카드와 5가 적힌 카드를 뽑았을 경우 답은 1+3=4가 됩니다.
* 승현이가 처음에 1이 적힌 카드와 5가 적힌 카드를 뽑고, 다음에 3이 적힌 카드와 5가 적힌 카드를 뽑았을 경우 답은 1+3=4가 됩니다.
* 승현이가 처음에 3이 적힌 카드와 5가 적힌 카드를 뽑고, 다음에 1이 적힌 카드와 5가 적힌 카드를 뽑았을 경우 답은 3+1=4가 됩니다.

따라서 답은 4가 됩니다.

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력 3</th>
   <th style="width: 50%;">출력 3</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">20<br>1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20</td>
   <td class="code-font">190</td>
  </tr>
 </tbody>
</table>