# PATTERNS
1. - [overview](#overview)

 # overview    
```
--------------------------- ROW 1 (1–6) ---------------------------

1. *****       2. *        3. 1        4. 1        5. ****     6. 1234
   *****          **          12          22          ***         123
   *****          ***         123         333         **          12
   *****          ****        1234        4444        *           1



--------------------------- ROW 2 (7–12) ---------------------------

7.    *        8. *****    9.    *     10. *       11.  1        12. 1****
     ***           ***          ***        **           01           12***
    *****           *          *****       ***          101          123**
                                ***        ****         0101         1234*
                                 *         ***                       12345                                 
                                           **
                                           *


--------------------------- ROW 3 (13–18) ---------------------------

13. 1        14. A        15. ABCDE      16. A        17.    A     18. D
    23           AB           ABC            BB             ABA        CD
    456          ABC          AB             CCC           ABCBA       BCD
    78910        ABCD         A              DDDD         ABCDCBA      ABCD



--------------------------- ROW 4 (19–22 + fillers) ---------------------------

19. *********      20. *     *        21. ****       22. 4 4 4 4 4 4 4
    **** ****          **   **            *  *           4 3 3 3 3 3 4
    ***   ***          *** ***            *  *           4 3 2 2 2 3 4
    **     **          *******            ****           4 3 2 1 2 3 4
    *       *          *** ***                           4 3 2 2 2 3 4
    **     **          **   **                           4 3 3 3 3 3 4
    ***   ***          *     *                           4 4 4 4 4 4 4
    **** ****                                                
    *********                                                

```
```cpp
#include <iostream>
using namespace std;

int main() {
    vector<int> vec ={3,5,1,8,2};

    sort(vec.begin(), vec.end(), greater <int>());

    for(int val: vec){
        cout << val<< " ";
    }
    cout << endl;
    return 0;
}
```

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

### patern 2
```cpp
*
**
***
****
*****
   
    void print2(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < i;j++){
                cout << "*";
            }
            cout << endl ;
        }
    }
    
    
```
### patern 3
```cpp

0
01
012
0123
01234

void print3(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < i;j++){
                cout << j << " " ;
            }
            cout << endl ;
        }
    }

```

### patern 4
```cpp

1
22
333
4444
55555

void print4(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < i;j++){
                cout << i << " " ;
            }
            cout << endl ;
        }

```

### patern 5
```cpp

*****
****
***
**
*


    void print5(int n){
        for (int i = 0;i <= n ;i++){
            for(int j = 0;j < n-i ;j++){
                cout << "*" << " " ;
            }
            cout << endl ;
        }
    }

```

### patern 6
```cpp

12345
1234
123
12
1

void print6(int n) {
for(int i = 0; i<n;i++) {
    for(int j=0;j<n-i;j++) {
        cout << j << " ";
        
    }
    cout << endl;
}
}

```

### patern 7
```cpp

    *
   ***
  *****

void print7(int n) {
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

### patern 8
 ```cpp

*****
_***
__*
void print8(int n) {
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
]

```

### patern 9
```cpp
*****
_***
__*
  *
 ***
*****

void print9(int n) {
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

void print9(int n) {
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

### patern 10
```cpp

*
**
***
**
*



void print10(int n) {
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

### patern 11
```cpp

0
10
010

void print11(int n) {
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
### patern 12
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

### patern 13
```cpp

1
23
456

void print13(int n) {
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

### patern 14
```cpp

A
AB
ABC
ABCD

void print14(int n) {
for(int i = 0; i<=n;i++) {
    for(int j=0;j<=i;j++) {
        cout << char(65+j);
    }
    cout << endl;
}
}
```
### patern 15
```cpp
ABCD
ABC
AB
A

void print15(int n) {
for(int i = n; i>=0;i--) {
    for(int j=0;j<=i;j++) {
        cout << char(65+j);
    }
    cout << endl;
}
}

```
### patern 16
```cpp
A
BB
CCC
DDDD

void print16(int n) {
for(int i = 0; i<=n;i++)  {
    for(int j=0;j<=i;j++) {
        cout << char(65+i);
    }
    cout << endl;
}
}
 ```

### patern 17
```cpp

   A
  ABA
 ABCBA

void print17(int n) {
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

### patern 18
```cpp
E
DE
CDE
BCDE
ABCDE

void print18(int n) {
    for(int i = 0; i < n; i++) {
        for(char ch = char('E' - i); ch <= 'E'; ch++) {
            cout << ch << " ";
        }
        cout << endl;
    }
}


```

### patern 19
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
void print19(int n) {
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

### patern 20
```cpp

*    *
**  **
******
**  **
*    *

int ins = 0;
void print20(int n) {
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

### patern 21
```cpp

*****
*   *
*   *
*****


void print21(int n) {
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

### patern 22
```
4 4 4 4 4 4 4
4 3 3 3 3 3 4
4 3 2 2 2 3 4
4 3 2 1 2 3 4
4 3 2 2 2 3 4
4 3 3 3 3 3 4
4 4 4 4 4 4 4
                                                   
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


