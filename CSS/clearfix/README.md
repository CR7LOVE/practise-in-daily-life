一共展示了 3 个 demo：
1. clear-failure，即清除失败
2. clear-success, 即清除成功
3. pseudo-elements，即利用伪元素进行清除

这也就解释了 3 中利用伪元素清除浮动时多了一个 display: table 属性。
在这里还有2个问题：

结论：
1. inline 元素不能清除浮动，block 或者 inline-block 元素才可以（1 VS 2 即知）
2. 利用伪元素清除浮动从根本上讲是模仿 2 中 div 的 clear: both 的
3. 伪元素添加 display 属性，从侧面印证了伪元素是 inline，这可以通过查看控制台中盒模型可知。    
4. 利用伪元素清除浮动时必须要加一个 display 属性，值是 block 或 table 或 inline-block 都可以，但是 inline 就不行。 
    span, i, a 清除失败均是由于此三元素的 display 的值是 inline 导致。
   