 # Striver
Striver DSA series 


### patterns
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
}
```

### patern 1
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

```cpp

0
01
012
0123
01234

void print1(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < i;j++){
                cout << j << " " ;
            }
            cout << endl ;
        }
    }

```


```cpp

1
22
333
4444
55555

void print1(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < i;j++){
                cout << i << " " ;
            }
            cout << endl ;
        }

```

```cpp

*****
****
***
**
*


    void print1(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < n-i ;j++){
                cout << "*" << " " ;
            }
            cout << endl ;
        }
    }

```

```cpp

12345
1234
123
12
1

void print1(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<n-i;j++) {
        cout << j << " ";
        
    }
    cout << endl;
}
}

```

```cpp

    *
   ***
  *****

void print1(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<n-i-1;j++) {
        cout << " ";
    }
    for(int j=0;j<2*i+1;j++) {
        cout << "*";
    }
    for(int j=0;j<n-i-1;j++) {
        cout << " ";
    }
    cout << endl ;
    }
```

 ```cpp

*****
_***
__*
void print1(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<i;j++) {
        cout << " ";
    }
    for(int j=0;j<2*n-(2*i + 1);j++) {
        cout << "*";
    }
    for(int j=0;j<i;j++) {
        cout << " ";
    }
    cout << endl ;
    }

```


```cpp
*****
_***
__*
  *
 ***
*****

void print1(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<i;j++) {
        cout << " ";
    }
    for(int j=0;j<2*n-(2*i + 1);j++) {
        cout << "*";
    }
    for(int j=0;j<i;j++) {
        cout << " ";
    }
    cout << endl ;
    }
}

void print2(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<n-i-1;j++) {
        cout << " ";
    }
    for(int j=0;j<2*i+1;j++) {
        cout << "*";
    }
    for(int j=0;j<n-i-1;j++) {
        cout << " ";
    }
    cout << endl ;
    }
}
 ```


```cpp

*
**
***
**
*



void print1(int n) {
for(int i = 1; i<=2*n-1;i++) {
    int stars = i;
    if(i>n) stars = 2*n-i;
    
    for(int j = 1; j<= stars ; j++){
            cout << "*";
        
    }
     cout << endl;   
    }

}

```

```cpp

0
10
010

void print1(int n) {
    int start =1;
for(int i = 0; i<n;i++) {
    if(i%2==0) start = 1;
    else start = 0;
    for(int j=0;j<i;j++) {
        cout << start;
        start=1-start;
    }
    cout << endl;
}
}

```

```cpp

1    1
12  21
123321


void print12(int n) {
int space 2* (n-1);
for(int i=1;i<=n;i++) {
// numbers 
for(int j=1;j<=1;j++) {
cout << j;
// space
for(int j=1;j<=space;j++) {
cout <<" ";
}
// numbers
for(int j = i;j>=1;j-) {
cout << j;
cout << endl;
space -= 2;
}
}


