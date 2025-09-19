# Striver
Striver DSA series 


###patterns
### corect way to practice question for placement
```cpp
#include<bits/stdc++.h>
using namespace std;
void print1(int n) {
for(int i = 0; i<n;i++) {
for(int j=0;j<n;j++) {
cout << "*";
}
cout << endl;
}
}

int main() {
int t;
cin >> t;
for(int i = 0; i<t;i++) {
int n;
cin >> n;
print1(n);
}

```

###patern 1
```cpp
*****
*****
*****
*****
*****


   
    void print1(int n){
        for (int i = 0;i < n ;i++){
            for(int j = 0;j < n;j++){
                cout << "*";
            }
            cout << endl ;
        }
    }
```

```cpp

*
**
***
****
*****
   
    void print1(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < i;j++){
                cout << "*";
            }
            cout << endl ;
        }
    }
    
    
```
