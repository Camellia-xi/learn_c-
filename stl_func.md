2025/7/8 
> 做了两道滑动窗口题，总结

## 函数
1. **`stoi()`**：C++ 标准库中用来把字符串转换为整数的函数
  - 基本语法：int stoi(const std::string& str, std::size_t* pos = 0, int base = 10);
  - 参数说明：
    - `str`: 要转换的字符串
    - `pos`: 可选，指针，返回第一个未被转换字符的位置
    - `base`: 可选，表示进制（默认 10 进制，可设为 2、8、16 等）

2. **`static_cast<>`**:强制类型转换，比(int)(d)更安全
3. **`bit_width()`**:`bit_width` 是一个用于**返回一个正整数的最小位宽（不包括符号位）**的函数，要求传入参数为无符号整数`unsigned`。1后面全是0，有几个0就是2的几次方。

## STL库
1. **`set`**: set是一个去重集合。
  - 可用 `set m.` 来使用 `find()`，查找后返回迭代器，若未找到返回 `m.end()`
  - 可用 `set m.` 来使用 `lower_bound`:
    - 基本用法：`iterator lower_bound(const Key& key) const`，返回集合中第一个 >= key 的元素迭代器；`lower_bound` 是 STL 中非常常用的函数，尤其适合有序容器（如 `std::set`, `std::map`, `std::vector`）

2. **`erase`**: `erase()` 是 C++ STL 中一个非常常用的方法，用于从容器中删除元素。不同容器用法略有不同，如 `string`、`vector`、`unordered_map`。**7/11**

  - **`string`**:
  
    - 按位置删除一个字符:
    
      ```cpp
      std::string s = "hello";
      s.erase(1, 1);  // 删除从位置1开始的1个字符 → "hllo"
      ```
    
    - 从位置开始删除到末尾:
    
      ```cpp
      s.erase(2);  // 从位置2开始一直删除到末尾
      ```
    
    - 使用迭代器:
    
      ```cpp
      std::string s = "hello";
      s.erase(s.begin() + 1);  // 删除第二个字符 → "hllo"
      ```

  - **`vector`**: 一般使用迭代器，删除单个元素或区间。

  - **`unordered_map`**: 按 key 删除（最常见），也可以使用迭代器。
3.**map**：是一个有序关联容器，存储唯一key -> value（mapped value） 的键值对，元素按 key 根据比较器（默认 std::less<Key>，即升序）**自动保持排序**。
  - `insert`
  - `erase`
  - `find`
