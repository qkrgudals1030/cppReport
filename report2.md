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


