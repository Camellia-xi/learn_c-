2025/7/8
> 做了两道滑动窗口题，总结
## 函数
1. **`stoi()`**：C++ 标准库中用来把字符串转换为整数的函数
  - 基本语法：int stoi(const std::string& str, std::size_t* pos = 0, int base = 10);
  - 参数说明：`str`:要转换的字符串
             `pos`:可选，指针，返回第一个未被转换字符的位置
             `base`:可选，表示进制（默认 10 进制，可设为 2、8、16 等）

## STL库
1. **`set`**:set是一个去重集合。
  - 可用`set m.`来使用`find()`，查找后返回迭代器，若未找到返回`m.end()`
  - 可用`set m.`来使用`lower_bound`:
                - 基本用法：`iterator lower_bound(const Key& key) const`,返回一个迭代器，指向集合中第一个 >= key 的元素;`lower_bound` 是一个非常常用的 **STL** 函数，尤其在有序容器中（如 `std::set`, `std::map`, `std::vector`）。

2. **`erase`**:`erase()` 是 C++ STL 中的一个非常常用的方法，用于从容器中删除元素。它在不同容器中表现略有不同，比如 `string`、`vector`、`unordered_map` 等都有自己的用法。
    - **`string`**:
                   - 按位置删除一个字符: 
```cpp
  std::string s = "hello";
  s.erase(1, 1);  // 删除从位置1开始的1个字符 → "hllo"
```
                  - 从位置开始删除到末尾:`s.erase(2) //从位置2开始一直删除到末尾`
                  - 使用迭代器：
```cpp
std::string s = "hello";
s.erase(s.begin() + 1);  // 删除第二个字符 → "hllo"
```

    - **`vector`**:一般使用迭代器，删除单个元素，或者区间
    - **`unordered_map`**:按 key 删除（最常见），也可以使用迭代器。
   