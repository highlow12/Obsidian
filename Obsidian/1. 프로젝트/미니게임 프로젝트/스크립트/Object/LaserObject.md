[[GridObject]]를 상속받습니다.
레이저와 상호작용하는 오브젝트들이 이 코드를 상속합니다
# 함수
## shootLaser
```C#
protected virtual void shootLaser(Vector3 origin, Vector3 dir)
```
레이저를 origin에서 dir 방향으로 발사합니다
레이저의 경로에 LaserObject를 상속받는 오브젝트가 있을 경우
그 오브젝트의 [[LaserObject#hitLaser|hitLaser]]를 호출합니다 함수의 인수로는 dir을 넣습니다

예시
```c#
// 레이저를 자신의 위치에서 자신의 앞 방향으로 발사합니다
shootLaser(transform.position, transform.forward)
```
## hitLaser
```c#
public virtual void hitLaser(Vector3 dir)
```
레이저에 피격됬다면 호출됩니다
실행되는 코드는 오브젝트마다 다르므로 상속된 코드에서 오버라이딩 해주십시오
