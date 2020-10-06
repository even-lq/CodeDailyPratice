### go语言解法

```go
func twoSum(nums []int, 
 target int) []int {
    
  // := 是声明并赋值，并且系统自动推断类型，不需要var关键字
  h := make(map[int]int) //  分配hashTable内存，并返回一个初始化的值
  // js for python 
  for i, value := range nums {
   //如果wanted:=h[value],返回ok，如果ok就执行下面的代码
   if wanted, ok := h[value]; ok {
    return []int{wanted, i}
   } else {
    h[target-value] = i
   }
  }
  //nil表示很多map类型的零值
  return nil

}
```

### JavaScript对象字面量解法