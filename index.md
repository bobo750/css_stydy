```css
/* @import url(./common/index.css); */
/**层叠样式表*/
body{
    /* background-color: red; */
}
*{/**1.全部选择器 
    css的注释，自己考虑是否使用  
    分号结尾千万注意  */
    color: red;
}
a{
    /**2.标签选择器 作用范围较广 这里是取消下划线*/
    /* text-decoration-line: none; */
}
.success{
    /**3.类选择器 可重复出现*/
    border:1px solid green;
    color:green;
}
.success2 {
    /** 3.1选择器中允许使用多个样式*/
    margin-bottom: 10px;
}
#error{
     /**4.id选择器 建议是唯一的， 
            在不同浏览器中多个id也可能会有样式显示，但不同浏览器加载可能会有问题，且对js的相关操作不利 
            作用范围小，不建议用id来定义样式*/
    border:1px solid red;
    color:red;
}
main article h1{
    /** 5.1结构选择器 后代选择器 波及范围较广*/
    color:red;
}
article >h2{
    /**5.2子元素选择器 只管自己的孩子*/
    color: green;
}
article h1~h1{
    /**5.3 h1后面的兄弟元素是h1的标签 后面所有的都会影响 */
    color: yellow;
}
article h1+h1{
    /**5.4 h1后面的 紧挨着的 兄弟元素是h1的标签 */
    color: orange;
}

h3[title]{
    /**6.1 属性选择器含有某个或某几个属性的*/
    color:gray;
}
h3[title][id]{
    /**6.1 属性选择器含有某个或某几个属性的*/
    color:green;
}
h3[title='djifdid']{
    /**6.2 属性为某值时*/
    color:red;
}
h3[title^='jifdi']{
    /**6.3 属性为某值开头  与正则类似*/
    color:orange;
}
h3[title$='jifdi']{
    /**6.4 属性为某值结尾*/
    color:orangered;
}
/* h3[title*='jifdi']{ */
    /**6.5 属性任意位置含有某值*/
    /* color:yellow;
} */
h3[title~='jifdi']{
    /**6.6 属性任意位置含有某值,但必须是隔离存在的*/
    color:salmon;
}
h3[title|='jifdi']{
    /**6.7 属性任意位置含有某值,但必须是以其开头或是以‘-’在后面连接的*/
    color:sienna;
}
a:link{
    /**7.1伪类选择器，默认状态*/
    color:green;
}
a:visited{
    /**7.2伪类选择器，点击之后*/
    color:orange;
}
a:hover{
    /**7.3伪类选择器，浮动在上面*/
    color:blue;
}
a:active{
    /**7.4伪类选择器，点击一瞬间*/
    color:black;
}
input:focus{
     /**7.5伪类选择器，扩展，每个标签可能适用的选择器不一样，要夺取尝试，建议使用第三方的ui插件*/
    background:red;
    outline: none;
}
input:hover{
    /**7.5伪类选择器，扩展，每个标签可能适用的选择器不一样，要夺取尝试，建议使用第三方的ui插件*/
   background:yellow;
}
input:active{
    /**7.5伪类选择器，扩展，每个标签可能适用的选择器不一样，要夺取尝试，建议使用第三方的ui插件*/
   background:black;
}
div{
    /*8锚点可以跳转到指定id的位置*/
    height: 300px;
}
div:target{
    /**8.1一般与锚点配合使用，跳转到的地方的样式变换*/
    color:black;
}
/* html{
    background:red;
} */
:root{
    /**7.6根目录的伪类选择器，与html标签的效果一样*/
    background:red;
}
div[id='faklf']{
    background:red;
    height: 190px;
    border: 1px solid black;
}
div:empty{
    /**7.7空元素的伪类选择器，可以跟在标签后面*/
    display: none;
}
article:first-child{
    /**7.8 article后代中的第一个的样式，包括孙子辈的第一个。。。*/
    color:red;
}
article>:first-child{
    /**7.9 article后代中的第一个的样式，限于儿子辈*/
    color:red;
}
article h1:first-child{
    /**7.10 article后代中的同代所有元素第一个是h1的样式，不是h1的选不中 
    与之对应的是  last-child
    */
    color:red;
}
article h1:first-child{
    /**7.10 article后代中的所有元素第一个是h1的样式，第一个不是h1，则都不选中*/
    color:red;
}
article h1:first-of-type{
    /**7.10 article后代中的第一个是h1的样式，按h1样式选第一个h1样式类型的
    与之对应的是  last-of-type
    */
    color:red;
}
article:only-child{
    /*7.11 唯一选择 后代有唯一儿子的样式*/
    color:red;
}
article >h1:only-of-type{
    /*7.11 选择子元素唯一h1的样式*/
    color:red;
}
article :nth-child(1){
    /*7.12 从中间 后代中的第一个，包括孙子辈等。。*/
    color:red;
}
article >:nth-child(1){
    /*7.12 从中间 儿子中的第一个，不包括孙子辈等。。*/
    color:red;
}
article >:nth-child(n){
    /*7.12 x相当于全部的样式。*/
    color:red;
}
article >:nth-child(2n){
    /*7.12 相当于隔行变色的样式。可以开动脑筋发散想法   */
    color:red;
}
article >:nth-child(odd){
    /*7.12 奇数行的样式   */
    color:red;
}
article >:nth-child(even){
    /*7.12 偶数行的样式   */
    color:red;
}
article >:nth-child(-n+2){
    /*7.12 前两个的样式   */
    color:red;
}
article >:nth-child(-n+2){
    /*7.12 从第二个开始的样式到之后   */
    color:red;
}
article h1:nth-of-type(2){
    /*7.12 后代中h1类型的第二个 相当于限制类型   */
    color:red;
}
article h1:nth-last-child(-n+2){
    /*7.12 后代中的后两二个  不限制类型，但如歌不匹配则样式不改变  */
    color:red;
}
article h1:nth-last-child(-n+2):not(:nth-child(1)){
    /*7.13 后代中的后两二个 排除当中的第一个  不限制类型，但如歌不匹配则样式不改变  选择器可以接在后面继续使用*/
    color:red;
}
input:disabled{
     /*7.14 表单中的禁用的input的样式*/
     color:red;
}
input:enabled{
    /*7.14 表单中的启用的input的样式*/
    color:red;
}
input:checked+label{
    /*7.15 表单中的选中的旁边的label的样式*/
    color:red;
}
input{
    /*7.16 去掉外边线*/
    outline:none;
}
input:optional{
    /*7.17 表单中非必填的表单样式*/
    color:green;
}
input:required{
    /*7.18 表单中必填的表单样式*/
    color:red;
}
input:valid{
    /*7.19 表单中验证有效的表单样式*/
    background:red;
}
input:invalid{
    /*7.20 表单中验证无效的表单样式*/
    background:red;
}
/*::双冒号是伪元素*/
p::first-letter{
    /*7.21 每个段落的第一个字符的样式*/
    color:red;
}
p::first-line{
    /*7.22 每个段落的第一个行的样式*/
    color:green;
}
span::after{
    /*7.23 span标签后面添加红色样式的.com*/
    contain: '.com';
    color: red;
}
span::before{
    /*7.23 span标签前面添加红色样式的www.*/
    contain: 'www.';
    /*contain中可以是Unicode编码,注意要加转义字符，效果是一样的*
    contain："\2193"*/
    color: red;
}
/*以下为练习*/
div{
    border: solid 1px #dddddd;
    width: 140;
}
div>input[type="text"]{
    border:none;
    outline:none;
}
div>input[type="text"]+span:after{
    /*表单后面有个标签，并且点击上去有手型的效果*/
    contain: "\293D";
    cursor: pointer;
}
/*8.1 选择器的权重  行内>id>类>标签>*
          权重位
    规则           粒度
    id             0100
    class,类       0010
    标签伪元素      0001
    *              0000  通配符
    行内样式        1000

    权重相同的后出现的覆盖先出现的  选择器的权重位可以叠加
    例如：body .jjj  的权重位位11
         .djajf[class] 为20

     !important强制提升优先级到最高，不建议用，在用第三方插件的时候想更改时可以使用  
   8.2 样式继承  继承是没有权重的 所有任何子元素定义的样式都可以覆盖掉
    有些属性不会被继承，例如边框border  
   
   8.3 通配符* 权重0 继承 null  0>null  *>继承
   
   
*/

/**  8.4 css预处理器
   .less 可以按层级关系去写，用插件可以自动生成.css文件 然后引用.css文件就可以了*/
```