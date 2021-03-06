# Code of Conduct

在和XLA中的各位交流时请注意: 我们都只是志愿者, 可能并没有时间做到太多,
所以对讲师的疏忽请多多包涵; 同时, 每个人都是从小白开始的, 对学员也请多点耐心 ><

在添加课程的时候请注意:

- 请尽量使用最新的和被广泛承认的标准.
  如果某个特性没有被广泛(以使用范围计)支持, 请注明.

  例如:
  - 对于lisp的语言课程, 选择scheme(r7rs/r5rs/racket)或者common lisp, 而非loli-lang;
  - 对于C++的语言课程, 假设现在是2020年, 在介绍concepts, coroutines, modules这些特性的时候,
    说明三大主流编译器对其中至少一个特性的支持缺失或不完整;
  - 对于数学课程, 假设现在是2021年, 介绍黎曼猜想时不要当作定理介绍;
    如果可能的话, 也注明当前验证过的所有值都满足这一猜想.

- 请尽量更新README以使得README中的介绍与实际的课程内容相符.

  例如, 如果c10s添加了Rust教程而忘记在`lang/README.md`的语言列表中添加Rust,
  请让c10s `commit --amend && push -f` x.

- 请正确地在README中和各个讲义中添加课程(组)的依赖信息,
  只需要添加这一课程里用到的知识, 间接依赖的课程不用给出;
  同时尽量减少课程的拓扑树上的节点层数.
  编号也请按照依赖关系正确编号, 尽量使得课程的所有依赖均拥有小于它的编号.
  如果有依赖环, 依赖信息仍然需要标出, 编号时可以任意忽略环里的一条依赖.

  例如:
  - 按照目前计划, 我们的所有语言课程都依赖js/python课程,
    请在每个语言课程的第一课里注明这个;
  - 算法课程很可能会依赖语言课程, 所以算法课程组的README里要加上依赖语言课程的说明,
    不过单个算法课程和算法课程组下的课程组不需要说明这个;
  - 在算法课程中, 各种具体的平衡树算法依赖平衡树/BST的课程,
    所以课程编号大于平衡树/BST的, 但是它们之间不会相互依赖, 也不会与其它课程有太复杂的关系,
    所以可以使用相同的课程编号.

