

考虑下面的区间求和问题，每次询问在某个区间的和。

形式上说：

给定 n 个整数 A[1..n]，
每次询问 l, r，要求返回 A[l] + A[l+1] + ... + A[r]。

朴素的做法，当询问的区间的区间都是 1..n 时，需要扫描每个元素，
因而每次询问的最坏复杂度是 O(n) 。

定义 A 数组的前缀和 S[i] = A[1] + A[2] + ... + A[i]。
如果我们预处理出 S 数组，那么每次询问就可以用区间减法，返回 S[r] - S[l-1].
此时每次询问的最坏复杂度就可以做到 O(1) 了。


问题，但是当我们被要求支持修改操作时，上面的做法就未必奏效了。

树状数组是一种用数组表示的树型数据结构，专为解决上面的问题而生，
由于她实现和分析起来都很简单，用来数据结构一章的开头在合适不过了。


 |  | 区间求和
 
原数组 A ｜  O(1)  | O(n)

前缀和 S  |   O(n)  |  O(1)

树状数组 C |  O(logn) |  O(logn)

<table>
<tr>
<td>John</td>
<td>Smith</td>
<td>123 Main St.</td>
<td>Springfield</td>
</tr>
<tr>
<td>Mary</td>
<td>Jones</td>
<td>456 Pine St.</td>
<td>Dover</td>
</tr>
<tr>
<td>Jim</td>
<td>Baker</td>
<td>789 Park Ave.</td>
<td>Lincoln</td>
</tr>
</table>




### 参考资料

- http://blog.csdn.net/shahdza/article/details/6314818

- [wikipedia - Fenwick tree](https://en.wikipedia.org/wiki/Fenwick_tree)


- [Binary Indexed Trees](https://www.topcoder.com/community/data-science/data-science-tutorials/binary-indexed-trees/)

- [POJ 3468. A Simple Problem with Integers](http://www.shuizilong.com/house/archives/poj-3468-a-simple-problem-with-integers/)
