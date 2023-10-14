# 레이저 피격시
LaserMirror의 transform.localPosition에서 레이저 발사 방향으로 레이저 발사
# 레이저 발사 조건
레이저 피격시
# 레이저 발사 방향
피격된 레이저의 transform.forward와 LaserMirror의 transform.forward의 방향이 수직이라면, 피격된 레이저의 transform.left 방향
평행이라면, 피격된 레이저의 transform.right 방향
그리고 피격된 레이저의 transform.forward 방향으로 레이저 발사

## 공통 기능
![[공통 기물 기능]]
