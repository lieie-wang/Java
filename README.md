# Java
这是我第一次使用GitHub想要创建一个放Java源代码的仓库。

第一个算法题


作为开胃菜，我当然选取了最容易的一道题目，在一个数组里面移除指定value，并且返回新的数组长度。
这题唯一需要注意的地方在于 in place ，不能新建另一个数组。
方法很简单，使用两个游标i，j，遍历数组，如果碰到了value，使用j记录位置，同时递增i，直到下一个非
value出现，将此时i对应的值复制到j的位置上，增加j，重复上述过程直到遍历结束。这时候j就是新的数组
长度。
代码如下：
class Solution {
public:
int removeElement(int A[], int n, int elem) {
int i = 0;
int j = 0;
for(i = 0; i < n; i++) {
if(A[i] == elem) {
continue;
}
A[j] = A[i];
j++;
}
return j;
}
};

