# Notes

### Emment语法

1. HTML基本结构
`!`

2. id选择器
`#`
`div#test`即表示：`<div id="test"></div>`

3. 类选择器
`.`
`div.test`即表示:`<div class="test"></div>`

4. 子节点（>），兄弟节点（+），上级节点（^）
- div>ul>li>p
    ```
    <div>
    <ul>
        <li>
        <p></p>
        </li>
    </ul>
    </div>
    ```
- div+ul+p
    ```
    <div></div>
    <ul></ul>
    <p></p>
    ```
- div>ul>li^divs (这里的`^`是接在li后面所以在li的上一级，与`ul`成了兄弟关系,当然两个`^^`就是上上级)
  ```
  <div>
   <ul>
     <li></li>
   </ul>
   <div></div>
    </div>
    ```
5. 重复（`*`）
  div*5（*号后面添加数字表示重复的元素个数）
   ```<div></div>
   <div></div>
   <div></div>
   <div></div>
   <div></div>
   ```
6. 分组（()）

    div>(ul>li>a)+div>p
    (括号里面的内容为一个代码块，表示与括号内部嵌套和外面的的层级无关)
    ```
    <div>
    <ul>
        <li><a href=""></a></li>
    </ul>
    <div>
        <p></p>
    </div>
    </div>
    ```
    解释：这里如果不加括号的话，猜想下，a+div这样div就是和a是兄弟关系了，会包含在li里面。  
    <br>  
7. 属性（[attr]）

    `a[href=’###’ name=‘xiaoA’] `（中括号内填写属性键值对的形式，并且空格隔开）
    ```
    <a href="###" name="xiaoA"></a>
    ```

8. 编号（`$`）
    ul>li.test$*3 （$代表一位数，后面更上*数字就代表从1递增到填写的数字）
    ```
    <ul>
    <li class="test1"></li>
    <li class="test2"></li>
    <li class="test3"></li>
    </ul>
    ```
    另：
    