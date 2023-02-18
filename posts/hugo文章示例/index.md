# hugo文章示例




-------------

 {{< admonition >}}
一个 **注意** 横幅
{{< /admonition >}}

{{< admonition abstract >}}
一个 **摘要** 横幅
{{< /admonition >}}

{{< admonition info >}}
一个 **信息** 横幅
{{< /admonition >}}

{{< admonition tip >}}
一个 **技巧** 横幅
{{< /admonition >}}

{{< admonition success >}}
一个 **成功** 横幅
{{< /admonition >}}

{{< admonition question >}}
一个 **问题** 横幅
{{< /admonition >}}

{{< admonition warning >}}
一个 **警告** 横幅
{{< /admonition >}}

{{< admonition failure >}}
一个 **失败** 横幅
{{< /admonition >}}

{{< admonition danger >}}
一个 **危险** 横幅
{{< /admonition >}}

{{< admonition bug >}}
一个 **Bug** 横幅
{{< /admonition >}}

{{< admonition example >}}
一个 **示例** 横幅
{{< /admonition >}}

{{< admonition quote >}}
一个 **引用** 横幅
{{< /admonition >}}


### 标题:`# `-`###### `
#### 效果
> # 标题1
> ## 标题2
> ### 标题3
> #### 标题4
> ##### 标题5
> ###### 标题6

----
### 加粗:`** **`
#### 效果
> **文字**

----
### 斜体:`_ _`.`* *`
#### 效果
> _文字_

----
### 加粗斜体:`*** ***`
#### 效果
> ***文字***
### 删除:`~~ ~~`
#### 效果
> ~~文字~~

----
### 换行:`enter`x1
#### 效果
> 春眠不觉晓，
> 处处闻啼鸟。

----
### 分段:`enter`x2
#### 效果
> 春眠不觉晓，

> 处处闻啼鸟。

----
### 引用:`>`(引用里面也可以嵌入代码)
#### 效果
> 引用
> >文字 

----
### 代码:`space`x4.`tab`.` `` `.` ``` ``` `(`space`.`tab`和` ``` `效果比较好)
#### 效果
>     cd /www/wwwroot/www.domain.com
>     wget --no-check-certificate https://download.nextcloud.com/server/releases/nextcloud-12.0.3.zip`
>     unzip nextcloud-12.0.3.zip
>     mv nextcloud/* /www/wwwroot/www.domain.com
>     chattr -i .user.ini
>     chown www:www -R ./

----
### 空格:`&ensp;`.`&emsp;`（不建议使用）
#### 效果分别是`正常`.`&ensp;`.`&emsp;`
> 文字
> &ensp;文字
> &emsp;文字

---
### 表格:`|`
#### 效果
> 
| 名字   | 年龄   | 性别     | 分数   |
| ---- | ---- | ------ | ---- |
| a    | 10   | male   | 10   |
| b    | 11   | female | 11   |
| c    | 12   | male   | 12   |
### 水平线:`---`.`***`.`___`
#### 效果
>  ----

----
### 文字链接:`[]`+`()`
#### 效果
> [文字](http://www.123.com)

----
### 图片链接:`!`+`[]`+`()`
#### 效果
> ![图片名](http://i4.bvimg.com/500967/d00e782c7b37777fs.jpg)

----
### 可点链接:`<>`
#### 效果
><www.123.com>

----
### 页内跳转:`{#文字}`(待补充，示例效果不对)
#### 效果
> 目录{#index}
> 跳转到[目录](#index)

----
### 无序列表:`*`.`+`.`-`

----
### 有序列表:`数字`

----
### 行内公式:`### 
#### 效果
>  $E=mc^2$ 

----
### 整行公式:`$ $`
#### 效果

>$$\sum_{i=1}^n a_i=0 $$
>$$f(x_1,x_x,\ldots,x_n)  = x_1^2  + x_2^2  + \cdots + x_n^2 $$
>$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$

----
### 进阶
链接参考式、流程、公式、html原始码、锚点（即页内跳转）、toc目录
