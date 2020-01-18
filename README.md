# ClassTimeTable
> 初次写类方法，如有不规范的地方，欢迎批评指正

HTML 课程表，可使用 JavaScript 渲染生成

# Usage（使用）
> 按照 [classTineTable.html](./classTineTable.html)、[classTineTable.js](./classTineTable.js) 使用即可

### 课程表数据格式
> (Number|String)：代表可以是 `整数`，也可以是 `字符串`
>
> (Number)：代表仅支持 `整数`
>
> (String)：代表仅支持 `字符串`


> 完整的 `课程表数据格式` 请查看 [classTineTable.js 236行](./classTineTable.js#L236)

```json
{
  /*星期几(Number|String)：1代表星期一、7代表星期天！*/
	"1": {
  
    //第几节课(Number|String)：1代表第1节课开始
		"1": {
			"name": "自习",//课程名(String)
			"teacher_name": "WenzhouChan",//教师名(String)
			"class": {
				"type": "A教学楼",//哪个教学楼(String)
				"num": 606       //教室号(String|Number)
			},
			"length": 1 //节次(Number)：有多少节
		}
	}
}
```

### 课程点击回调事件
> 使用 `clickListener` 方法即可
```js
//仅为示例，具体使用请查看 classTimeTable.js
new ClassTimeTable().clickListener(function (e) {
    //点击课程回调
    console.log(e);//返回的数据是 Object，如下
});
```
回调返回的数据：
```
{
  "name":"动态网页技术",
  "teacher_name":"元芳",
  "class":{
    "type":"B综合楼",
    "num":303
  },
  "length":4
}
```

# LICENSE
```
MIT License

Copyright (c) 2020 Chuwen

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
