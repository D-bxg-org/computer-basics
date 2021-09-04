# 顺序表（sequence list）

## 1 存储结构

```c
// 数组实现
#define MAX_SIZE = 10;
typedef struct {
    ElemType data[MAX_SIZE ];
    int length;
} SqList; // sq = sequence 顺序
```

```c
// 动态指针实现
typedef struct SqList
{
    ElemType *elem; // 顺序表存储空间的基址（指向顺序表所占内存的起始位置）
    int length;     // 当前顺序表长度（包含多少元素）
    int listSize;   // 当前分配的存储容量（可以存储多少元素）
} SqList;
```

## 2 数据运算

