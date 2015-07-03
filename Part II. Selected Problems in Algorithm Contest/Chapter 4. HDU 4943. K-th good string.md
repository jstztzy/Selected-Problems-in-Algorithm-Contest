http://acm.hdu.edu.cn/showproblem.php?pid=4943

HDU 4943. K-th good string
### Problem Description
One day, Lord gave you a string S. Let’s define the pair(x, p) represent the substring S[p-x+1,p-x+2,…,p]. The index of S counts from 0. Then, Lord will tell you some information about this string. 

There are three types of the information: 

1. Lord will give you a pair(x, p) and then says I think the substring is good.(Only consider the substring (x, p) is good, not include the substring of (x, p)) 

2. Lord will give you a pair(x, p) and then says I think the substring is not good. 

3. Lord will give you a pair(x, p) and a integer K, then you should answer the length of the K-th good string. The K-th good string means that if you list all the distinct good strings which contain pair(x, p) as suffix, then sort them by their length in ascending order, the K-th string is K-th good string. 

Now, can you hold the information from Lord? Yon can consider all the substring is not good initially.

### Input
First line is a integer T, means the number of test case, T<=10.

In every test case, there is a string S in the first line, composed by lowercase letters, |S|<=100000.

An integer q in the second line (q<=200000), and q lines follow. Every line has an integer t, means the type of the message. If t equals 3, then three integers x, p, K follow, else two integers x, p follow.

The pair (x, p) will always represent a substring of S.

### Output
For each case, output “Case #k:” one line first, where k means the case number count from 1.

For every message of type 3, print the answer one line. If there is no such K-th good string, print -1.
