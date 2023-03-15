#### CPnt는 두 지점을 나타내는 클래스 이다. 
> CPnt p1, p2, p3;
>> 에서 p1의 지점과 p2의 지점이 더해 지는 연산에서
>>> 각각의 h와 w가 더해 질 수 있도록
>>>> 오퍼레이터 오버로딩을 하시오.

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

#### 소감 
> cpp 수업을 통해 어려운 부분들은 반복과 필기를 통해 조금더 쉽게 이해해 볼 수 있었고 깃허브 사용을 오랜만에 하게되면서 지금 까지 했던 과제 들을 정리 해볼 수 있는 기회가 생긴거 같습니다. 깃허브를 다시 잘 활용하여 cpp을 공부하기 쉽게 잘 정리해놓겠습니다. 코딩을 공부하는 것이 어렵다고만 생각하는 것이 아닌 여러번 반복하고 이해가 안되는 부분들은 물어보고 정보를 찾아보는 것을 통해 코딩하는 것에 대해 쉽게 접근 할 수 있을거 같다는 생각을 하게되었습니다. 열심히 cpp공부를 해보겠습니다. 감사합니다. 

