虚线包含的部分就是各子树，由上到下各层的前缀分别为 0，01，000，0010。
> 按照上文的理解：对于任意一个节点，都可以把这颗二叉树分解为一系列连续的，不包含自己的子树。最高层的子树，由整颗树不包含自己的树的另一半组成； 下一层子树由剩下部分不包含自己的一半组成；依此类推，直到分割完整颗树。

虚线包含的部分就是各子树，由上到下各层的前缀分别为 1，01，000，0010。

每一个这样的列表都称之为一个 K 桶，并且每个 K 桶内部信息存放位置是根据上次看到的时间顺序排列，最近（least-recently）看到的放在头部，最后（most-recently）看到的放在尾部。每个桶都有不超过 k 个的数据项。
> 最近（least-recently）与最后（most-recently）的翻译，会产生歧义

最近最少（least-recently）访问的节点放在队列头，最近最多（most-recently）访问的节点放在队列尾部。以模拟gnutella用户行为分析的结果，最近最多访问的活跃节点，也是将来最有可能需要访问的节点