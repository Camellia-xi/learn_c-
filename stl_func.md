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


   