# Unity-c#-script

## 배열

* 배열 선언: 배열을 선언하고, 이어서 new를 사용해 배열에 필요한 박스 수를 지정해야 한다.

```csharp
float[] arr = new float[5]
```

* 배열의 길이: 배열에 지정한 박스 수

```csharp
arr.Length
```

## 클래스
게임에서 서로 관계가 있는 클래스 변수(멤버 변수), 클래스 함수(멤버 함수)들을 합쳐 스크립트를 한번에 관리한다.
```csharp
// 데이터 저장하는 data type 제공
using System.Ccollections;
using System.Collections.Generic;
// 유니티 동작에 필요한 기능 제공
using UnityEngine;

public class Player
{
    // 멤버 변수
    private int hp = 100;
    // 멤버 함수
    public void Attack()
    {
        Debug.Log(this.power + "대미지를 입혔다.");
    }
}

public class Test : MonoBehaviour
{
    Player sang = new Player();
    sang.Attack();
}
```
위와같이 Player형의 sang변수에는 Player()를 대입하는데 이를 Player형의 실체인 <span style="color: red">인스턴스</span>라고 한다. <span style="color: red">new</span> 키워드 다음에 <span style="color: red">클래스명()</span>을 쓴다.

* this 키워드: 자신의 인스턴스가 갖는 변수
* 상속: MonoBehaviour, 유니티가 미리 준비한 MonoBehaviour 클래스의 기능을 Player 클래스에 집어넣겠다고 선언하는 과정
* MonoBehaviour: 게임 오브젝트를 구성하는 기본 기능을 멤버 변수, 멤버 함수로 준비한 클래스로 게임 오브젝트에 붙여 실행하는 스크립트는 MonoBehaviour 클래스를 상속해야 한다.