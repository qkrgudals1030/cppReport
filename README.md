/*
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
*/cpp
