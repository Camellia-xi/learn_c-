##  `for`循环中的指代
1. 键值对形式的如下：
```cpp
     unordered_map<char,int> st;
     for(auto& [key,value]:st)
     {
        //...代码
     }
```

2. nums.size() 返回的是 unsigned int/long
3.dfs问题，需要标记的时候，可以考虑加个int & flag