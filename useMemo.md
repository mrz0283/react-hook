#### useMemo

`shouldComponentUpdate`类似作用,在渲染过程中避免重复渲染
当状态或父组件传来的属性值发生变化时，更新组件


1、`useMemo`就是用`memoization`提高性能
   Memoization 的原理就是把函数的每次执行结果都放入一个对象中，在接下来的执行中，在对象中查找是否已经有相应执行过的值，如果有，直接返回该值，没有才真正执行函数体的求值部分。在对象里找值是要比执行函数的速度要快的。
2、`memoization`是`JavaScript`中的一种缓存技术
如果有CPU密集型操作,可以通过将初始化操作的结果存储在缓存中来优化使用,如果操作必然执行,将不再使用CPU,因为相同的结果存储在某个地方,只是进行返回
                   //   牺牲空间换取速度   //
                   
                  
`useMemo()`是一个函数,有两个参数,第一个参数是函数,第二个参数是数组
`useMemo(()=>{},[默认可以不写])`
useMemo和useEffect执行的时间不同,useEffect是componentDidMount以后执行的,而useMemo是在组件渲染过程中执行的
