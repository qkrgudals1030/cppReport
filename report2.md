### 1. friend를 활용하는 [클래스]의 예를 하나 만드시오.

~~~

#include <iostream>  // friend functions
using namespace std;
class CTest {
  	int x;
  public:
    CTest(int a=2):x(a){}
    friend int main();
};
int main () {
    CTest me;
    cout << me.x << endl;
    return 0;
}

~~~

### 2. [클래스]에서 static을 활용하는 예를 하나 보이시오.

~~~
#include <iostream>
using namespace std;
class Cnt {
public:
    static int cnt;
    void inc() { cnt++; }
};
// count를 초기화 하시오.
int Cnt::cnt=0;
int main() {
    Cnt c;
    c.inc();
    c.inc();
    c.inc();
    cout << "횟수: " << Cnt::cnt << endl;
    return 0;
}

~~~

### 3. Poly로 부터 w, h를 상속받고,사각형의 면적을 구하는 코딩을 하시오. 포인터를 활용하여 화면에 출력하시오.

~~~

#include<iostream>
using namespace std;
class CPoly{
protected:
	int w, h;
};
class CRect : public CPoly{
public:
	CRect(){ w=2; h=3;}
	int Area(){ cout << w*h;}	
};
int main(){
	CRect r;
	CRect* p = &r;
	p->Area();
	//r.Area();
}

~~~

### 4. 소감
> 오늘 수업에서는 c++의 다양한 특징들에 대해 공부하였는데 이를 한번에 외우려고 하는것이 아니라 기록을 해두고 여러번 반복해보면서 해야 잘외울 수 있을거 같다고 생각을 하게 되었습니다. 이를 통해 깃허브를 조금더 활용해 볼려고 하고 있습니다. 여러번 반복학습을 통해 다음 수업에는 코딩을 할때 참고 하지 않고 코딩할 수 있도록 열심히 해보겠습니다. 모르는 것이 있으면 카페와 교수님 친구들을 통해 해결하겠습니다. c++ 화이팅 !!!!

