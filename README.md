#CPnt는 두 지점을 나타내는 클래스 이다. 
CPnt p1, p2, p3;
에서 p1의 지점과 p2의 지점이 더해 지는 연산에서
각각의 h와 w가 더해 질 수 있도록
오퍼레이터 오버로딩을 하시오.

~~~
#include<iostream>
using namespace std;
class CPnt{
    int w, h;
    public:
    CPnt(int _w, int _h){
        w=_w;
        h=_h;
    }
    CPnt(){w=0;h=0;}
    void pr(){
        cout << w * h <<endl;
    }
    void prpt(){
        cout << w << " " << h <<endl;
    }
    CPnt operator+(CPnt r){
        CPnt t;
        t.w = w + r.w;
        t.h = h + r.h;
        return(t);
    }
};
int main(){
    CPnt p1(1,1), p2(2,2), p3;
    //p3 = p1.operator+(p2);
    p3 = p1+p2;
    p3.prpt();
    p3.pr();
    return 0;
}
~~~ 
