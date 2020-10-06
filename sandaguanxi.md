组合has-a

组合关系下的构造和析构，Container类的数据成员是Component类的对象

构造由内而外，Container的构造函数首先调用Component的default的默认构造函数，再执行自己的。

```C++
Container::Container(...): Component() {...}; //初始化列表中调用
```

析构由内而外，Container的析构函数先执行自己的，再调用Component的析构函数。

```C++
Container::~Container(...) {... ~Component};
```

