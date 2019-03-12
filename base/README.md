# Javascript
本文章对 `Javascript` 做一个阶段性的终结。

希望大家先对基础教程 `Javascript Junior Level` 了解一下再看这一篇文章。

<a href="http://javascript-junior.biuxbiu.design/#/" target="_blank"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="168" height="20"><linearGradient id="b" x2="0" y2="100%"><stop offset="0" stop-color="#bbb" stop-opacity=".1"/><stop offset="1" stop-opacity=".1"/></linearGradient><clipPath id="a"><rect width="168" height="20" rx="3" fill="#fff"/></clipPath><g clip-path="url(#a)"><path fill="#555" d="M0 0h135v20H0z"/><path fill="#97ca00" d="M135 0h33v20H135z"/><path fill="url(#b)" d="M0 0h168v20H0z"/></g><g fill="#fff" text-anchor="middle" font-family="DejaVu Sans,Verdana,Geneva,sans-serif" font-size="110"> <text x="685" y="150" fill="#010101" fill-opacity=".3" transform="scale(.1)" textLength="1250">Javascript Junior Level</text><text x="685" y="140" transform="scale(.1)" textLength="1250">Javascript Junior Level</text><text x="1505" y="150" fill="#010101" fill-opacity=".3" transform="scale(.1)" textLength="230">Link</text><text x="1505" y="140" transform="scale(.1)" textLength="230">Link</text></g> </svg></a>

## 数组


#### 数组创建

* 空数组
```copy
var Obj = new Array();
```

* 指定数组长度（个数）
```copy
var Obj = new Array(5);
```

* 指定元素数组
```copy
var Obj = new Array('a','b','c'...,'z');
```

* 单维数组（也称为数组的字面量）
```copy
var Obj = ['a','b','c'...,'z'];
```

* 多维数组
```copy
var Obj = (['a','b','c'],['1','2','3'],['a1','b2','c3']);
```

#### 数组操作

###### 存取数组元素
* 单维数组获取元素：`数组名[元素下标索引]`
```copy
var theFirstLetter = Obj[0];        //获取第一个元素
```

* 多维数组获取元素：`数组名[数组小标索引][元素下标索引]`
```copy
var theFirstGroupFirstLetter = Obj[0][1];     //获取第一组数组的第二个元素
```

* 新增数组元素：使用 `[]` 新增一个数组元素。
```copy
Obj[4] = '5';
```

* 删除数组元素：`delete`
```copy
delete Obj[4];
```

* 关联数组：当下标为 `非数值` 的时候，生成关联数组，下标作为对象的属性名字。
```copy
Obj['letter'] = 'hello world';
```

* 数组添加到对象当中
```copy
var Obj = {};
var ObjArray = ['1','2','3'];
for(var i = 0; i <= ObjArray.length; i++){
    Obj[i] = ObjArray[i];
}
console.log(Obj);
```

>还有另一个小技巧，后续我们会讨论 `push` 和 `apply` 的用法。
```copy
var Obj = {};
var ObjArray = ['1','2','3'];
[].push.apply(Obj,ObjArray);
console.log(Obj);
```

* 遍历数组
```copy
var Obj = ['1','2','3'];
for(var i = 0;i <= Obj.length; i++){
    console.log(Obj[i]);
}
```

#### 数组属性

* constructor：`返回对象的构造函数`
```copy
var Obj = ['1','2'];
console.log(Obj.constructor);       //返回数组对象的构造函数
```

>构造函数对象的 `constructor` 也返回构造函数。
```copy
function con(){
    console.log('1')
}
var dataOne = new con();
var dataTwo = new con();
dataOne.constructor;        //返回对象的构造函数
dataTwo.constructor;        //返回对象的构造函数
结果
//ƒ con(){
    console.log('1')
}//
```


* length：`返回数组的长度`
```copy
var Obj = ['1','2','3'];
console.log(Obj.length)
```

* prototype：`通过增加属性和方法扩展数组定义`