# 并查集（Union-Find）

一种树型的数据结构，用于处理一些不交集（Disjoint Sets）的合并及查询问题。不交集指的是一系列没有重复元素的集合。主要是支持两种操作：

- **合并（Union）**：将两个集合合并成一个集合。
- **查找（Find）**：确定某个元素属于哪个集合。通常是返回集合内的一个「代表元素」。

```go
type unionFind struct {
	father []int
}

func (u unionFind) init(nums []int) {
	for i := range nums {
		u.father[i] = i
	}
}

func (u unionFind) find(x int) int {
	if u.father[x] == x {
		return x
	}
	root := u.find(u.father[x]) // 状态压缩，找到根节点，而不是一层一层找父节点
	u.father[x] = root
	return root
}
func (u unionFind) union(x, y int) {
	xRoot, yRoot := u.find(x), u.find(y)
	if xRoot != yRoot {
		u.father[yRoot] = xRoot
	}
}
```

