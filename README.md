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

```

```cpp

1
23
456

void print1(int n) {
    int num=1;
for(int i = 1; i<=n;i++) {
    for(int j=1;j<=i;j++) {
        cout << num;
        num = num+1;
    }
    cout << endl;
}
}

```
```cpp

A
AB
ABC
ABCD

void print1(int n) {
for(int i = 0; i<=n;i++) {
    for(int j=0;j<=i;j++) {
        cout << char(65+j);
    }
    cout << endl;
}
}
```

```cpp
ABCD
ABC
AB
A

void print1(int n) {
for(int i = n; i>=0;i--) {
    for(int j=0;j<=i;j++) {
        cout << char(65+j);
    }
    cout << endl;
}
}

```

```cpp
A
BB
CCC
DDDD

void print1(int n) {
for(int i = 0; i<=n;i++)  {
    for(int j=0;j<=i;j++) {
        cout << char(65+i);
    }
    cout << endl;
}
}
 ```

```cpp

   A
  ABA
 ABCBA

void print1(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<n-i-1;j++) {
        cout << " ";
    }
    
    char ch='A';
    int breakpoint = (2*i+1) / 2;
    for(int j=1;j<=2*i+1;j++) {
        cout << ch;
        if(j <= breakpoint ) ch++;
        else ch--;
    }
    
    for(int j=0;j<n-i-1;j++) {
        cout << " ";
    }
    cout << endl ;
    }
}


```

```cpp

E
DE
CDE
BCDE
ABCDE

```


```cpp

**********
****  ****
***    ***
**      **
*        *
*        *
**      **
***    ***
****. ****
**********

int ins = 0;
void print1(int n) {
for(int i = 0; i<n;i++) {
    
    for(int j=1;j<=n-i;j++) {
        cout << "*";
    }
    
    for(int j=0;j<ins;j++) {
        cout << " ";
    }
    
    for(int j=1;j<=n-i;j++) {
        cout << "*";
    }
    ins+=2;
    cout<<endl;

}


ins =8;
for(int i = 1; i<=n;i++) {
    
    for(int j=1;j<=i;j++) {
        cout << "*";
    }
    
    for(int j=0;j<ins;j++) {
        cout << " ";
    }
    
    for(int j=1;j<=i;j++) {
        cout << "*";
    }
    ins -= 2;
    cout << endl;

}
}

```

```cpp

*    *
**  **
******
**  **
*    *

int ins = 0;
void print1(int n) {
    int space = 2*n-2;
    for(int i = 1; i<2*n-1;i++) {
        int stars =i;
        if(i>n) stars= 2*n-i;
    for(int j=1;j<=stars;j++) {
        cout << "*";
    }
    
    for(int j=1;j<=space ;j++) {
        cout << " ";
    }
    
    for(int j=1;j<=stars;j++) {
        cout << "*";
    }
    
    cout<<endl;
    
    if(i<n) space -= 2;
    else space += 2;

}
}
```

```cpp

*****
*   *
*   *
*****


void print1(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<n;j++) {
        if(i==0 || j==0 || i==n-1 || j==n-1){
        cout << "*";
        }
        else cout<<" ";
    }
    cout << endl;
}
}

```

```

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    for (int i = 0; i < n; i++) {
        for (int j = i; j >= 0; j--) {
            cout << char(65 + (n - 1) - j);
        }
        cout << endl;
    }

    return 0;
}


```cpp

#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    for (int i = 0; i < n; i++) {
        for (int j = i; j >= 0; j--) {
            cout << char(65 + (n - 1) - j);
        }
        cout << endl;
    }

    return 0;
}

```


---


# STL

##### popsize and capacity 
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec; //0
    vec.push_back(1);
    vec.push_back(2);
    vec.push_back(3);
    vec.push_back(4);
    vec.push_back(5);
    cout << vec.size() << endl; //3
    cout << vec.capacity() << endl; //4

return 0;

}
```

##### emplace_back 
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec; //0
    vec.push_back(1);
    vec.push_back(2);
    vec.push_back(3);
    vec.push_back(4);
    vec.push_back(5);
    vec.emplace_back(6);
    
    
    for(int val: vec) {
        cout << val << " ";
        
    }
    cout << endl;

return 0;

}
```

##### pop
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec; //0
    vec.push_back(1);
    vec.push_back(2);
    vec.push_back(3);
    vec.push_back(4);
    vec.push_back(5);
    vec.emplace_back(6);
    
    vec.pop_back();
    for(int val: vec) {
        cout << val << " ";
        
    }
    cout << endl;

return 0;

}
```
##### [ ] ( )
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec; //0
    vec.push_back(1);
    vec.push_back(2);
    vec.push_back(3);
    vec.push_back(4);
    vec.push_back(5);
    cout << vec.size() << endl; //3
    cout << vec.capacity() << endl; //4

    cout << "val at idx 2" << vec [2] << or << vec.at(2) << endl;

return 0;

}

```

##### front and back 
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec; //0
    vec.push_back(1);
    vec.push_back(2);
    vec.push_back(3);
    vec.push_back(4);
    vec.push_back(5);
    vec.emplace_back(6);
    
    vec.pop_back();
    for(int val: vec) {
        cout << val << " ";
        
    }
    cout << endl;
    
    cout << "front" << vec.front() << endl;
    cout << "back" << vec.back() << endl;

return 0;

}
```

##### vector begin and erase 
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec = {1, 2, 3, 4, 5};
    vec.erase (vec.begin());
    for(int val: vec) {
        cout << val << " ";
    }
    cout << endl;
    
return 0;

}
```
