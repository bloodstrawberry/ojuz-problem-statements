역사상 가장 많이 팔린 장난감이 루빅 큐브라는 사실은 많이 알려져 있습니다. 불과 40년 동안 3억 5000만개나 팔렸다고 하네요. 유명한 사업가인 승현이는 루빅 큐브를 단순화한 퍼즐을 만들어 루빅 큐브의 성공을 답습해 많은 돈을 벌고자 합니다. 승현이의 기발한 발명품인 Riddick's Cube는 $1 \times 1$ 크기의 격자들로 구성된 $N \times M$ 직사각형이며, 각 격자는 특정 색으로 색칠되어 있습니다. 규칙은 간단합니다. 한 번 움직일 때마다 하나의 행(가로줄) 또는 하나의 열(세로줄)을 순환적으로 한 칸씩 움직이게 하면 됩니다. (행은 왼쪽 또는 오른쪽, 열은 위 또는 아래로 움직입니다.) 예로 들어, [그림 1]은 2번째 행을 오른쪽으로 움직인 것이고, [그림 2]는 3번째 열을 위로 움직인 것입니다.

<div style="text-align: center; font-size: 15px;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/IZhO13_riddicks/fig1.png"/>
 <p>[그림 1]</p>
</div>

<div style="text-align: center; font-size: 15px;">
 <img src="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/IZhO13_riddicks/fig2.png"/>
 <p>[그림 2]</p>
</div>

각 행이 같은 색을 가진 정사각형들로 구성되어 있거나 각 열이 같은 색을 가진 정사각형들로 구성되어 있다면 퍼즐의 상태가 최종적(최종 상태)이라고 정의하겠습니다.

승현이는 퍼즐이 얼마나 잘 풀리는지 알고 싶어서, 판매 이전에 얼마나 어려운지 시험해 보고자 합니다. 하지만 자신이 직접 풀기는 귀찮으므로 여러분에게 문제를 넘겨주었습니다. 복잡도를 결정하기 위해서 규칙을 단순화합니다: 여러분은 열 몇 개를 움직인 다음 (안 움직여도 됨) 행 몇 개를 움직일 수 있습니다.

여러분에게 Riddick's Cube의 배치 상태 중 하나가 주어졌습니다. 만약 최종 상태가 단순화된 규칙만을 사용해서 만들어질 수 있다면, 복잡도는 최종 상태를 만들 수 있는 최소한의 움직이는 횟수와 같습니다. 불가능하다면, 이 상태는 풀기 엄청나게 어려워서 복잡도가 $100500$과 같게 됩니다. (원래의 규칙대로 풀릴 수도 있지만 너무 복잡해 보입니다.)

복잡도를 구합시다.

### 입력 형식

첫 번째 줄에 두 개의 정수 $N$과 $M$이 공백을 사이로 두고 주어집니다. ($1 \le N, M \le 5$) 다음 $N$개 줄에는 $M$개의 정수가 각각 주어집니다. 각 정수는 퍼즐의 각 칸에 색칠된 색을 나타냅니다. 색 번호는 1 이상 100 이하의 자연수입니다. 주어진 퍼즐 상태가 원래의 규칙을 사용해서 풀리지 않을 수도 있습니다.

### 출력 형식

주어진 퍼즐의 복잡도를 출력합니다.

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th>입력</th>
   <th>출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td style="width: 50%;" class="code-font">2 3<br/>
1 2 1<br/>
2 3 3</td>
   <td class="code-font">2</td>
  </tr>
  <tr>
   <td style="width: 50%;" class="code-font">2 3<br/>
2 2 1<br/>
1 2 1</td>
   <td class="code-font">100500</td>
  </tr>
 </tbody>
</table>
