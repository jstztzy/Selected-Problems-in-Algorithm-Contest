

考虑下面的区间求和问题，每次询问在某个区间的和。

形式上说：

给定 n 个整数 A[1..n]，
每次询问 l, r，要求返回 A[l] + A[l+1] + ... + A[r]。

朴素的做法，当询问的区间的区间都是 1..n 时，需要扫描每个元素，
因而每次询问的最坏复杂度是 O(n) 。

定义 A 数组的前缀和 S[i] = A[1] + A[2] + ... + A[i]。
如果我们预处理出 S 数组，那么每次询问就可以用区间减法，返回 S[r] - S[l-1].
此时每次询问的最坏复杂度就可以做到 O(1) 了。


问题：在上面问题的基础上，要求支持单点修改操作。
由于有了修改操作，上面的做法就不奏效了。

很多数据结构、例如树状数组、线段树、二叉搜索树，都可以很好的处理这个问题。
附录的第一章将介绍树状数组，因为她的实现最简单。

<table>
<tr>
<td>数据结构</td>
<td>单点修改</td>
<td>区间求和</td>
</tr>
<tr>
<td>原数组</td>
<td>O(1)</td>
<td>O(n)</td>
</tr>
<tr>
<td>前缀和</td>
<td>O(n)</td>
<td>O(1)</td>
</tr>
<tr>
<td>树状数组</td>
<td>O(logn)</td>
<td>O(logn)</td>
</tr>
</table>


### 参考资料

- http://blog.csdn.net/shahdza/article/details/6314818

- [wikipedia - Fenwick tree](https://en.wikipedia.org/wiki/Fenwick_tree)


- [Binary Indexed Trees](https://www.topcoder.com/community/data-science/data-science-tutorials/binary-indexed-trees/)

- [POJ 3468. A Simple Problem with Integers](http://www.shuizilong.com/house/archives/poj-3468-a-simple-problem-with-integers/)
