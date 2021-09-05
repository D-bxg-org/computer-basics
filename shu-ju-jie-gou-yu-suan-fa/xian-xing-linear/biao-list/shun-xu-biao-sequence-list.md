# 顺序表（sequence list）

## 1 存储结构

```c
// 数组实现
#define MAX_SIZE = 10;
typedef struct {
    ElemType data[MAX_SIZE ];
    int length;
} SeqList; // sq = sequence 顺序
```

```c
// 动态指针实现
typedef struct SeqList {
    ElemType *elem; // 顺序表存储空间的基址（指向顺序表所占内存的起始位置）
    int length;     // 当前顺序表长度（包含多少元素）
    int listSize;   // 当前分配的存储容量（可以存储多少元素）
} SeqList;
```

## 2 数据运算

### 2.1 对于表的（list）

1 增

```c
void initSeqList(SeqList* pSeqList){
    
};
```

2 删

```c
destorySeqList(SeqList* pSeqList);
```

3 改

```c
mergeSeqList();
```

4 查

```c
bool isEmpty(SeqList seqList){
    return seqList.length == 0 ? true : false;
};
length(SeqList seqList){
    return seqList.length;
};
showSeqList(SeqList seqList){
    if(isEmpty(seqList)){
        printf("错误");
        return 0;
    }else{
        for(int i = 0; i < seqList.length; i++){
            printf("%d",seqList.elem[i]);
        }
    }
};
```

### 2.2 对于数据元素的（element）

