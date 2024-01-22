# #싱글톤
# 변수
## private
- `int allReceverNum`: 스테이지 내의 모든 리시버 개수
- `int laserRecevedNum`: 레이저에 맞은 리시버의 개수
# 메소드
## public
- `void addRecever()`: 모든 리시버가 시작할 때 이 메소드를 호출한다
- `void laserReceve()`: 모든 리시버가 레이저를 맞았을 때 이 메소드를 호출한다
## private
- `void clearGame()`: `allReceverNum == laserRecevedNum` 일때 호출되어 스테이지가 끝남을 알린다