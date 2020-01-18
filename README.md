# 数据结构学习笔记及源代码

## 一、稀疏数组及队列
### 1.稀疏数组
一个数组中有多个0或者其他同一元素，可转化为稀疏数组。  
**转换方法：**  
1.稀疏数组的每一列分别为元数组的row、column、value。  
2.第一行为原数组有几行几列以及有几个有效值（不为0或者同一元素）  
3.剩下的为第几行第几列的值是什么。  
### 2.队列
**要点**  
1.先进先出
#### 2.1用数组表示
1.前后端下标：front、rear  
2.最大容量：maxSize  
3.队列空：front==rear  
4.队列满：rear==maxSize-1  
#### 2.2用数组表示循环队列
1.front表示第一个元素，rear表示最后一个元素的后一个位置。  
2.队列满：（rear+1）%maxSize == front  
3.队列空：front == rear  
4.有效数据的个数：（rear+maxSize-front）%maxSize

## 二、链表
### 1.单链表
**要点**  
1.链式存储  
2.节点包含next域、data域
3.分类：带头结点（head）节点和不带头结点
### 2.双向链表
**要点**
1.data域、next指针、pre指针。
### 3.单向环形链表
**约瑟夫环的运用**  
要点：设置两个辅助结点，first指向当前状态的第一个结点（即被移除的结点的下一个结点），helper指向first-->helper.next=first

## 三、栈
**要点**  
1.先进后出
2.栈顶top、栈底bottom
3.出栈pop入栈push  
### 1.数组实现
1.初始化top=-1  
2.push：top++，stack[top]=value  
3.pop: sys.out.print(stack[top]), top--
### 2.用栈实现计算器
1.
