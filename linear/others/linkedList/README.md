## 链表

* 单链表

* 双链表

#### 单链表的基本操作

* 结构体定义
```c
typedef struct Node{
        ElemType data; //数据域
        struct Node* next; //指针域
    }Node,*DLinkListPtr;
```

* **头插法**建立单链表
```c
node = (DLinkListPtr)malloc(sizeof(Node));
node->data = &data;
node->next = list->next;
list->next = node;
```

* **尾插法**建立单链表
```c
node->data = &data;
while(p->next)  //将指针移到最后一个结点
{
    p = p->next;
}
node->next = NULL;
p-next = node;
```

* **插入**数据到第pos个位置
```c
while(i < pos-1 && p) //将指针移动到第pos-1个结点位置
{
    p = p->next;
    i++;
}
newNode->data = e;
newNode->next = p->next;
p->next = newNode;
```

* **删除**第pos个结点
```c
while(p && i < pos-1) //将指针移动到第pos-1个结点位置
{
    p = p->next;
    i++;
}
q = p->next;
*e = q->data;
p->next = q->next;
free(q);
```

### 双链表的基本操作

* 结构体定义
```c
typedef struct DNode{
    Elemtype data;
    DNode* struct prior;
    DNode* struct next;
    }Node,*DLinkListPtr;
```

 * **建立**双链表
 ```c
node = (DLinkListPtr)malloc(sizeof(DNode));
p->next = node;
node->prior = p;
p = p->next;
 ```
* **插入**数据到第pos个位置

    * 插入的位置在表头

    * 插入的位置在最后

    * 插入的位置在中间


* **删除**指定数值的结点

```c
while(p){
    if(p->data == data)
    {
        p->prior->next = p->next;
        p->next->prior = p->prior;
        free(p);
        return dlist;
    }
    p-p>next;
    }
    printf("Not availiable!");
```




