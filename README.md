# Striver
Striver DSA series .....

## INDEX
 1. Patterns <br>
 2. Stl

---------
```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "run C",
            "type": "shell",
            "command": "cmd",
            "args": [
                "/c",
                "gcc ${file} -o ${fileDirname}\\${fileBasenameNoExtension}.exe && ${fileDirname}\\${fileBasenameNoExtension}.exe < ${fileDirname}\\input.txt > ${fileDirname}\\output.txt"
            ],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": ["$gcc"]
        },
        {
            "label": "run C++",
            "type": "shell",
            "command": "cmd",
            "args": [
                "/c",
                "g++ ${file} -std=c++17 -o ${fileDirname}\\${fileBasenameNoExtension}.exe && ${fileDirname}\\${fileBasenameNoExtension}.exe < ${fileDirname}\\input.txt > ${fileDirname}\\output.txt"
            ],
            "group": { "kind": "build", "isDefault": true },
            "problemMatcher": ["$gcc"]
        },
        {
            "label": "run STL (C++)",
            "type": "shell",
            "command": "cmd",
            "args": [
                "/c",
                "g++ ${file} -std=c++17 -o ${fileDirname}\\${fileBasenameNoExtension}.exe && ${fileDirname}\\${fileBasenameNoExtension}.exe < ${fileDirname}\\input.txt > ${fileDirname}\\output.txt"
            ],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": ["$gcc"]
        },
        {
     


    
    if(p1.first < p2.first) return true;
    else return false ;
}





       "label": "run Java",
            "type": "shell",
            "command": "cmd",
            "args": [
                "/c",
                "javac ${file} && java -cp ${fileDirname} ${fileBasenameNoExtension} < ${fileDirname}\\input.txt > ${fileDirname}\\output.txt"
            ],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": ["$javac"]
        },
        {
            "label": "run Python (with I/O)",
            "type": "shell",
            "command": "cmd",
            "args": [
                "/c",
                "python ${file} < ${fileDirname}\\input.txt > ${fileDirname}\\output.txt"
            ],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": []
        },
        {
            "label": "run Python (terminal output)",
            "type": "shell",
            "command": "python",
            "args": ["${file}"],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": []
        },
        {
            "label": "run JavaScript",
            "type": "shell",
            "command": "node",
            "args": ["${file}"],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": []
        },
        {
            "label": "run SQL (SQLite3)",
            "type": "shell",
            "command": "cmd",
            "args": [
                "/c",
                "sqlite3 ${fileDirname}\\database.db < ${file}"
            ],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": []
        },
        {
            "label": "open HTML/CSS",
            "type": "shell",
            "command": "cmd",
            "args": [
                "/c",
                "start ${file}"
            ],
            "group": { "kind": "build", "isDefault": false },
            "problemMatcher": []
        }
    ]
}

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


# STL

### vector 

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
##### same number in table
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec(10,-2); //dynamic programming tabular data 
    
    vec.pop_back();
    for(int val: vec) {
        cout << val << " ";
        
    }
    cout << endl;

return 0;

}
```

##### +n on begin 

```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec = {1, 2, 3, 4, 5};
    vec.erase (vec.begin() + 2 );
    for(int val: vec) {
        cout << val << " ";
    }
    cout << endl;
    
return 0;

}
```

##### replacing an element by other

```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec = {1, 2, 3, 4, 5};
    vec.erase (vec.begin() + 2 );
    for(int val: vec) {
        cout << val << " ";
    }
    cout << endl;
    
return 0;

}
```

##### clear

```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec = {1, 2, 3, 4, 5};
    
    vec.clear();
    
    for(int val: vec) {
        cout << val << " ";
    }
    cout << endl;
    
    cout << "is empty: "<< vec.empty() << endl;
    
return 0;

}
```

##### loop with begin 
```cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> vec = {1, 2, 3, 4, 5};
    
    for(vector<int>:: reverse_iterator it=vec.rbegin(); it != vec.rend(); it++) {
        cout << *(it) << " ";
    }
    
    cout << endl;
    
return 0;

}
```

### list

##### push and pop 

```cpp
#include <iostream>
#include <list>

using namespace std;

int main() {
    list<int> l; //0
    l.push_back(1);
    l.push_back(2);
    l.push_back(3);
    l.push_back(4);
    l.push_back(5);
    
    l.emplace_back(6);
    
    l.pop_back();
    
    for(int val: l) {
        cout << val << " ";
        
    }
    cout << endl;
    
    cout << "front" << l.front() << endl;
    cout << "back" << l.back() << endl;

return 0;

}
```

##### pair
```cpp
#include <iostream>
#include <list>


using namespace std;

int main() {
    pair<int, pair<char, int>> p = {1, {'a', 3}};
    
    cout << p.first << endl;
    cout << p.second.first << endl;

return 0;

}
```

```cpp
#include <iostream>
#include <list>
#include <vector>
#include <deque>

using namespace std;

int main() {
    vector<pair<int, int>> vec = {{1, 2}, {2, 3}, {3, 4}};
   // vec.push_back(4, 54); //insert
    vec.emplace_back(4, 5); //in-place objects create
    for(auto p: vec) {
        cout << p.first <<" "<< p.second << endl;
    }

return 0;

}
```

### stack

```cpp

#include <iostream>
#include <stack>

using namespace std;
int main() {
    stack<int> s;
    s.push(1);
    s.push (2);
    s.push(3);
    stack<int> s2;
    s2.swap(s);
    while(!s.empty()) {
        cout << s.top() << "";
        s.pop();
    }
    cout << endl;
    
return 0;

}

```

```cpp
#include <iostream>
#include <stack>

using namespace std;
int main() {
    stack<int> s;
    s.push(1);
    s.push (2);
    s.push(3);
    stack<int> s2;
    s2.swap(s);
    
    cout << endl;
    
    cout << "s.size: " << s.size() << endl;
    cout << "s2.size: " << s2.size() << endl;
    
return 0;

}

```




### queue

```cpp
#include <iostream>
#include <queue>

using namespace std;

int main(){
    queue<int> q;
    q.push(1);
    q.push(2);
    q.push(3);
    while(!q.empty()) {
        cout << q.front() <<" ";
        q.pop();
    }
    cout << endl;

return 0;

}
```

### Map
```cpp
#include <iostream>
#include <map>

using namespace std;

int main() {
    map<string, int> m;
    m["tv"] = 100;
    m["laptop"] = 100;
    m["headphones"] = 50;
    m["tablet"] = 120;
    m["watch"] = 50;
    for(auto p: m) {
        cout << p.first << " " << p.second << endl;
    }
    return 0;
}

```

```cpp

#include <iostream>
#include <map>

using namespace std;

int main() {
    map<string, int> m;
    m["tv"] = 100;
    m["laptop"] = 100;
    m["headphones"] = 50;
    m["tablet"] = 120;
    m["watch"] = 50;
    for(auto p: m) {
        cout << p.first << " " << p.second << endl;
    }
    
    m.emplace("camera", 25);
    
    for(auto p: m) {
        cout << p.first << " " << p.second << endl;
    }
    
    cout <<< "count = " << m.count("laptop") << endl;
    
    return 0;
}

```
```cpp
#include <iostream>
#include <map>

using namespace std;

int main() {
    map<string, int> m;
    m["tv"] = 100;
    m["laptop"] = 100;
    m["headphones"] = 50;
    m["tablet"] = 120;
    m["watch"] = 50;
    for(auto p: m) {
        cout << p.first << " " << p.second << endl;
    }
    
    m.emplace("camera", 25);
    
    m.erase("tv");

    for(auto p: m) {
        cout << p.first << " " << p.second << endl;
    }
        if (m.find("camera") != m.end()) {
            cout << "found\n";
            
        }else {
            cout << "not found";
        }
    
    
    return 0;
}
```
```cpp
#include <iostream>
#include <map>

using namespace std;

int main() {
    map<string, int> m;
    m["tv"] = 100;
    m["laptop"] = 100;
    m["headphones"] = 50;
    m["tablet"] = 120;
    m["watch"] = 50;
    for(auto p: m) {
        cout << p.first << " " << p.second << endl;
    }
    
    m.emplace("camera", 25);
    
    m.erase(m.find("tv"));
    
    for(auto p: m) {
        cout << p.first <<" "<< p.second << endl;
    }
    
    
    return 0;
}
```

##### multimap
```cpp
#include <iostream>
#include <map>

using namespace std;

int main() {
    multimap<string, int> m;
    
    m.emplace("tv", 100);
    m.emplace("tv", 100);
    m.emplace("tv", 100);
    m.emplace("tv", 100);
    
    m.erase(m.find("tv"));
    
    for(auto p: m) {
        cout << p.first << " " << p.second << endl;
    }

return 0;


}
```

#### set
```cpp
#include <iostream>
#include <map>
#include <set>
using namespace std;

int main() {
    set<int> s;
    s.insert(1);
    s.insert(2);
    s.insert(3);
    s.insert(4);
    s.insert(5);
    for(auto val: s) {
        cout << val << " ";
        cout << endl;
    }

return 0;


}
```

```cpp
#include <iostream>
#include <map>
#include <set>
using namespace std;

int main() {
    set<int> s;
    s.insert(1);
    s.insert(2);
    s.insert(3);
    s.insert(4);
    s.insert(5);
    
    
    cout << "lower bound = " << *(s.lower_bound (4)) << endl; //4
    
    for(auto val: s) {
        cout << val << " ";
        cout << endl;
    }

return 0;


}
```

```cpp
#include <iostream>
#include <algorithm>  

using namespace std;

int main() {
    int arr[5] = {3, 5, 1, 8, 2};

    sort(arr, arr + 5);  

    for (int val : arr) {
        cout << val << " ";  
    }

    cout << endl;

    return 0;
}

```

#### sorting
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

int main() {
vector<int> vec = {3, 5, 1, 8, 2};

sort(vec.begin(), vec.end(), greater<int>());

for(int val : vec) {
    cout << val << " ";
};

cout << endl;
return 0;
};
```

###### sorting in pair
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

int main() {
    vector<pair<int, int>> vec = {{3, 1}, {2, 1}, {7, 1}, {5, 2}};

    sort(vec.begin(), vec.end());

    for(auto p : vec) {
        cout << p.first << " " << p.second << endl;
    };


return 0;
};
```

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;
bool comparator(pair<int,int> p1,pair<int,int> p2){
    if(p1.second < p2.second) return true;
    if(p1.second > p2.second) return false;
    
    if(p1.first < p2.first) return true;
    else return false ;
}



int main() {
    vector<int> vec = {1, 2, 3, 4, 5};
    
    reverse (vec.begin(), vec.end());
for(auto val : vec) {
    cout << val<< endl;
}

return 0;
};
```

##### next permutations 
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;
bool comparator(pair<int,int> p1,pair<int,int> p2){
    if(p1.second < p2.second) return true;
    if(p1.second > p2.second) return false;
    
    if(p1.first < p2.first) return true;
    else return false ;
}



int main() {
    string s = "abc";
    next_permutation (s.begin(), s.end());
    
    cout << s << endl;

return 0;
};
```
##### prev permutations 
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;
bool comparator(pair<int,int> p1,pair<int,int> p2){
    if(p1.second < p2.second) return true;
    if(p1.second > p2.second) return false;
    
    if(p1.first < p2.first) return true;
    else return false ;
}



int main() {
    string s = "abc";
    prev_permutation (s.begin(), s.end());
    
    cout << s << endl;

return 0;
};
```


```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;
bool comparator(pair<int,int> p1,pair<int,int> p2){
    if(p1.second < p2.second) return true;
    if(p1.second > p2.second) return false;
int main() {
    vector<int> vec = {1,2,3,4,5};
    
    cout << *(max_element(vec.begin(),vec.end()) )<< endl;
    cout << *(min_element(vec.begin(),vec.end()) )<< endl;
    cout << binary_search(vec.begin(),vec.end(),4) << endl;
return 0;
};
```

#### builtin count sets 
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

int main() {
    int n = 15;
    
    cout << __builtin_popcount(n) << endl ;
    
return 0;
};
```

