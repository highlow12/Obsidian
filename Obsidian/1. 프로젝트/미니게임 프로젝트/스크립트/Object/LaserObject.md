# 함수
## shootLaser
```C#
protected virtual void shootLaser(Vector3 origin, Vector3 dir)
```
레이저를 origin에서 dir 방향으로 발사합니다
레이저의 경로에 LaserObject를 상속받는 오브젝트가 있을 경우
그 오브젝트의 [[LaserObject#hitLaser| hitLaser]]를 호출합니다 함수의

예시
```c#
// 레이저를 자신의 위치에서 자신의 앞 방향으로 발사합니다
shootLaser(transform.position, transform.forward)
```
## hitLaser
```c#
public virtual void hitLaser(Vector3 direction)
```