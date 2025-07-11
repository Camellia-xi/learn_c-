##  `for`循环中的指代
1. 键值对形式的如下：
```cpp
     unordered_map<char,int> st;
     for(auto& [key,value]:st)
     {
        //...代码
     }
```