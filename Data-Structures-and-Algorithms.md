# 阶段 1

leetcode 难度最高在中等难度的中等题。

- 一维数组、二维矩阵、字符串这些相关性质的检测。（只做简单的模拟题，结合高级知识的题后面会自然遇到。）
- 初级数据结构 (列表、链表、栈、单向队列、双向队列、哈希表)
- 双指针
- 二分查找
- 堆
- 树（重点，与多种算法思想相关，比如 DFS, BFS）
- 递归、分治、回溯 把这些用典型的python语言来展示，特别是它们之间的联系和表现形式

# Python 语言展示的各种算法思想及数据结构示例：

## 一维数组（列表）：
python
复制
array = [1, 2, 3, 4, 5]
二维矩阵：
python
复制
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
字符串：
python
复制
s = "hello world"
初级数据结构之列表：
python
复制
lst = [1, 2, 3]
链表（简单模拟）：
python
复制
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

node1 = ListNode(1)
node2 = ListNode(2)
node1.next = node2
栈：
python
复制
stack = []
stack.append(1)
stack.pop()
单向队列：
python
复制
from collections import deque
queue = deque()
queue.append(1)
queue.popleft()
双向队列：
python
复制
queue = deque()
queue.append(1)
queue.appendleft(2)
queue.pop()
queue.popleft()
哈希表（字典）：
python
复制
hash_table = {}
hash_table["key"] = "value"
双指针：
python
复制
lst = [1, 2, 3, 4, 5]
left, right = 0, len(lst) - 1
while left < right:
    # do something
    left += 1
    right -= 1
二分查找：
python
复制
def binary_search(lst, target):
    left, right = 0, len(lst) - 1
    while left <= right:
        mid = left + (right - left) // 2
        if lst[mid] == target:
            return mid
        elif lst[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1
堆（使用 heapq 模块）：
python
复制
import heapq
heap = []
heapq.heappush(heap, 1)
heapq.heappop(heap)
树（以二叉树为例）：
python
复制
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

root = TreeNode(1)
root.left = TreeNode(2)
root.right = TreeNode(3)
递归：
python
复制
def factorial(n):
    if n == 0 or n == 1:
        return 1
    return n * factorial(n - 1)
分治：
python
复制
def merge_sort(lst):
    if len(lst) <= 1:
        return lst
    mid = len(lst) // 2
    left = merge_sort(lst[:mid])
    right = merge_sort(lst[mid:])
    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] < right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    result.extend(left[i:])
    result.extend(right[j:])
    return result
回溯：
python
复制
def permute(nums):
    result = []
    def backtrack(path, remaining):
        if not remaining:
            result.append(path)
            return
        for i in range(len(remaining)):
            backtrack(path + [remaining[i]], remaining[:i] + remaining[i + 1:])
    backtrack([], nums)
    return result
这些算法思想之间的联系：
递归、分治和回溯都涉及到函数调用自身的过程。递归通常是一个问题可以分解为相同性质的子问题，通过不断调用自身来解决。分治是将问题分解为多个子问题，分别解决子问题后再合并结果。回溯则是在搜索问题的解空间时，不断尝试各种可能性，当发现当前路径不满足条件时，回溯到上一步重新尝试。
树的遍历可以使用递归实现，比如深度优先搜索（DFS）和广度优先搜索（BFS）。DFS 可以通过递归或者栈来实现，而 BFS 可以使用队列来实现。
双指针在某些问题中可以和二分查找结合使用，提高查找效率。
堆可以用于实现优先队列等数据结构，在一些需要动态维护最值的问题中很有用，也可以和其他算法思想结合使用。
阶段 1
难度最高在中等难度的中等题。

一维数组、二维矩阵、字符串这些相关性质的检测。（只做简单的模拟题，结合高级知识的题后面会自然遇到。）
初级数据结构 (列表、链表、栈、单向队列、双向队列、哈希表)
双指针
二分查找
堆
树（重点，与多种算法思想相关，比如 DFS, BFS）
递归、分治、回溯 把这些用典型的python语言来展示，特别是它们之间的联系和表现形式 补充下各类数据结构和算法适合的场景，以及对应常用操作
一维数组（列表）
Python 示例：
python
复制
     arr = [1, 2, 3, 4, 5]
适用场景：存储一组有序或无序的数据元素。例如存储一组学生的成绩。
常用操作：
访问元素：arr[0]获取第一个元素。
遍历：for num in arr:。
修改元素：arr[2]=10将第三个元素修改为 10。
追加元素：arr.append(6)在末尾添加元素。
二维矩阵
Python 示例：
python
复制
     matrix = [[1, 2], [3, 4]]
适用场景：表示表格数据、图像像素等。例如棋盘游戏中的棋盘状态。
常用操作：
访问元素：matrix[0][1]获取第一行第二列的元素。
遍历行：for row in matrix:遍历每一行。
遍历元素：for i in range(len(matrix)): for j in range(len(matrix[0])): print(matrix[i][j])。
字符串
Python 示例：
python
复制
     s = "hello"
适用场景：处理文本信息，如文本解析、格式化等。
常用操作：
访问字符：s[0]获取第一个字符。
切片：s[1:3]获取第二个和第三个字符。
拼接：s1 = s + " world"。
查找子串：s.find('ll')查找子串的位置。
列表（初级数据结构）
同上述一维数组部分。
链表
Python 示例：
python
复制
     class ListNode:
         def __init__(self, val = 0, next=None):
             self.val = val
             self.next = next
     node1 = ListNode(1)
     node2 = ListNode(2)
     node1.next = node2
适用场景：适用于频繁的插入和删除操作场景，如实现 LRU 缓存。
常用操作：
创建节点：如上述ListNode类的实例化。
插入节点：在某个节点后插入新节点。
删除节点：断开节点间的连接以删除节点。
栈
Python 示例：
python
复制
     stack = []
     stack.append(1)
     stack.pop()
适用场景：函数调用栈、表达式求值（如中缀表达式转后缀表达式并求值）。
常用操作：
入栈（append）：将元素添加到栈顶。
出栈（pop）：移除并返回栈顶元素。
查看栈顶：stack[-1]（不弹出）。
单向队列
Python 示例：
python
复制
     from collections import deque
     queue = deque()
     queue.append(1)
     queue.popleft()
适用场景：广度优先搜索中存储待访问节点，任务调度等。
常用操作：
入队（append）：在队尾添加元素。
出队（popleft）：从队首移除元素。
双向队列
Python 示例：
python
复制
     queue = deque()
     queue.append(1)
     queue.appendleft(2)
     queue.pop()
     queue.popleft()
适用场景：需要在两端进行高效插入和删除操作的场景，如滑动窗口算法。
常用操作：
两端入队（append和appendleft）。
两端出队（pop和popleft）。
哈希表（字典）
Python 示例：
python
复制
     hash_table = {}
     hash_table['key'] = 'value'
适用场景：快速查找、存储键值对，如存储单词及其出现频率。
常用操作：
插入键值对：hash_table[key]=value。
查找键值：if key in hash_table:。
删除键值对：del hash_table[key]。
双指针
Python 示例：
python
复制
     arr = [1, 2, 3, 4, 5]
     left, right = 0, len(arr)-1
     while left < right:
         # 操作
         left += 1
         right -= 1
适用场景：在有序数组中查找满足特定条件的元素对（如两数之和问题），链表中判断是否有环等。
常用操作：移动指针（left += 1和right -= 1等），比较指针指向元素的值。
二分查找
Python 示例：
python
复制
     def binary_search(arr, target):
         left, right = 0, len(arr)-1
         while left <= right:
             mid = left+(right - left)//2
             if arr[mid]==target:
                 return mid
             elif arr[mid]<target:
                 left = mid + 1
             else:
                 right = mid - 1
         return -1
适用场景：在有序数组中快速查找元素。例如在已排序的电话号码簿中查找号码。
常用操作：计算中间索引（mid = left+(right - left)//2），比较中间元素与目标元素。
堆
Python 示例：
python
复制
     import heapq
     heap = []
     heapq.heappush(heap, 1)
     heapq.heappop(heap)
适用场景：实现优先队列，如任务调度中按照任务优先级执行任务。
常用操作：
插入元素（heappush）：将元素插入堆中并保持堆的性质。
弹出最小（或最大）元素（heappop）：移除并返回堆中的最小（或最大）元素。
树（以二叉树为例）
Python 示例：
python
复制
     class TreeNode:
         def __init__(self, val = 0, left=None, right=None):
             self.val = val
             self.left = left
             self.right = right
     root = TreeNode(1)
     root.left = TreeNode(2)
     root.right = TreeNode(3)
适用场景：表示层次结构数据，如文件系统目录结构、组织结构图等。
常用操作：
遍历（DFS 和 BFS）：
DFS（递归实现）：
python
复制
         def preorder(root):
             if root:
                 print(root.val)
                 preorder(root.left)
                 preorder(root.right)
BFS（使用队列实现）：
python
复制
         from collections import deque
         def bfs(root):
             if not root:
                 return
             queue = deque([root])
             while queue:
                 node = queue.popleft()
                 print(node.val)
                 if node.left:
                     queue.append(node.left)
                 if node.right:
                     queue.append(node.right)
插入节点：根据树的性质（如二叉查找树的插入规则）插入新节点。
删除节点：根据节点的度（子节点个数）等情况采用不同的删除策略。
递归
联系与表现形式：递归函数调用自身来解决问题。例如计算阶乘：
python
复制
     def factorial(n):
         if n == 0 or n == 1:
             return 1
         return n * factorial(n - 1)
适用场景：具有自相似结构的问题，如树的遍历、斐波那契数列计算等。
分治
联系与表现形式：将问题分解为子问题，分别解决后合并结果。例如归并排序：
python
复制
     def merge_sort(lst):
         if len(lst)<=1:
             return lst
         mid = len(lst)//2
         left = merge_sort(lst[:mid])
         right = merge_sort(lst[mid:])
         return merge(left, right)
     def merge(left, right):
         result = []
         i = j = 0
         while i < len(left) and j < len(right):
             if left[i]<right[j]:
                 result.append(left[i])
                 i += 1
             else:
                 result.append(right[j])
                 j += 1
         result.extend(left[i:])
         result.extend(right[j:])
         return result
适用场景：问题可以分解为独立的子问题，如大整数乘法、矩阵乘法优化等。
回溯
联系与表现形式：在搜索过程中，当发现当前选择不符合要求时，回退到上一步重新选择。例如全排列问题：
python
复制
     def permute(nums):
         result = []
         def backtrack(path, remaining):
             if not remaining:
                 result.append(path)
                 return
             for i in range(len(remaining)):
                 backtrack(path + [remaining[i]], remaining[:i]+remaining[i + 1:])
         backtrack([], nums)
         return result
适用场景：组合问题、排列问题、N 皇后问题等搜索问题。
这些数据结构和算法之间的联系：
递归是分治和回溯的基础实现方式，分治和回溯在问题分解和求解过程中往往用到递归。
树的遍历（DFS 和 BFS）算法中，DFS 可以方便地用递归实现，而 BFS 使用队列这种数据结构实现，它们都与树这种数据结构紧密相关。
双指针算法可以用于优化一些在数组或链表上的查找、排序等操作，与数组、链表等数据结构相关。
二分查找需要在有序数组（列表）上进行，依赖于数组这种数据结构的有序性。
堆这种数据结构常用于实现优先队列，在一些算法（如 Dijkstra 算法）中作为辅助数据结构，这些算法可能会与图（一种特殊的树结构扩展）相关。

