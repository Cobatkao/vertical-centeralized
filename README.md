# 碎碎念

互联网上关于垂直居中的文章和总结太多了，代码和表述水平层次不齐。常常看过一遍就会忘记，好记性不如烂笔头，还是少说点废话，直接都实现一遍，供日后复看！

以下针对是否已知**居中元素宽高**进行分类

# 已知固定宽高

1. [absolute + negative margin](http://isaacgao.cn/vertical-centeralized/1st_absolute_negative_margin.html)
2. [absolute + calc()](http://isaacgao.cn/vertical-centeralized/3nd_absolute_calc.html)
  
    `calc`可以少写两个样式，但是它是CSS3属性，[兼容性较差](https://caniuse.com/#search=calc)，IE目前仅兼容到IE11，firefox，chrome，safari都完美兼容。
3. [absolute + margin: auto](http://isaacgao.cn/vertical-centeralized/2nd_absolute_margin_auto.html)

如上三种方法，都是利用定位将元素左上角顶点移动到视窗中心，然后利用负margin，使居中元素中心点与视窗中心点重合，达到水平垂直居中；



# 未知宽高

1. [absolute_transform](http://isaacgao.cn/vertical-centeralized/4nd_absolute_transform.html)

    `translate()`属性中的百分比是相对于居中元素自身，因此可以做到居中。
2. [vh + translateY](http://isaacgao.cn/vertical-centeralized/5nd_viewport_relative.html)

    仅适用于元素在视窗中垂直居中，因为vh是相对于视窗的高度。
3. [flex](http://isaacgao.cn/vertical-centeralized/6nd_flex_box.html)

    最简单的方法，**推荐！现代化的布局方案。**
4. [table](http://isaacgao.cn/vertical-centeralized/8nd_table.html)
  
    古老的页面布局方式，可以实现水平垂直居中，但是会增加很多冗余代码。
5. [table-cell + 文本排版式](http://isaacgao.cn/vertical-centeralized/7nd_text_like.html)
  
    文本式单独拆开来其实就是`inline-block`水平居中方案以及`table-cell`垂直居中方案的合用，也算是把文本排版的特性都利用了个遍了。




