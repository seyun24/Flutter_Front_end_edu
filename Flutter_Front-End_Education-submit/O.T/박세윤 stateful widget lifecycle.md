# **Stateful Widget Lifecycle**

## 1. widget
플루터에서 위젯이란 플루터에 보이는 모든 요소이다.
+ stateful 
  
  동적인 성질을 가졌으며
  화면에 표시될때 변화 시킬수있다.
  
+ stateless 
  
  정적인 성질을 가졌으며 화면에 표시될때 변화하지 않고 그상태를 유지한다.

## 2. lifecycle
  + state

    state=상태 
    
    말그대로 상태를 나타내며
    
    위젯의 변화의 따른 상태를 
    
    나타내는 객체이다.

  + stateful

    상태가 고정되는 것이 아니라

    변화하는 동적인 성질을 가지고

    있으므로 변화에 따른 state를  
    
    생성하며 stateless에 비해
    다소
    복잡한 라이프 사이클 구조를 가지고 있으며 
    
    아래와 같은 순서로 실행됨

    - CreateState

      state를 생성하고 반환값을 받는 역할을 함
     
  
    - mounted == true

      state가 생성되었다는 것을 알림 >(전달)   mounted 
    - initState()

      초기화 역할을 하며

      처음 시작하고 한번만
      
       호출됨
    - didChangeDependencies()

      위젯이 의존하던 위젯이 변화가 생길때 호출됨

      ex)부모 위젯

      ex)부모-자녀
        
        자녀는 부모에게 의존하며
        부모의 상태에 따라 변화함

    - build()

      화면의 ui를 그리는 역할
      위젯의 상태의 변화를 화면에 표시함
    - didUpdateWidget()

      부모 위젯이 상태가 변경되면서 rebuild 할때 호출됨 
    - setState()

      상태의 변화를 알림
      

      위젯 상태를 갱신 하는 
      
      역할
    - deactivate()

      위젯 트리에서만 state 
      제거될때 호출됨
    - dispose()

      영구적으로 state가 제거 되었을때 호출됨
    - mounted == flase

        state가 완전히 사라졌다는 것을 >(전달 ) > mounted

    
    

  + stateless

    변화가 일어나지 않는 정적인 성질을 가졌 으므로 라이프 사이클 또한 간단함
    
    stateless =상태를 갖고있지  x

    그러므로 state를 생성하지 않음 

    상태의 변화가 거의 없기 때문에
    라이프 사이클이 단순함
    + 생성 > 빌드 > 종료
  

  

  




  
  
  
  

 



  
  
  


