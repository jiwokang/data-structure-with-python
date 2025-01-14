# 트리(tree)

> 본 포스팅은 한국외대 컴퓨터공학부 신찬수 교수님의 "[자료구조 - Data Structures with Python](https://www.youtube.com/playlist?list=PLsMufJgu5933ZkBCHS7bQTx0bncjwi4PK)" 중 20강 "[트리(tree)](https://youtube.com/watch?v=w-1w4ood7Bc)" 강의를 정리한 노트입니다.

## 순차적 자료구조

배열, 인덱스, i = 0, 1..., 연결리스트 링크(next, prev) 등이 있는 자료구조.

## 트리

부모, 자식 노드를 갖고 데이터를 표현하는 자료구조. 자식이 하나만 있거나 없는 경우를 연결리스트라고 부른다. 연결리스트는 트리의 특별한 유형이라고 할 수도 있다.

자식이 최대 두 개인 트리를 이진 트리(binary tree)라고 부른다. 삼진 트리도 가능하지만 이진 트리가 가장 간단하고 많이 쓰이는 구조이다.

- 노드: 각각의 요소
- 링크: 노드를 연결하는 선, 엣지라고 부르기도 한다.
- 루트 노드: 최고의 조상
- 리프 노드(leaf node): 자식이 하나도 없는 노드
- 레벨: 루트 노드가 레벨 0. 루트로부터 각각 레벨 1, 2, 3...
- 높이: 루트부터 리프까지 가장 깊은 레벨까지의 통과하는 노드의 수. 레벨 수 == 트리 높이
- 경로(path): 노드 v에서 w까지 거치는 노드들. 출발노드-경유노드-도착노드
- 경로길이(path length): 경로에 포함되는 링크(엣지)의 개수
- 자식(child) 노드와 부모(parent) 노드, 형제 노드

## 구현

```txt
    a
  /   \
 b     c
  \   / \
   d e  f
  /\ /
 h i g
```

- 표현법 1) 리스트: `A = [a, b, c None, d, e, f, None, None, h, i, g]`
- 
<img width="605" alt="image" src="https://user-images.githubusercontent.com/91314143/168820209-b540f9aa-218b-4952-bebe-9a2cc8af0d94.png">

- 표현법 2) 리스트(재귀적): `[a, [ [b, [], [d, [], []] ], [c, [e, [], []] [f, [], [] ]]]`
- 표현법 3) 노드 클래스를 이용: 다음에 다시 살펴볼 것
