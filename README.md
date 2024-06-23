## 相关介绍

这是一个 [LeetCode](https://leetcode.cn/problemset/all/) 题目自动统计及分析程序，可自动统计所有提交通过的题目，并以 Markdown 的形式展示。

根据个人需求，目前只考虑获取**提交次数**和**重刷次数**这两个指标，以便更好地进行刷题。

采用 GitHub Actions 进行自动化部署，无需本地服务器资源。

## 使用教程

1. 由模板项目[生成](https://github.com/CompetitiveLin/leetcode-revise/generate)自己的项目

2. 点击生成项目下的 Settings -> Secrets -> Actions -> New repository secret，分别添加以下 Secrets：
    - Name：`LEETCODE_SESSION`
        - Secret：已登录 LeetCode 账号的浏览器中 Cookie 名为 LEETCODE_SESSION 的值

3. 回到项目首页并进入 Actions 部分，在左侧点击`Github LeetCode Bot`，再点击蓝色提示框中的 `Run workflow`，最后点击绿色的 `Run workflow` 按钮即可

## 补充说明

默认配置为每12小时更新一次，可根据需求修改 [action.yml](.github/workflows/action.yml#L9) 文件的第 `9` 行。如有其他需求，欢迎提交PR。

> 重刷次数的计算规则为：累计所有提交通过且互为不同一天的记录次数

## 数据统计

| 最近提交时间 | 题目 | 题目难度 | 提交次数| 重刷次数 |
| ---- | ---- | ---- | ---- | ---- |
| 2024-06-23 19:20 | [#122 买卖股票的最佳时机 II](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-ii) | MEDIUM | 2 | **2** |
| 2024-06-23 15:47 | [#31 下一个排列](https://leetcode.cn/problems/next-permutation) | MEDIUM | 6 | **3** |
| 2024-06-16 13:51 | [#22 括号生成](https://leetcode.cn/problems/generate-parentheses) | MEDIUM | 3 | **3** |
| 2024-06-15 15:46 | [#300 最长递增子序列](https://leetcode.cn/problems/longest-increasing-subsequence) | MEDIUM | 5 | **3** |
| 2024-06-15 14:12 | [#2779 数组的最大美丽值](https://leetcode.cn/problems/maximum-beauty-of-an-array-after-applying-operation) | MEDIUM | 4 | 1 |
| 2024-06-14 21:37 | [#2786 访问数组中的位置使分数最大](https://leetcode.cn/problems/visit-array-positions-to-maximize-score) | MEDIUM | 2 | 1 |
| 2024-05-26 15:35 | [#189 轮转数组](https://leetcode.cn/problems/rotate-array) | MEDIUM | 3 | **2** |
| 2024-05-06 11:57 | [#382 链表随机节点](https://leetcode.cn/problems/linked-list-random-node) | MEDIUM | 3 | 1 |
| 2024-05-06 11:07 | [#413 等差数列划分](https://leetcode.cn/problems/arithmetic-slices) | MEDIUM | 1 | 1 |
| 2024-04-18 14:51 | [#525 连续数组](https://leetcode.cn/problems/contiguous-array) | MEDIUM | 1 | 1 |
| 2024-03-31 14:08 | [#424 替换后的最长重复字符](https://leetcode.cn/problems/longest-repeating-character-replacement) | MEDIUM | 2 | 1 |
| 2024-03-23 16:02 | [#1471 数组中的 k 个最强值](https://leetcode.cn/problems/the-k-strongest-values-in-an-array) | MEDIUM | 1 | 1 |
| 2024-03-19 19:39 | [#1838 最高频元素的频数](https://leetcode.cn/problems/frequency-of-the-most-frequent-element) | MEDIUM | 1 | 1 |
| 2024-03-18 14:24 | [#658 找到 K 个最接近的元素](https://leetcode.cn/problems/find-k-closest-elements) | MEDIUM | 4 | 1 |
| 2024-03-18 11:20 | [#187 重复的DNA序列](https://leetcode.cn/problems/repeated-dna-sequences) | MEDIUM | 2 | 1 |
| 2024-03-15 14:19 | [#2487 从链表中移除节点](https://leetcode.cn/problems/remove-nodes-from-linked-list) | MEDIUM | 1 | 1 |
| 2024-03-12 18:00 | [#1261 在受污染的二叉树中查找元素](https://leetcode.cn/problems/find-elements-in-a-contaminated-binary-tree) | MEDIUM | 1 | 1 |
| 2024-03-10 10:17 | [#299 猜数字游戏](https://leetcode.cn/problems/bulls-and-cows) | MEDIUM | 2 | 1 |
| 2024-03-03 11:41 | [#225 用队列实现栈](https://leetcode.cn/problems/implement-stack-using-queues) | EASY | 3 | 1 |
| 2024-02-09 10:42 | [#236 二叉树的最近公共祖先](https://leetcode.cn/problems/lowest-common-ancestor-of-a-binary-tree) | MEDIUM | 3 | **2** |
| 2024-01-26 15:56 | [#91 解码方法](https://leetcode.cn/problems/decode-ways) | MEDIUM | 2 | 1 |
| 2024-01-26 10:13 | [#235 二叉搜索树的最近公共祖先](https://leetcode.cn/problems/lowest-common-ancestor-of-a-binary-search-tree) | MEDIUM | 3 | 1 |
| 2024-01-24 11:25 | [#274 H 指数](https://leetcode.cn/problems/h-index) | MEDIUM | 3 | 1 |
| 2024-01-23 22:15 | [#26 删除有序数组中的重复项](https://leetcode.cn/problems/remove-duplicates-from-sorted-array) | EASY | 2 | 1 |
| 2024-01-23 22:05 | [#80 删除有序数组中的重复项 II](https://leetcode.cn/problems/remove-duplicates-from-sorted-array-ii) | MEDIUM | 1 | 1 |
| 2024-01-23 16:34 | [#25 K 个一组翻转链表](https://leetcode.cn/problems/reverse-nodes-in-k-group) | HARD | 1 | 1 |
| 2024-01-23 12:13 | [#39 组合总和](https://leetcode.cn/problems/combination-sum) | MEDIUM | 2 | **2** |
| 2024-01-23 09:27 | [#77 组合](https://leetcode.cn/problems/combinations) | MEDIUM | 2 | 1 |
| 2024-01-22 11:10 | [#670 最大交换](https://leetcode.cn/problems/maximum-swap) | MEDIUM | 13 | **2** |
| 2024-01-20 15:18 | [#82 删除排序链表中的重复元素 II](https://leetcode.cn/problems/remove-duplicates-from-sorted-list-ii) | MEDIUM | 3 | **2** |
| 2024-01-20 13:17 | [#373 查找和最小的 K 对数字](https://leetcode.cn/problems/find-k-pairs-with-smallest-sums) | MEDIUM | 3 | **2** |
| 2024-01-19 16:19 | [#56 合并区间](https://leetcode.cn/problems/merge-intervals) | MEDIUM | 4 | **2** |
| 2024-01-18 15:29 | [#494 目标和](https://leetcode.cn/problems/target-sum) | MEDIUM | 2 | **2** |
| 2024-01-18 14:02 | [#416 分割等和子集](https://leetcode.cn/problems/partition-equal-subset-sum) | MEDIUM | 1 | 1 |
| 2024-01-18 10:52 | [#148 排序链表](https://leetcode.cn/problems/sort-list) | MEDIUM | 1 | 1 |
| 2024-01-03 10:27 | [#150 逆波兰表达式求值](https://leetcode.cn/problems/evaluate-reverse-polish-notation) | MEDIUM | 1 | 1 |
| 2024-01-03 09:58 | [#209 长度最小的子数组](https://leetcode.cn/problems/minimum-size-subarray-sum) | MEDIUM | 4 | 1 |
| 2024-01-03 09:18 | [#15 三数之和](https://leetcode.cn/problems/3sum) | MEDIUM | 7 | **3** |
| 2023-12-29 16:24 | [#322 零钱兑换](https://leetcode.cn/problems/coin-change) | MEDIUM | 1 | 1 |
| 2023-12-29 15:53 | [#230 二叉搜索树中第K小的元素](https://leetcode.cn/problems/kth-smallest-element-in-a-bst) | MEDIUM | 1 | 1 |
| 2023-12-29 15:01 | [#78 子集](https://leetcode.cn/problems/subsets) | MEDIUM | 2 | 1 |
| 2023-12-28 17:12 | [#279 完全平方数](https://leetcode.cn/problems/perfect-squares) | MEDIUM | 2 | 1 |
| 2023-12-28 13:30 | [#5 最长回文子串](https://leetcode.cn/problems/longest-palindromic-substring) | MEDIUM | 2 | 1 |
| 2023-12-26 22:24 | [#1143 最长公共子序列](https://leetcode.cn/problems/longest-common-subsequence) | MEDIUM | 2 | 1 |
| 2023-12-24 12:30 | [#567 字符串的排列](https://leetcode.cn/problems/permutation-in-string) | MEDIUM | 3 | 1 |
| 2023-12-23 10:30 | [#1962 移除石子使总数最小](https://leetcode.cn/problems/remove-stones-to-minimize-the-total) | MEDIUM | 1 | 1 |
| 2023-12-20 20:08 | [#94 二叉树的中序遍历](https://leetcode.cn/problems/binary-tree-inorder-traversal) | EASY | 1 | 1 |
| 2023-12-20 20:00 | [#11 盛最多水的容器](https://leetcode.cn/problems/container-with-most-water) | MEDIUM | 5 | **2** |
| 2023-12-14 17:19 | [#226 翻转二叉树](https://leetcode.cn/problems/invert-binary-tree) | EASY | 3 | 1 |
| 2023-12-10 12:27 | [#1137 第 N 个泰波那契数](https://leetcode.cn/problems/n-th-tribonacci-number) | EASY | 2 | **2** |
| 2023-12-10 12:18 | [#70 爬楼梯](https://leetcode.cn/problems/climbing-stairs) | EASY | 3 | **2** |
| 2023-12-06 11:20 | [#3 无重复字符的最长子串](https://leetcode.cn/problems/longest-substring-without-repeating-characters) | MEDIUM | 8 | **2** |
| 2023-12-05 19:53 | [#53 最大子数组和](https://leetcode.cn/problems/maximum-subarray) | MEDIUM | 3 | **2** |
| 2023-12-03 10:34 | [#1423 可获得的最大点数](https://leetcode.cn/problems/maximum-points-you-can-obtain-from-cards) | MEDIUM | 2 | 1 |
| 2023-12-02 13:16 | [#215 数组中的第K个最大元素](https://leetcode.cn/problems/kth-largest-element-in-an-array) | MEDIUM | 3 | **2** |
| 2023-12-02 11:49 | [#1094 拼车](https://leetcode.cn/problems/car-pooling) | MEDIUM | 3 | 1 |
| 2023-12-01 15:34 | [#287 寻找重复数](https://leetcode.cn/problems/find-the-duplicate-number) | MEDIUM | 1 | 1 |
| 2023-12-01 14:44 | [#2661 找出叠涂元素](https://leetcode.cn/problems/first-completely-painted-row-or-column) | MEDIUM | 3 | 1 |
| 2023-11-25 16:27 | [#92 反转链表 II](https://leetcode.cn/problems/reverse-linked-list-ii) | MEDIUM | 2 | **2** |
| 2023-11-25 15:33 | [#138 随机链表的复制](https://leetcode.cn/problems/copy-list-with-random-pointer) | MEDIUM | 2 | 1 |
| 2023-11-13 20:11 | [#307 区域和检索 - 数组可修改](https://leetcode.cn/problems/range-sum-query-mutable) | MEDIUM | 4 | **3** |
| 2023-11-13 15:25 | [#1234 替换子串得到平衡字符串](https://leetcode.cn/problems/replace-the-substring-for-balanced-string) | MEDIUM | 2 | 1 |
| 2023-11-10 22:06 | [#114 二叉树展开为链表](https://leetcode.cn/problems/flatten-binary-tree-to-linked-list) | MEDIUM | 2 | **2** |
| 2023-11-09 15:01 | [#151 反转字符串中的单词](https://leetcode.cn/problems/reverse-words-in-a-string) | MEDIUM | 2 | 1 |
| 2023-11-04 16:08 | [#47 全排列 II](https://leetcode.cn/problems/permutations-ii) | MEDIUM | 5 | **4** |
| 2023-11-04 15:45 | [#46 全排列](https://leetcode.cn/problems/permutations) | MEDIUM | 7 | **5** |
| 2023-11-02 10:23 | [#153 寻找旋转排序数组中的最小值](https://leetcode.cn/problems/find-minimum-in-rotated-sorted-array) | MEDIUM | 1 | 1 |
| 2023-10-27 10:26 | [#1465 切割后面积最大的蛋糕](https://leetcode.cn/problems/maximum-area-of-a-piece-of-cake-after-horizontal-and-vertical-cuts) | MEDIUM | 2 | 1 |
| 2023-10-23 22:55 | [#142 环形链表 II](https://leetcode.cn/problems/linked-list-cycle-ii) | MEDIUM | 2 | **2** |
| 2023-10-23 19:28 | [#141 环形链表](https://leetcode.cn/problems/linked-list-cycle) | EASY | 2 | 1 |
| 2023-10-11 10:11 | [#2512 奖励最顶尖的 K 名学生](https://leetcode.cn/problems/reward-top-k-students) | MEDIUM | 1 | 1 |
| 2023-10-05 19:53 | [#309 买卖股票的最佳时机含冷冻期](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-with-cooldown) | MEDIUM | 1 | 1 |
| 2023-10-05 17:54 | [#121 买卖股票的最佳时机](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock) | EASY | 1 | 1 |
| 2023-09-25 22:38 | [#146 LRU 缓存](https://leetcode.cn/problems/lru-cache) | MEDIUM | 1 | 1 |
| 2023-09-21 15:14 | [#155 最小栈](https://leetcode.cn/problems/min-stack) | MEDIUM | 3 | 1 |
| 2023-09-19 21:25 | [#347 前 K 个高频元素](https://leetcode.cn/problems/top-k-frequent-elements) | MEDIUM | 3 | 1 |
| 2023-09-18 19:50 | [#337 打家劫舍 III](https://leetcode.cn/problems/house-robber-iii) | MEDIUM | 4 | **2** |
| 2023-09-17 22:03 | [#213 打家劫舍 II](https://leetcode.cn/problems/house-robber-ii) | MEDIUM | 4 | **2** |
| 2023-09-17 22:02 | [#198 打家劫舍](https://leetcode.cn/problems/house-robber) | MEDIUM | 10 | **5** |
| 2023-09-14 20:00 | [#75 颜色分类](https://leetcode.cn/problems/sort-colors) | MEDIUM | 3 | 1 |
| 2023-09-13 20:18 | [#763 划分字母区间](https://leetcode.cn/problems/partition-labels) | MEDIUM | 1 | 1 |
| 2023-09-12 20:12 | [#438 找到字符串中所有字母异位词](https://leetcode.cn/problems/find-all-anagrams-in-a-string) | MEDIUM | 1 | 1 |
| 2023-09-10 12:15 | [#2594 修车的最少时间](https://leetcode.cn/problems/minimum-time-to-repair-cars) | MEDIUM | 4 | 1 |
| 2023-09-01 09:45 | [#2240 买钢笔和铅笔的方案数](https://leetcode.cn/problems/number-of-ways-to-buy-pens-and-pencils) | MEDIUM | 3 | 1 |
| 2023-08-28 19:16 | [#57 插入区间](https://leetcode.cn/problems/insert-interval) | MEDIUM | 1 | 1 |
| 2023-08-25 09:49 | [#83 删除排序链表中的重复元素](https://leetcode.cn/problems/remove-duplicates-from-sorted-list) | EASY | 3 | 1 |
| 2023-08-10 20:25 | [#784 字母大小写全排列](https://leetcode.cn/problems/letter-case-permutation) | MEDIUM | 7 | **3** |
| 2023-07-16 12:33 | [#1679 K 和数对的最大数目](https://leetcode.cn/problems/max-number-of-k-sum-pairs) | MEDIUM | 1 | 1 |
| 2023-07-13 23:30 | [#931 下降路径最小和](https://leetcode.cn/problems/minimum-falling-path-sum) | MEDIUM | 1 | 1 |
| 2023-07-12 19:42 | [#450 删除二叉搜索树中的节点](https://leetcode.cn/problems/delete-node-in-a-bst) | MEDIUM | 5 | 1 |
| 2023-07-10 22:29 | [#394 字符串解码](https://leetcode.cn/problems/decode-string) | MEDIUM | 3 | 1 |
| 2023-07-06 00:26 | [#328 奇偶链表](https://leetcode.cn/problems/odd-even-linked-list) | MEDIUM | 1 | 1 |
| 2023-07-03 23:34 | [#445 两数相加 II](https://leetcode.cn/problems/add-two-numbers-ii) | MEDIUM | 3 | 1 |
| 2023-06-27 21:34 | [#912 排序数组](https://leetcode.cn/problems/sort-an-array) | MEDIUM | 13 | **6** |
| 2023-06-25 13:35 | [#162 寻找峰值](https://leetcode.cn/problems/find-peak-element) | MEDIUM | 2 | 1 |
| 2023-06-23 13:38 | [#2095 删除链表的中间节点](https://leetcode.cn/problems/delete-the-middle-node-of-a-linked-list) | MEDIUM | 3 | 1 |
| 2023-06-11 19:37 | [#1171 从链表中删去总和值为零的连续节点](https://leetcode.cn/problems/remove-zero-sum-consecutive-nodes-from-linked-list) | MEDIUM | 5 | 1 |
| 2023-06-08 21:01 | [#2390 从字符串中移除星号](https://leetcode.cn/problems/removing-stars-from-a-string) | MEDIUM | 1 | 1 |
| 2023-06-07 20:08 | [#2611 老鼠和奶酪](https://leetcode.cn/problems/mice-and-cheese) | MEDIUM | 5 | 1 |
| 2023-06-02 13:15 | [#2559 统计范围内的元音字符串数](https://leetcode.cn/problems/count-vowel-strings-in-ranges) | MEDIUM | 3 | 1 |
| 2023-06-01 16:33 | [#2517 礼盒的最大甜蜜度](https://leetcode.cn/problems/maximum-tastiness-of-candy-basket) | MEDIUM | 3 | 1 |
| 2023-05-31 21:16 | [#2300 咒语和药水的成功对数](https://leetcode.cn/problems/successful-pairs-of-spells-and-potions) | MEDIUM | 3 | 1 |
| 2023-05-29 22:29 | [#2352 相等行列对](https://leetcode.cn/problems/equal-row-and-column-pairs) | MEDIUM | 2 | 1 |
| 2023-05-25 16:03 | [#452 用最少数量的箭引爆气球](https://leetcode.cn/problems/minimum-number-of-arrows-to-burst-balloons) | MEDIUM | 2 | 1 |
| 2023-05-21 14:18 | [#435 无重叠区间](https://leetcode.cn/problems/non-overlapping-intervals) | MEDIUM | 3 | 1 |
| 2023-05-14 18:13 | [#1054 距离相等的条形码](https://leetcode.cn/problems/distant-barcodes) | MEDIUM | 3 | 1 |
| 2023-05-11 17:54 | [#560 和为 K 的子数组](https://leetcode.cn/problems/subarray-sum-equals-k) | MEDIUM | 1 | 1 |
| 2023-05-11 10:54 | [#1016 子串能表示从 1 到 N 数字的二进制串](https://leetcode.cn/problems/binary-string-with-substrings-representing-1-to-n) | MEDIUM | 2 | 1 |
| 2023-05-07 12:24 | [#1010 总持续时间可被 60 整除的歌曲](https://leetcode.cn/problems/pairs-of-songs-with-total-durations-divisible-by-60) | MEDIUM | 3 | 1 |
| 2023-05-06 22:58 | [#1419 数青蛙](https://leetcode.cn/problems/minimum-number-of-frogs-croaking) | MEDIUM | 10 | 1 |
| 2023-05-05 13:57 | [#283 移动零](https://leetcode.cn/problems/move-zeroes) | EASY | 1 | 1 |
| 2023-05-04 16:25 | [#128 最长连续序列](https://leetcode.cn/problems/longest-consecutive-sequence) | MEDIUM | 4 | 1 |
| 2023-05-03 22:12 | [#1003 检查替换后的词是否有效](https://leetcode.cn/problems/check-if-word-is-valid-after-substitutions) | MEDIUM | 1 | 1 |
| 2023-05-02 11:03 | [#970 强整数](https://leetcode.cn/problems/powerful-integers) | MEDIUM | 3 | 1 |
| 2023-05-01 12:27 | [#1376 通知所有员工所需的时间](https://leetcode.cn/problems/time-needed-to-inform-all-employees) | MEDIUM | 1 | 1 |
| 2023-04-30 19:11 | [#49 字母异位词分组](https://leetcode.cn/problems/group-anagrams) | MEDIUM | 2 | 1 |
| 2023-04-30 14:00 | [#1033 移动石子直到连续](https://leetcode.cn/problems/moving-stones-until-consecutive) | MEDIUM | 3 | 1 |
| 2023-04-14 20:04 | [#1023 驼峰式匹配](https://leetcode.cn/problems/camelcase-matching) | MEDIUM | 3 | 1 |
| 2023-04-09 11:22 | [#739 每日温度](https://leetcode.cn/problems/daily-temperatures) | MEDIUM | 2 | 1 |
| 2023-04-03 22:13 | [#1053 交换一次的先前排列](https://leetcode.cn/problems/previous-permutation-with-one-swap) | MEDIUM | 4 | 1 |
| 2023-03-30 20:02 | [#1637 两点之间不包含任何点的最宽垂直区域](https://leetcode.cn/problems/widest-vertical-area-between-two-points-containing-no-points) | EASY | 2 | 1 |
| 2023-03-29 23:55 | [#1641 统计字典序元音字符串的数目](https://leetcode.cn/problems/count-sorted-vowel-strings) | MEDIUM | 1 | 1 |
| 2023-03-22 19:50 | [#1626 无矛盾的最佳球队](https://leetcode.cn/problems/best-team-with-no-conflicts) | MEDIUM | 5 | 1 |
| 2023-03-21 19:16 | [#62 不同路径](https://leetcode.cn/problems/unique-paths) | MEDIUM | 2 | 1 |
| 2023-03-18 11:47 | [#1616 分割两个字符串得到回文串](https://leetcode.cn/problems/split-two-strings-to-make-palindrome) | MEDIUM | 5 | 1 |
| 2023-03-17 21:21 | [#89 格雷编码](https://leetcode.cn/problems/gray-code) | MEDIUM | 1 | 1 |
| 2023-03-15 11:09 | [#1615 最大网络秩](https://leetcode.cn/problems/maximal-network-rank) | MEDIUM | 1 | 1 |
| 2023-03-14 19:12 | [#1605 给定行和列的和求可行矩阵](https://leetcode.cn/problems/find-valid-matrix-given-row-and-column-sums) | MEDIUM | 1 | 1 |
| 2023-03-13 15:38 | [#289 生命游戏](https://leetcode.cn/problems/game-of-life) | MEDIUM | 2 | 1 |
| 2023-03-08 21:52 | [#LCR 166 珠宝的最高价值](https://leetcode.cn/problems/li-wu-de-zui-da-jie-zhi-lcof) | MEDIUM | 1 | 1 |
| 2023-03-06 21:52 | [#1653 使字符串平衡的最少删除次数](https://leetcode.cn/problems/minimum-deletions-to-make-string-balanced) | MEDIUM | 4 | 1 |
| 2023-03-03 19:26 | [#1487 保证文件名唯一](https://leetcode.cn/problems/making-file-names-unique) | MEDIUM | 5 | 1 |
| 2023-02-28 21:44 | [#1801 积压订单中的订单总数](https://leetcode.cn/problems/number-of-orders-in-the-backlog) | MEDIUM | 2 | 1 |
| 2023-02-27 17:01 | [#1144 递减元素使数组呈锯齿状](https://leetcode.cn/problems/decrease-elements-to-make-array-zigzag) | MEDIUM | 4 | 1 |
| 2023-02-20 10:19 | [#1792 最大平均通过率](https://leetcode.cn/problems/maximum-average-pass-ratio) | MEDIUM | 2 | 1 |
| 2023-02-12 09:58 | [#1138 字母板上的路径](https://leetcode.cn/problems/alphabet-board-path) | MEDIUM | 4 | 1 |
| 2023-02-09 17:45 | [#1797 设计一个验证系统](https://leetcode.cn/problems/design-authentication-manager) | MEDIUM | 2 | 1 |
| 2023-02-08 14:28 | [#1233 删除子文件夹](https://leetcode.cn/problems/remove-sub-folders-from-the-filesystem) | MEDIUM | 1 | 1 |
| 2023-01-30 19:28 | [#1669 合并两个链表](https://leetcode.cn/problems/merge-in-between-linked-lists) | MEDIUM | 2 | 1 |
| 2023-01-29 16:50 | [#264 丑数 II](https://leetcode.cn/problems/ugly-number-ii) | MEDIUM | 2 | 1 |
| 2023-01-28 14:37 | [#1664 生成平衡数组的方案数](https://leetcode.cn/problems/ways-to-make-a-fair-array) | MEDIUM | 2 | 1 |
| 2023-01-27 20:38 | [#503 下一个更大元素 II](https://leetcode.cn/problems/next-greater-element-ii) | MEDIUM | 3 | 1 |
| 2023-01-27 19:53 | [#42 接雨水](https://leetcode.cn/problems/trapping-rain-water) | HARD | 2 | 1 |
| 2023-01-26 18:25 | [#1663 具有给定数值的最小字符串](https://leetcode.cn/problems/smallest-string-with-a-given-numeric-value) | MEDIUM | 2 | 1 |
| 2023-01-23 22:32 | [#199 二叉树的右视图](https://leetcode.cn/problems/binary-tree-right-side-view) | MEDIUM | 2 | 1 |
| 2023-01-16 22:39 | [#1813 句子相似性 III](https://leetcode.cn/problems/sentence-similarity-iii) | MEDIUM | 3 | 1 |
| 2023-01-13 20:15 | [#38 外观数列](https://leetcode.cn/problems/count-and-say) | MEDIUM | 1 | 1 |
| 2023-01-13 14:19 | [#36 有效的数独](https://leetcode.cn/problems/valid-sudoku) | MEDIUM | 1 | 1 |
| 2023-01-09 16:15 | [#1806 还原排列的最少操作步数](https://leetcode.cn/problems/minimum-number-of-operations-to-reinitialize-a-permutation) | MEDIUM | 1 | 1 |
| 2023-01-07 22:33 | [#1658 将 x 减到 0 的最小操作数](https://leetcode.cn/problems/minimum-operations-to-reduce-x-to-zero) | MEDIUM | 1 | 1 |
| 2023-01-05 20:00 | [#143 重排链表](https://leetcode.cn/problems/reorder-list) | MEDIUM | 2 | 1 |
| 2023-01-05 19:37 | [#206 反转链表](https://leetcode.cn/problems/reverse-linked-list) | EASY | 2 | 1 |
| 2023-01-03 15:54 | [#34 在排序数组中查找元素的第一个和最后一个位置](https://leetcode.cn/problems/find-first-and-last-position-of-element-in-sorted-array) | MEDIUM | 4 | 1 |
| 2022-12-31 10:58 | [#2037 使每位学生都有座位的最少移动次数](https://leetcode.cn/problems/minimum-number-of-moves-to-seat-everyone) | EASY | 1 | 1 |
| 2022-12-19 14:07 | [#1971 寻找图中是否存在路径](https://leetcode.cn/problems/find-if-path-exists-in-graph) | EASY | 4 | 1 |
| 2022-12-18 21:25 | [#28 找出字符串中第一个匹配项的下标](https://leetcode.cn/problems/find-the-index-of-the-first-occurrence-in-a-string) | EASY | 1 | 1 |
| 2022-12-17 18:17 | [#1764 通过连接另一个数组的子数组得到一个数组](https://leetcode.cn/problems/form-array-by-concatenating-subarrays-of-another-array) | MEDIUM | 4 | 1 |
| 2022-12-16 12:06 | [#1785 构成特定和需要添加的最少元素](https://leetcode.cn/problems/minimum-elements-to-add-to-form-a-given-sum) | MEDIUM | 2 | 1 |
| 2022-12-15 20:52 | [#21 合并两个有序链表](https://leetcode.cn/problems/merge-two-sorted-lists) | EASY | 1 | 1 |
| 2022-12-15 20:42 | [#LCR 142 训练计划 IV](https://leetcode.cn/problems/he-bing-liang-ge-pai-xu-de-lian-biao-lcof) | EASY | 1 | 1 |
| 2022-12-15 20:23 | [#23 合并 K 个升序链表](https://leetcode.cn/problems/merge-k-sorted-lists) | HARD | 4 | 1 |
| 2022-12-15 11:18 | [#1945 字符串转化后的各位数字之和](https://leetcode.cn/problems/sum-of-digits-of-string-after-convert) | EASY | 3 | 1 |
| 2022-12-13 12:34 | [#24 两两交换链表中的节点](https://leetcode.cn/problems/swap-nodes-in-pairs) | MEDIUM | 4 | 1 |
| 2022-12-13 11:30 | [#1832 判断句子是否为全字母句](https://leetcode.cn/problems/check-if-the-sentence-is-pangram) | EASY | 1 | 1 |
| 2022-12-12 16:15 | [#1781 所有子字符串美丽值之和](https://leetcode.cn/problems/sum-of-beauty-of-all-substrings) | MEDIUM | 1 | 1 |
| 2022-12-11 16:13 | [#1827 最少操作使数组递增](https://leetcode.cn/problems/minimum-operations-to-make-the-array-increasing) | EASY | 1 | 1 |
| 2022-12-10 18:47 | [#1691 堆叠长方体的最大高度](https://leetcode.cn/problems/maximum-height-by-stacking-cuboids) | HARD | 12 | 1 |
| 2022-12-08 09:57 | [#1812 判断国际象棋棋盘中一个格子的颜色](https://leetcode.cn/problems/determine-color-of-a-chessboard-square) | EASY | 2 | 1 |
| 2022-12-07 22:24 | [#1775 通过最少操作次数使数组的和相等](https://leetcode.cn/problems/equal-sum-arrays-with-minimum-number-of-operations) | MEDIUM | 7 | 1 |
| 2022-12-06 18:03 | [#852 山脉数组的峰顶索引](https://leetcode.cn/problems/peak-index-in-a-mountain-array) | MEDIUM | 2 | **2** |
| 2022-12-06 17:43 | [#1805 字符串中不同整数的数目](https://leetcode.cn/problems/number-of-different-integers-in-a-string) | EASY | 5 | 1 |
| 2022-12-05 14:01 | [#8 字符串转换整数 (atoi)](https://leetcode.cn/problems/string-to-integer-atoi) | MEDIUM | 17 | 1 |
| 2022-12-03 10:38 | [#1796 字符串中第二大的数字](https://leetcode.cn/problems/second-largest-digit-in-a-string) | EASY | 4 | 1 |
| 2022-12-02 10:12 | [#1769 移动所有球到每个盒子所需的最小操作数](https://leetcode.cn/problems/minimum-number-of-operations-to-move-all-balls-to-each-box) | MEDIUM | 1 | 1 |
| 2022-12-01 10:32 | [#1779 找到最近的有相同 X 或 Y 坐标的点](https://leetcode.cn/problems/find-nearest-point-that-has-the-same-x-or-y-coordinate) | EASY | 1 | 1 |
| 2022-11-30 15:35 | [#895 最大频率栈](https://leetcode.cn/problems/maximum-frequency-stack) | HARD | 2 | 1 |
| 2022-11-29 18:06 | [#1758 生成交替二进制字符串的最少操作数](https://leetcode.cn/problems/minimum-changes-to-make-alternating-binary-string) | EASY | 1 | 1 |
| 2022-11-28 16:31 | [#813 最大平均值和的分组](https://leetcode.cn/problems/largest-sum-of-averages) | MEDIUM | 3 | 1 |
| 2022-11-27 20:12 | [#1752 检查数组是否经排序和轮转得到](https://leetcode.cn/problems/check-if-array-is-sorted-and-rotated) | EASY | 2 | 1 |
| 2022-11-26 19:10 | [#743 网络延迟时间](https://leetcode.cn/problems/network-delay-time) | MEDIUM | 9 | **5** |
| 2022-11-26 18:56 | [#787 K 站中转内最便宜的航班](https://leetcode.cn/problems/cheapest-flights-within-k-stops) | MEDIUM | 6 | **2** |
| 2022-11-26 16:01 | [#882 细分图中的可到达节点](https://leetcode.cn/problems/reachable-nodes-in-subdivided-graph) | HARD | 2 | 1 |
| 2022-11-26 13:52 | [#809 情感丰富的文字](https://leetcode.cn/problems/expressive-words) | MEDIUM | 2 | 1 |
| 2022-11-24 16:25 | [#19 删除链表的倒数第 N 个结点](https://leetcode.cn/problems/remove-nth-node-from-end-of-list) | MEDIUM | 6 | **2** |
| 2022-11-24 15:52 | [#1668 最大重复子字符串](https://leetcode.cn/problems/maximum-repeating-substring) | EASY | 4 | **2** |
| 2022-11-24 15:03 | [#795 区间子数组个数](https://leetcode.cn/problems/number-of-subarrays-with-bounded-maximum) | MEDIUM | 3 | 1 |
| 2022-11-23 21:31 | [#878 第 N 个神奇数字](https://leetcode.cn/problems/nth-magical-number) | HARD | 9 | **2** |
| 2022-11-23 17:30 | [#1742 盒子中小球的最大数量](https://leetcode.cn/problems/maximum-number-of-balls-in-a-box) | EASY | 1 | 1 |
| 2022-11-21 20:32 | [#18 四数之和](https://leetcode.cn/problems/4sum) | MEDIUM | 4 | 1 |
| 2022-11-21 19:47 | [#16 最接近的三数之和](https://leetcode.cn/problems/3sum-closest) | MEDIUM | 2 | 1 |
| 2022-11-21 18:17 | [#1 两数之和](https://leetcode.cn/problems/two-sum) | EASY | 11 | **2** |
| 2022-11-21 14:35 | [#692 前K个高频单词](https://leetcode.cn/problems/top-k-frequent-words) | MEDIUM | 2 | 1 |
| 2022-11-21 11:04 | [#799 香槟塔](https://leetcode.cn/problems/champagne-tower) | MEDIUM | 2 | 1 |
| 2022-11-19 20:48 | [#139 单词拆分](https://leetcode.cn/problems/word-break) | MEDIUM | 3 | 1 |
| 2022-11-19 16:56 | [#208 实现 Trie (前缀树)](https://leetcode.cn/problems/implement-trie-prefix-tree) | MEDIUM | 2 | 1 |
| 2022-11-19 10:02 | [#1732 找到最高海拔](https://leetcode.cn/problems/find-the-highest-altitude) | EASY | 1 | 1 |
| 2022-11-18 00:48 | [#792 匹配子序列的单词数](https://leetcode.cn/problems/number-of-matching-subsequences) | MEDIUM | 2 | 1 |
| 2022-11-16 13:19 | [#775 全局倒置与局部倒置](https://leetcode.cn/problems/global-and-local-inversions) | MEDIUM | 9 | 1 |
| 2022-11-15 20:30 | [#1926 迷宫中离入口最近的出口](https://leetcode.cn/problems/nearest-exit-from-entrance-in-maze) | MEDIUM | 4 | 1 |
| 2022-11-15 19:11 | [#1710 卡车上的最大单元数](https://leetcode.cn/problems/maximum-units-on-a-truck) | EASY | 2 | 1 |
| 2022-11-14 00:19 | [#704 二分查找](https://leetcode.cn/problems/binary-search) | EASY | 10 | **2** |
| 2022-11-13 17:37 | [#916 单词子集](https://leetcode.cn/problems/word-subsets) | MEDIUM | 4 | 1 |
| 2022-11-13 15:18 | [#LCR 170 交易逆序对的总数](https://leetcode.cn/problems/shu-zu-zhong-de-ni-xu-dui-lcof) | HARD | 3 | **3** |
| 2022-11-13 13:33 | [#791 自定义字符串排序](https://leetcode.cn/problems/custom-sort-string) | MEDIUM | 2 | 1 |
| 2022-11-12 20:54 | [#1339 分裂二叉树的最大乘积](https://leetcode.cn/problems/maximum-product-of-splitted-binary-tree) | MEDIUM | 3 | 1 |
| 2022-11-12 14:18 | [#790 多米诺和托米诺平铺](https://leetcode.cn/problems/domino-and-tromino-tiling) | MEDIUM | 4 | 1 |
| 2022-11-11 13:02 | [#129 求根节点到叶节点数字之和](https://leetcode.cn/problems/sum-root-to-leaf-numbers) | MEDIUM | 3 | 1 |
| 2022-11-11 10:03 | [#1704 判断字符串的两半是否相似](https://leetcode.cn/problems/determine-if-string-halves-are-alike) | EASY | 1 | 1 |
| 2022-11-08 08:26 | [#1684 统计一致字符串的数目](https://leetcode.cn/problems/count-the-number-of-consistent-strings) | EASY | 1 | 1 |
| 2022-11-07 15:37 | [#816 模糊坐标](https://leetcode.cn/problems/ambiguous-coordinates) | MEDIUM | 2 | 1 |
| 2022-11-06 11:38 | [#1678 设计 Goal 解析器](https://leetcode.cn/problems/goal-parser-interpretation) | EASY | 1 | 1 |
| 2022-11-05 18:31 | [#1106 解析布尔表达式](https://leetcode.cn/problems/parsing-a-boolean-expression) | HARD | 3 | 1 |
| 2022-11-04 14:12 | [#754 到达终点数字](https://leetcode.cn/problems/reach-a-number) | MEDIUM | 4 | 1 |
| 2022-11-02 20:43 | [#1620 网络信号最好的坐标](https://leetcode.cn/problems/coordinate-with-maximum-network-quality) | MEDIUM | 1 | 1 |
| 2022-11-01 14:49 | [#1662 检查两个字符串数组是否相等](https://leetcode.cn/problems/check-if-two-string-arrays-are-equivalent) | EASY | 1 | 1 |
| 2022-10-31 10:25 | [#481 神奇字符串](https://leetcode.cn/problems/magical-string) | MEDIUM | 4 | 1 |
| 2022-10-29 23:17 | [#1773 统计匹配检索规则的物品数量](https://leetcode.cn/problems/count-items-matching-a-rule) | EASY | 2 | 1 |
| 2022-10-27 10:20 | [#1822 数组元素积的符号](https://leetcode.cn/problems/sign-of-the-product-of-an-array) | EASY | 2 | 1 |
| 2022-10-24 15:37 | [#1235 规划兼职工作](https://leetcode.cn/problems/maximum-profit-in-job-scheduling) | HARD | 7 | **2** |
| 2022-10-24 08:13 | [#915 分割数组](https://leetcode.cn/problems/partition-array-into-disjoint-intervals) | MEDIUM | 3 | 1 |
| 2022-10-23 18:07 | [#1768 交替合并字符串](https://leetcode.cn/problems/merge-strings-alternately) | EASY | 2 | 1 |
| 2022-10-21 10:50 | [#901 股票价格跨度](https://leetcode.cn/problems/online-stock-span) | MEDIUM | 1 | 1 |
| 2022-10-20 21:51 | [#779 第K个语法符号](https://leetcode.cn/problems/k-th-symbol-in-grammar) | MEDIUM | 1 | 1 |
| 2022-10-19 16:47 | [#1700 无法吃午餐的学生数量](https://leetcode.cn/problems/number-of-students-unable-to-eat-lunch) | EASY | 2 | 1 |
| 2022-10-17 12:25 | [#904 水果成篮](https://leetcode.cn/problems/fruit-into-baskets) | MEDIUM | 3 | 1 |
| 2022-10-16 13:16 | [#886 可能的二分法](https://leetcode.cn/problems/possible-bipartition) | MEDIUM | 4 | 1 |
| 2022-10-15 14:16 | [#7 整数反转](https://leetcode.cn/problems/reverse-integer) | MEDIUM | 4 | 1 |
| 2022-10-15 10:09 | [#1441 用栈操作构建数组](https://leetcode.cn/problems/build-an-array-with-stack-operations) | MEDIUM | 4 | 1 |
| 2022-10-14 16:07 | [#940 不同的子序列 II](https://leetcode.cn/problems/distinct-subsequences-ii) | HARD | 6 | 1 |
| 2022-10-13 20:08 | [#769 最多能完成排序的块](https://leetcode.cn/problems/max-chunks-to-make-sorted) | MEDIUM | 2 | 1 |
| 2022-10-12 10:03 | [#817 链表组件](https://leetcode.cn/problems/linked-list-components) | MEDIUM | 6 | 1 |
| 2022-10-11 10:02 | [#1790 仅执行一次字符串交换能否使两个字符串相等](https://leetcode.cn/problems/check-if-one-string-swap-can-make-strings-equal) | EASY | 3 | 1 |
| 2022-10-10 12:24 | [#856 括号的分数](https://leetcode.cn/problems/score-of-parentheses) | MEDIUM | 2 | 1 |
| 2022-10-08 10:54 | [#870 优势洗牌](https://leetcode.cn/problems/advantage-shuffle) | MEDIUM | 2 | 1 |
| 2022-10-07 12:41 | [#1694 重新格式化电话号码](https://leetcode.cn/problems/reformat-phone-number) | EASY | 2 | 1 |
| 2022-10-07 12:16 | [#1800 最大升序子数组和](https://leetcode.cn/problems/maximum-ascending-subarray-sum) | EASY | 3 | 1 |
| 2022-10-05 12:22 | [#811 子域名访问计数](https://leetcode.cn/problems/subdomain-visit-count) | MEDIUM | 1 | 1 |
| 2022-10-04 22:20 | [#921 使括号有效的最少添加](https://leetcode.cn/problems/minimum-add-to-make-parentheses-valid) | MEDIUM | 4 | 1 |
| 2022-09-30 15:12 | [#73 矩阵置零](https://leetcode.cn/problems/set-matrix-zeroes) | MEDIUM | 1 | 1 |
| 2022-09-30 14:44 | [#面试题 01.08 零矩阵](https://leetcode.cn/problems/zero-matrix-lcci) | MEDIUM | 2 | 1 |
| 2022-09-29 23:57 | [#面试题 17.09 第 k 个数](https://leetcode.cn/problems/get-kth-magic-number-lcci) | MEDIUM | 3 | 1 |
| 2022-09-29 10:16 | [#面试题 01.09 字符串轮转](https://leetcode.cn/problems/string-rotation-lcci) | EASY | 1 | 1 |
| 2022-09-27 22:47 | [#面试题 01.02 判定是否互为字符重排](https://leetcode.cn/problems/check-permutation-lcci) | EASY | 1 | 1 |
| 2022-09-27 11:35 | [#面试题 17.19 消失的两个数字](https://leetcode.cn/problems/missing-two-lcci) | HARD | 3 | 1 |
| 2022-09-26 15:21 | [#788 旋转数字](https://leetcode.cn/problems/rotated-digits) | MEDIUM | 1 | 1 |
| 2022-09-22 09:45 | [#1640 能否连接形成数组](https://leetcode.cn/problems/check-array-formation-through-concatenation) | EASY | 3 | 1 |
| 2022-09-13 15:55 | [#1608 特殊数组的特征值](https://leetcode.cn/problems/special-array-with-x-elements-greater-than-or-equal-x) | EASY | 7 | 1 |
| 2022-09-09 15:29 | [#1598 文件夹操作日志搜集器](https://leetcode.cn/problems/crawler-log-folder) | EASY | 3 | 1 |
| 2022-09-01 13:48 | [#1475 商品折扣后的最终价格](https://leetcode.cn/problems/final-prices-with-a-special-discount-in-a-shop) | EASY | 1 | 1 |
| 2022-08-31 13:22 | [#946 验证栈序列](https://leetcode.cn/problems/validate-stack-sequences) | MEDIUM | 2 | 1 |
| 2022-08-19 12:44 | [#1450 在既定时间做作业的学生人数](https://leetcode.cn/problems/number-of-students-doing-homework-at-a-given-time) | EASY | 1 | 1 |
| 2022-08-17 12:14 | [#1302 层数最深叶子节点的和](https://leetcode.cn/problems/deepest-leaves-sum) | MEDIUM | 1 | 1 |
| 2022-08-10 18:34 | [#640 求解方程](https://leetcode.cn/problems/solve-the-equation) | MEDIUM | 4 | 1 |
| 2022-08-01 12:42 | [#1374 生成每种字符都是奇数个的字符串](https://leetcode.cn/problems/generate-a-string-with-characters-that-have-odd-counts) | EASY | 1 | 1 |
| 2022-07-25 14:34 | [#919 完全二叉树插入器](https://leetcode.cn/problems/complete-binary-tree-inserter) | MEDIUM | 1 | 1 |
| 2022-07-23 14:13 | [#LCR 115 序列重建](https://leetcode.cn/problems/ur2n8P) | MEDIUM | 7 | 1 |
| 2022-07-17 11:09 | [#565 数组嵌套](https://leetcode.cn/problems/array-nesting) | MEDIUM | 1 | 1 |
| 2022-07-14 13:12 | [#745 前缀和后缀搜索](https://leetcode.cn/problems/prefix-and-suffix-search) | HARD | 2 | 1 |
| 2022-07-13 19:22 | [#735 小行星碰撞](https://leetcode.cn/problems/asteroid-collision) | MEDIUM | 11 | 1 |
| 2022-07-11 13:05 | [#676 实现一个魔法字典](https://leetcode.cn/problems/implement-magic-dictionary) | MEDIUM | 2 | 1 |
| 2022-07-08 13:51 | [#1217 玩筹码](https://leetcode.cn/problems/minimum-cost-to-move-chips-to-the-same-position) | EASY | 1 | 1 |
| 2022-07-07 15:38 | [#648 单词替换](https://leetcode.cn/problems/replace-words) | MEDIUM | 3 | 1 |
| 2022-07-05 11:23 | [#729 我的日程安排表 I](https://leetcode.cn/problems/my-calendar-i) | MEDIUM | 8 | 1 |
| 2022-07-04 10:40 | [#1200 最小绝对差](https://leetcode.cn/problems/minimum-absolute-difference) | EASY | 2 | 1 |
| 2022-07-03 20:08 | [#556 下一个更大元素 III](https://leetcode.cn/problems/next-greater-element-iii) | MEDIUM | 1 | 1 |
| 2022-06-24 13:38 | [#515 在每个树行中找最大值](https://leetcode.cn/problems/find-largest-value-in-each-tree-row) | MEDIUM | 1 | 1 |
| 2022-06-22 14:33 | [#513 找树左下角的值](https://leetcode.cn/problems/find-bottom-left-tree-value) | MEDIUM | 4 | 1 |
| 2022-06-21 19:28 | [#1108 IP 地址无效化](https://leetcode.cn/problems/defanging-an-ip-address) | EASY | 2 | 1 |
| 2022-06-19 23:06 | [#98 验证二叉搜索树](https://leetcode.cn/problems/validate-binary-search-tree) | MEDIUM | 13 | 1 |
| 2022-06-19 15:20 | [#508 出现次数最多的子树元素和](https://leetcode.cn/problems/most-frequent-subtree-sum) | MEDIUM | 2 | 1 |
| 2022-06-18 14:19 | [#LCR 029 循环有序列表的插入](https://leetcode.cn/problems/4ueAj6) | MEDIUM | 15 | 1 |
| 2022-06-17 15:48 | [#1089 复写零](https://leetcode.cn/problems/duplicate-zeros) | EASY | 2 | 1 |
| 2022-06-13 23:05 | [#1051 高度检查器](https://leetcode.cn/problems/height-checker) | EASY | 2 | 1 |
| 2022-06-12 23:05 | [#890 查找和替换模式](https://leetcode.cn/problems/find-and-replace-pattern) | MEDIUM | 1 | 1 |
| 2022-06-05 14:59 | [#478 在圆内随机生成点](https://leetcode.cn/problems/generate-random-point-in-a-circle) | MEDIUM | 8 | 1 |
| 2022-06-04 12:34 | [#929 独特的电子邮件地址](https://leetcode.cn/problems/unique-email-addresses) | EASY | 5 | 1 |
| 2022-05-30 20:32 | [#1022 从根到叶的二进制数之和](https://leetcode.cn/problems/sum-of-root-to-leaf-binary-numbers) | EASY | 3 | 1 |
| 2022-05-28 12:21 | [#1021 删除最外层的括号](https://leetcode.cn/problems/remove-outermost-parentheses) | EASY | 1 | 1 |
| 2022-05-27 17:40 | [#面试题 17.11 单词距离](https://leetcode.cn/problems/find-closest-lcci) | MEDIUM | 2 | 1 |
| 2022-05-24 12:35 | [#965 单值二叉树](https://leetcode.cn/problems/univalued-binary-tree) | EASY | 2 | 1 |
| 2022-05-21 17:47 | [#961 在长度 2N 的数组中找出重复 N 次的元素](https://leetcode.cn/problems/n-repeated-element-in-size-2n-array) | EASY | 2 | 1 |
| 2022-05-20 14:55 | [#436 寻找右区间](https://leetcode.cn/problems/find-right-interval) | MEDIUM | 3 | 1 |
| 2022-05-19 13:50 | [#462 最小操作次数使数组元素相等 II](https://leetcode.cn/problems/minimum-moves-to-equal-array-elements-ii) | MEDIUM | 1 | 1 |
| 2022-05-18 13:08 | [#668 乘法表中第k小的数](https://leetcode.cn/problems/kth-smallest-number-in-multiplication-table) | HARD | 3 | 1 |
| 2022-05-17 11:08 | [#953 验证外星语词典](https://leetcode.cn/problems/verifying-an-alien-dictionary) | EASY | 2 | 1 |
| 2022-05-16 16:08 | [#面试题 04.06 后继者](https://leetcode.cn/problems/successor-lcci) | MEDIUM | 5 | 1 |
| 2022-05-15 14:35 | [#812 最大三角形面积](https://leetcode.cn/problems/largest-triangle-area) | EASY | 4 | 1 |
| 2022-05-13 22:09 | [#102 二叉树的层序遍历](https://leetcode.cn/problems/binary-tree-level-order-traversal) | MEDIUM | 3 | 1 |
| 2022-05-13 13:28 | [#面试题 01.05 一次编辑](https://leetcode.cn/problems/one-away-lcci) | MEDIUM | 3 | 1 |
| 2022-05-12 21:36 | [#944 删列造序](https://leetcode.cn/problems/delete-columns-to-make-sorted) | EASY | 2 | 1 |
| 2022-05-10 15:12 | [#210 课程表 II](https://leetcode.cn/problems/course-schedule-ii) | MEDIUM | 2 | 1 |
| 2022-05-09 14:49 | [#107 二叉树的层序遍历 II](https://leetcode.cn/problems/binary-tree-level-order-traversal-ii) | MEDIUM | 2 | 1 |
| 2022-05-09 14:35 | [#117 填充每个节点的下一个右侧节点指针 II](https://leetcode.cn/problems/populating-next-right-pointers-in-each-node-ii) | MEDIUM | 1 | 1 |
| 2022-05-09 14:32 | [#116 填充每个节点的下一个右侧节点指针](https://leetcode.cn/problems/populating-next-right-pointers-in-each-node) | MEDIUM | 2 | 1 |
| 2022-05-09 13:49 | [#942 增减字符串匹配](https://leetcode.cn/problems/di-string-match) | EASY | 1 | 1 |
| 2022-05-08 10:22 | [#442 数组中重复的数据](https://leetcode.cn/problems/find-all-duplicates-in-an-array) | MEDIUM | 1 | 1 |
| 2022-05-07 20:21 | [#207 课程表](https://leetcode.cn/problems/course-schedule) | MEDIUM | 2 | 1 |
| 2022-05-07 16:37 | [#433 最小基因变化](https://leetcode.cn/problems/minimum-genetic-mutation) | MEDIUM | 3 | 1 |
| 2022-05-06 15:00 | [#113 路径总和 II](https://leetcode.cn/problems/path-sum-ii) | MEDIUM | 1 | 1 |
| 2022-05-06 14:46 | [#933 最近的请求次数](https://leetcode.cn/problems/number-of-recent-calls) | EASY | 1 | 1 |
| 2022-05-05 11:07 | [#713 乘积小于 K 的子数组](https://leetcode.cn/problems/subarray-product-less-than-k) | MEDIUM | 3 | 1 |
| 2022-05-04 12:31 | [#1823 找出游戏的获胜者](https://leetcode.cn/problems/find-the-winner-of-the-circular-game) | MEDIUM | 2 | 1 |
| 2022-05-03 12:37 | [#937 重新排列日志文件](https://leetcode.cn/problems/reorder-data-in-log-files) | MEDIUM | 2 | 1 |
| 2022-05-02 15:00 | [#591 标签验证器](https://leetcode.cn/problems/tag-validator) | HARD | 8 | 1 |
| 2022-05-02 14:17 | [#796 旋转字符串](https://leetcode.cn/problems/rotate-string) | EASY | 4 | **2** |
| 2022-05-01 17:59 | [#1305 两棵二叉搜索树中的所有元素](https://leetcode.cn/problems/all-elements-in-two-binary-search-trees) | MEDIUM | 3 | 1 |
| 2022-04-30 14:28 | [#908 最小差值 I](https://leetcode.cn/problems/smallest-range-i) | EASY | 6 | 1 |
| 2022-04-29 15:45 | [#427 建立四叉树](https://leetcode.cn/problems/construct-quad-tree) | MEDIUM | 1 | 1 |
| 2022-04-28 12:36 | [#905 按奇偶排序数组](https://leetcode.cn/problems/sort-array-by-parity) | EASY | 2 | 1 |
| 2022-04-26 19:39 | [#883 三维形体投影面积](https://leetcode.cn/problems/projection-area-of-3d-shapes) | EASY | 2 | 1 |
| 2022-04-25 12:52 | [#398 随机数索引](https://leetcode.cn/problems/random-pick-index) | MEDIUM | 2 | 1 |
| 2022-04-24 13:08 | [#868 二进制间距](https://leetcode.cn/problems/binary-gap) | EASY | 1 | 1 |
| 2022-04-22 15:01 | [#396 旋转函数](https://leetcode.cn/problems/rotate-function) | MEDIUM | 2 | 1 |
| 2022-04-21 13:01 | [#824 山羊拉丁文](https://leetcode.cn/problems/goat-latin) | EASY | 1 | 1 |
| 2022-04-20 14:44 | [#388 文件的最长绝对路径](https://leetcode.cn/problems/longest-absolute-file-path) | MEDIUM | 2 | 1 |
| 2022-04-19 12:26 | [#821 字符的最短距离](https://leetcode.cn/problems/shortest-distance-to-a-character) | EASY | 1 | 1 |
| 2022-04-18 15:36 | [#386 字典序排数](https://leetcode.cn/problems/lexicographical-numbers) | MEDIUM | 2 | 1 |
| 2022-04-17 13:28 | [#819 最常见的单词](https://leetcode.cn/problems/most-common-word) | EASY | 3 | 1 |
| 2022-04-16 12:46 | [#479 最大回文数乘积](https://leetcode.cn/problems/largest-palindrome-product) | HARD | 2 | 1 |
| 2022-04-15 15:05 | [#385 迷你语法分析器](https://leetcode.cn/problems/mini-parser) | MEDIUM | 4 | 1 |
| 2022-04-14 10:21 | [#1672 最富有客户的资产总量](https://leetcode.cn/problems/richest-customer-wealth) | EASY | 1 | 1 |
| 2022-04-13 18:53 | [#380 O(1) 时间插入、删除和获取随机元素](https://leetcode.cn/problems/insert-delete-getrandom-o1) | MEDIUM | 5 | 1 |
| 2022-04-12 10:06 | [#806 写字符串需要的行数](https://leetcode.cn/problems/number-of-lines-to-write-string) | EASY | 1 | 1 |
| 2022-04-11 15:05 | [#357 统计各位数字都不同的数字个数](https://leetcode.cn/problems/count-numbers-with-unique-digits) | MEDIUM | 1 | 1 |
| 2022-04-10 12:27 | [#804 唯一摩尔斯密码词](https://leetcode.cn/problems/unique-morse-code-words) | EASY | 1 | 1 |
| 2022-04-09 18:33 | [#780 到达终点](https://leetcode.cn/problems/reaching-points) | HARD | 6 | 1 |
| 2022-04-08 11:24 | [#429 N 叉树的层序遍历](https://leetcode.cn/problems/n-ary-tree-level-order-traversal) | MEDIUM | 2 | 1 |
| 2022-04-06 14:13 | [#310 最小高度树](https://leetcode.cn/problems/minimum-height-trees) | MEDIUM | 1 | 1 |
| 2022-04-05 15:42 | [#762 二进制表示中质数个计算置位](https://leetcode.cn/problems/prime-number-of-set-bits-in-binary-representation) | EASY | 3 | 1 |
| 2022-04-03 20:29 | [#744 寻找比目标字母大的最小字母](https://leetcode.cn/problems/find-smallest-letter-greater-than-target) | EASY | 8 | 1 |
| 2022-04-02 18:50 | [#132 分割回文串 II](https://leetcode.cn/problems/palindrome-partitioning-ii) | HARD | 4 | 1 |
| 2022-04-01 11:41 | [#954 二倍数对数组](https://leetcode.cn/problems/array-of-doubled-pairs) | MEDIUM | 10 | 1 |
| 2022-03-31 12:57 | [#728 自除数](https://leetcode.cn/problems/self-dividing-numbers) | EASY | 1 | 1 |
| 2022-03-30 17:45 | [#1606 找到处理最多请求的服务器](https://leetcode.cn/problems/find-servers-that-handled-most-number-of-requests) | HARD | 6 | 1 |
| 2022-03-29 13:49 | [#2024 考试的最大困扰度](https://leetcode.cn/problems/maximize-the-confusion-of-an-exam) | MEDIUM | 1 | 1 |
| 2022-03-28 14:22 | [#693 交替位二进制数](https://leetcode.cn/problems/binary-number-with-alternating-bits) | EASY | 1 | 1 |
| 2022-03-27 12:46 | [#2028 找出缺失的观测数据](https://leetcode.cn/problems/find-missing-observations) | MEDIUM | 7 | 1 |
| 2022-03-26 15:02 | [#682 棒球比赛](https://leetcode.cn/problems/baseball-game) | EASY | 1 | 1 |
| 2022-03-25 13:23 | [#172 阶乘后的零](https://leetcode.cn/problems/factorial-trailing-zeroes) | MEDIUM | 4 | 1 |
| 2022-03-24 10:20 | [#661 图片平滑器](https://leetcode.cn/problems/image-smoother) | EASY | 1 | 1 |
| 2022-03-23 18:40 | [#440 字典序的第K小数字](https://leetcode.cn/problems/k-th-smallest-in-lexicographical-order) | HARD | 6 | 1 |
| 2022-03-22 12:43 | [#2038 如果相邻两个颜色均相同则删除当前颜色](https://leetcode.cn/problems/remove-colored-pieces-if-both-neighbors-are-the-same-color) | MEDIUM | 3 | 1 |
| 2022-03-21 15:27 | [#653 两数之和 IV - 输入二叉搜索树](https://leetcode.cn/problems/two-sum-iv-input-is-a-bst) | EASY | 1 | 1 |
| 2022-03-20 15:10 | [#2039 网络空闲的时刻](https://leetcode.cn/problems/the-time-when-the-network-becomes-idle) | MEDIUM | 1 | 1 |
| 2022-03-19 15:00 | [#606 根据二叉树创建字符串](https://leetcode.cn/problems/construct-string-from-binary-tree) | MEDIUM | 3 | 1 |
| 2022-03-18 12:11 | [#2043 简易银行系统](https://leetcode.cn/problems/simple-bank-system) | MEDIUM | 1 | 1 |
| 2022-03-17 14:57 | [#720 词典中最长的单词](https://leetcode.cn/problems/longest-word-in-dictionary) | MEDIUM | 8 | 1 |
| 2022-03-16 19:29 | [#432 全 O(1) 的数据结构](https://leetcode.cn/problems/all-oone-data-structure) | HARD | 4 | 1 |
| 2022-03-15 15:21 | [#2044 统计按位或能得到最大值的子集数目](https://leetcode.cn/problems/count-number-of-maximum-bitwise-or-subsets) | MEDIUM | 6 | 1 |
| 2022-03-14 11:27 | [#599 两个列表的最小索引总和](https://leetcode.cn/problems/minimum-index-sum-of-two-lists) | EASY | 2 | 1 |
| 2022-03-13 16:05 | [#393 UTF-8 编码验证](https://leetcode.cn/problems/utf-8-validation) | MEDIUM | 10 | 1 |
| 2022-03-12 13:21 | [#590 N 叉树的后序遍历](https://leetcode.cn/problems/n-ary-tree-postorder-traversal) | EASY | 1 | 1 |
| 2021-09-14 15:09 | [#524 通过删除字母匹配到字典里最长单词](https://leetcode.cn/problems/longest-word-in-dictionary-through-deleting) | MEDIUM | 3 | 1 |
| 2021-08-03 13:57 | [#581 最短无序连续子数组](https://leetcode.cn/problems/shortest-unsorted-continuous-subarray) | MEDIUM | 8 | 1 |
| 2021-07-30 19:34 | [#171 Excel 表列序号](https://leetcode.cn/problems/excel-sheet-column-number) | EASY | 5 | 1 |
| 2021-07-13 09:53 | [#40 组合总和 II](https://leetcode.cn/problems/combination-sum-ii) | MEDIUM | 3 | 1 |
| 2021-07-12 19:52 | [#714 买卖股票的最佳时机含手续费](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-with-transaction-fee) | MEDIUM | 1 | 1 |
| 2021-07-12 18:59 | [#740 删除并获得点数](https://leetcode.cn/problems/delete-and-earn) | MEDIUM | 1 | 1 |
| 2021-07-06 16:21 | [#746 使用最小花费爬楼梯](https://leetcode.cn/problems/min-cost-climbing-stairs) | EASY | 1 | 1 |
| 2021-07-05 15:44 | [#120 三角形最小路径和](https://leetcode.cn/problems/triangle) | MEDIUM | 2 | 1 |
| 2021-07-05 14:12 | [#55 跳跃游戏](https://leetcode.cn/problems/jump-game) | MEDIUM | 4 | 1 |
| 2021-07-05 13:41 | [#45 跳跃游戏 II](https://leetcode.cn/problems/jump-game-ii) | MEDIUM | 15 | 1 |
| 2021-07-05 12:31 | [#509 斐波那契数](https://leetcode.cn/problems/fibonacci-number) | EASY | 2 | 1 |
| 2021-07-02 15:38 | [#1833 雪糕的最大数量](https://leetcode.cn/problems/maximum-ice-cream-bars) | MEDIUM | 4 | 1 |
| 2021-06-15 10:56 | [#33 搜索旋转排序数组](https://leetcode.cn/problems/search-in-rotated-sorted-array) | MEDIUM | 1 | 1 |
| 2021-06-13 15:46 | [#278 第一个错误的版本](https://leetcode.cn/problems/first-bad-version) | EASY | 4 | 1 |
| 2021-06-04 09:26 | [#160 相交链表](https://leetcode.cn/problems/intersection-of-two-linked-lists) | EASY | 7 | 1 |
| 2021-05-24 16:52 | [#130 被围绕的区域](https://leetcode.cn/problems/surrounded-regions) | MEDIUM | 4 | **2** |
| 2021-05-24 11:09 | [#547 省份数量](https://leetcode.cn/problems/number-of-provinces) | MEDIUM | 1 | 1 |
| 2021-05-22 00:06 | [#695 岛屿的最大面积](https://leetcode.cn/problems/max-area-of-island) | MEDIUM | 3 | 1 |
| 2021-05-21 14:21 | [#200 岛屿数量](https://leetcode.cn/problems/number-of-islands) | MEDIUM | 1 | 1 |
| 2021-05-10 15:31 | [#872 叶子相似的树](https://leetcode.cn/problems/leaf-similar-trees) | EASY | 7 | 1 |
| 2021-05-05 10:53 | [#154 寻找旋转排序数组中的最小值 II](https://leetcode.cn/problems/find-minimum-in-rotated-sorted-array-ii) | HARD | 1 | 1 |
| 2021-05-05 10:49 | [#LCR 128 库存管理 I](https://leetcode.cn/problems/xuan-zhuan-shu-zu-de-zui-xiao-shu-zi-lcof) | EASY | 2 | **2** |
| 2021-04-13 18:39 | [#783 二叉搜索树节点最小距离](https://leetcode.cn/problems/minimum-distance-between-bst-nodes) | EASY | 1 | 1 |
| 2021-03-30 13:37 | [#74 搜索二维矩阵](https://leetcode.cn/problems/search-a-2d-matrix) | MEDIUM | 1 | 1 |
| 2021-03-27 22:24 | [#61 旋转链表](https://leetcode.cn/problems/rotate-list) | MEDIUM | 3 | 1 |
| 2021-03-22 18:57 | [#191 位1的个数](https://leetcode.cn/problems/number-of-1-bits) | EASY | 1 | 1 |
| 2020-11-27 20:12 | [#454 四数相加 II](https://leetcode.cn/problems/4sum-ii) | MEDIUM | 5 | 1 |
| 2020-11-25 22:35 | [#1370 上升下降字符串](https://leetcode.cn/problems/increasing-decreasing-string) | EASY | 1 | 1 |
| 2020-10-25 19:58 | [#845 数组中的最长山脉](https://leetcode.cn/problems/longest-mountain-in-array) | MEDIUM | 1 | 1 |
| 2020-10-15 20:52 | [#9 回文数](https://leetcode.cn/problems/palindrome-number) | EASY | 1 | 1 |
| 2020-09-04 13:05 | [#257 二叉树的所有路径](https://leetcode.cn/problems/binary-tree-paths) | EASY | 1 | 1 |
| 2020-08-16 15:28 | [#733 图像渲染](https://leetcode.cn/problems/flood-fill) | EASY | 2 | 1 |
| 2020-08-14 23:14 | [#20 有效的括号](https://leetcode.cn/problems/valid-parentheses) | EASY | 6 | 1 |
| 2020-08-10 14:09 | [#696 计数二进制子串](https://leetcode.cn/problems/count-binary-substrings) | EASY | 4 | 1 |
| 2020-08-08 09:45 | [#99 恢复二叉搜索树](https://leetcode.cn/problems/recover-binary-search-tree) | MEDIUM | 1 | 1 |
| 2020-08-06 16:44 | [#495 提莫攻击](https://leetcode.cn/problems/teemo-attacking) | EASY | 2 | 1 |
| 2020-08-03 20:36 | [#415 字符串相加](https://leetcode.cn/problems/add-strings) | EASY | 6 | 1 |
| 2020-07-31 13:43 | [#面试题 17.01 不用加号的加法](https://leetcode.cn/problems/add-without-plus-lcci) | EASY | 1 | 1 |
| 2020-07-31 13:05 | [#面试题 08.03 魔术索引](https://leetcode.cn/problems/magic-index-lcci) | EASY | 2 | 1 |
| 2020-07-29 10:05 | [#12 整数转罗马数字](https://leetcode.cn/problems/integer-to-roman) | MEDIUM | 1 | 1 |
| 2020-07-28 18:48 | [#104 二叉树的最大深度](https://leetcode.cn/problems/maximum-depth-of-binary-tree) | EASY | 1 | 1 |
| 2020-07-27 10:32 | [#392 判断子序列](https://leetcode.cn/problems/is-subsequence) | EASY | 8 | 1 |
| 2020-07-23 15:55 | [#2 两数相加](https://leetcode.cn/problems/add-two-numbers) | MEDIUM | 5 | 1 |
| 2020-07-23 14:37 | [#344 反转字符串](https://leetcode.cn/problems/reverse-string) | EASY | 5 | 1 |
| 2020-07-23 14:15 | [#64 最小路径和](https://leetcode.cn/problems/minimum-path-sum) | MEDIUM | 6 | 1 |
| 2020-07-20 14:17 | [#167 两数之和 II - 输入有序数组](https://leetcode.cn/problems/two-sum-ii-input-array-is-sorted) | MEDIUM | 1 | 1 |
| 2020-07-18 23:56 | [#97 交错字符串](https://leetcode.cn/problems/interleaving-string) | MEDIUM | 4 | 1 |
| 2020-07-17 16:01 | [#35 搜索插入位置](https://leetcode.cn/problems/search-insert-position) | EASY | 7 | 1 |
| 2020-04-22 22:11 | [#17 电话号码的字母组合](https://leetcode.cn/problems/letter-combinations-of-a-phone-number) | MEDIUM | 3 | 1 |
