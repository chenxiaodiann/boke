---
title: 【读书笔记】《JavaScript权威指南》第7章数组
date: 2018-11-08 04:10:03
tags: [读书笔记, 《JavaScript权威指南》]
categories: [读书笔记]
---


# html5

## 新增标签

### 结构标签

```html
<header> 标记定义一个页面或一个区域的头部
<section> 标记定义一个区域
<footer> 标记定义一个页面或一个区域的底部
以上级别最高，可以嵌套以下
<aside> 标记定义页面内容的部分的侧边栏
<article> 标记定义一篇文章
<figure> 标记定义一组媒体内容以及它们的标题
<hgroup> 标记定义文件中一个区域的相关信息
<nav> 标记定义导航栏链接
以上全部不可互相嵌套，第二部分里面可嵌套以下
<div>
<figcaption> 标记定义figure元素的标题
header/section/aside/article/footer 不要嵌套在里面
```

### 多媒体标签

```html
<viodeo> 定义视频，比如电影片段或其他视频流 
<audio>  定义声音，比如音乐或其他音频流    
<source> 媒介元素，定义媒介资源。允许规定可替换的音频文件，供不同浏览器去选择适合他的文件类型
<embed>  定义嵌入的内容，比如插件，比如音视频     
```

### web应用标签

#### 状态标签

```html
<meter>标签定义度量衡。仅用于已知最大和最小值的度量
<progress> 标签定义运行中的进度（进程）
```

#### 列表标签

```
<datalist>为input标记定义一个下拉表格，配合option
<details>标记定义一个元素的详细内容 ，配合summary
```

#### Menu

```html
<menu>  命令列表（目前所有主流浏览器都不支持）
<menutitem>menu命令列表标签（只有火狐支持）
<command>menu标记定义一个命令按钮（目前只有 Internet Explorer 支持）
```

#### 注释标签

```html
<ruby> 标记定义注释或音标
```

#### 其他标签

```html
mark  标记定义有标记的文本（黄色选中状态）
output 标记定义一些输出类型，计算表单结果配合oninput事件
```

#### 重定义标签

```html
显示不变，只是表达的含义进行了重新定义的标签
<b> 内联 文本 通常是粗体 没有传递表示重要的意思
<i >内联 斜体 没有传递表示重要的意思
<dd> 可以同的details 与 figure 一同使用 定义包含文本 dialog也可用
<dt> 可以同的details 与 figure 一同使用 汇总细节 dialog也可用
<dt>是标题，dd理解为 li
<hr> 表示主题结束 而不是水平线
<menu>不只是定义<ul><li> 增加定义用户界面的菜单 配合commond 或者menuitem使用
<small>表示批注 表示小字体 例如打印 注释或者法律条款 big已删除
<strong> 表示重要性而不是强调符号
```

## 属性变化

### input

##### 电子邮件 input类型

```html
email 输入类型用于应该包含电邮地址的输入字段。 当提交表单时，会自动地对 email 字段的值进行验证。
<input type="email" name="email">
在手机端有不同 在键盘的表现上
```

##### 统一资源定位符url     input类型

```html
url 输入类型用于应该包含 URL 地址的输入字段。 会在提交表单时对 url 字段的值自动进行验证。
<type="url" name="url" >
在苹果手机端的键盘表现上有不同
```

##### 电话号码input类型

```html
tel 输入类型用于应该包含电话号码的输入字段。
<type="tel" name="tel">
还是在手机端的键盘上有表现
```

##### 数字input类型

```html
number 输入类型用于包含数字值的输入字段。您可以设置可接受数字的限制。
<type="number" name="number" >
在电脑上focus时有按钮 还只能输入数字和加号减号点号和e 不能输入其他字母
在手机端的键盘上有表现
```

##### 日期和时间选择器

```html
<input type="date" name="user_date" />
date - 选择日、月、年
month - 选择月、年
week - 选择周、年
time - 选择时间（时、分）
datetime - 选择时间、日期、月、年（UTC 时间）
datetime-local - 选择时间、日期、月、年（本地时间）
手机上  只有在苹果手机上 有效果
```

##### radio属性值

```html
range 输入类型用于应该包含指定范围值的输入字段。
range 类型显示为滑块。
您也可以设置可接受数字的限制
<input type="range" name="posints" min="1" max="10">
```

##### saerch属性值

```html
- search 输入类型用于搜索字段，比如站内搜索或谷歌搜索等。
- 搜索字段的外观与常规的文本字段无异。
- <input type="search" name="search">
```

##### color属性值

```html
- color 输入类型用于规定颜色。
- 该输入类型允许您从拾色器中选取颜色：
```

### 表单属性

##### auteocomplete

```html
- form或input域应该拥有自动完成功能
- 当用户在自动完成域中开始输入时，浏览器应该在该域中显示填写的选项
- autocomplete 属性适用于 <form>，以及下面的 <input> 类型：text, search, url, telephone, email, password, datepickers, range 以及 color。
- <form autocomplete="no"></form>
- autocomplete 属性有可能在 form元素中是开启的，而在input元素中是关闭的。
```

 

##### autofocus

```html
- 规定在页面加载时，域自动的获取焦点
- 适用于所有<input>标签的类型
- 语法  <input autofocus="antofocus "/>
```



##### multiple

```html
- 规定输入域可选择多个值
- 适用于以下类型的 <input> 标签：
- email 和 file。
- <inpu type=file multiple="multiple">
- 加上了multiple就相当于是说可以同时上传多个文件
- <inpu type=email multiple="multiple">
- 如果不使用mutiple的话，邮箱还是可以输入多个邮箱，但整体变成一个string字符串，而不是一个数组。
```



##### placeholder

```html
- 属性提供一种提示（hint） 描述输入域所期待的值
- <input type="search" placeholder="Search Comtent"/>
- 适用于<input> 标签type属性值为：text search url telephone email password
```



##### required

```html
- 规定必须在提交之前填写输入域（不能为空）
- required属性适用于以下类型的<input>标签：text, search, url, telephone, email, password, date, number, checkbox, radio, file
- <input type="text" required="required"/>
```

### 链接属性

##### size

```html
- sizes 属性规定被链接资源的尺寸。只有当被链接资源是图标时 (rel="icon")，才能使用该属性。该属性可接受多个值。值由空格分隔。
-  根据不同的分辨率引用不同的sizes   因为针对高低屏幕  响应式 开发的
- <link rel="icon" hraf="icon.gif" type="image/gif(jpg,png)" sizes="16*16"> 显示多大的图标 
```



##### tareget

```html
- target 属性规定在何处打开页面上的所有链接。可以在每个链接中使用 target 属性来覆盖该属性。如果没有为 base 元素规定 href 属性，则 target 属性是必需的。
- <base href="<http://localhost/(绝对路径)>" target="_blan"> <base>标签写在<head></head>里就可以控制  这个路径下的所有超链接都弹出一个页面
```



##### a 超链接

###### media

```html
- media 属性规定目标 URL 是为什么类型的媒介/设备进行优化的。
- 该属性用于规定目标 URL 是为特殊设备（比如 iPhone）、语音或打印媒介设计的。
- 该属性可接受多个值。
- 只能在 href 属性存在时使用。
- a:madia=""(对设备进行优化handhelp tv 主要是告诉后台  后台方便针对不同设备 进行不同的处理)
```



###### hreflang

```html
- hreflang 属性规定被链接文档的语言。
- 仅在使用 href 属性时才可以指定 hreflang 属性。和 lang 属性类似，hreflang 属性的值也是 ISO 标准的双字符语言代码。和 lang 属性不同的是，hreflang 属性不会指定标签中的内容所使用的语言，而是指定被 href 属性调用的文档所使用的语言。
- a:hreflang="zh"( 设置语言（中文） 主要告诉浏览器  浏览器自己加载)
```



###### rel

```html
- rel 属性规定当前文档与被链接文档之间的关系。
- 仅在 href 属性存在时使用。
- a:rel="external"(设置链接  可以引用外部链接) 
```

### 其他属性

##### script

```html
- script标签中defer属性规定对脚本进行延迟加载，直到页面结构加载成功后才对脚本进行加载 目前是只有ie支持
- script标签中async实现JavaScript双线程加载，属性规定对脚本进行异步加载，
```



##### ol

```html
- ol 有序列表
- Start--起始值
```



###### Reversed--倒叙排列

```html
- reversed 属性是逻辑属性。
- 当使用该属性时，它规定列表属性为降序 (9, 8, 7...)，而不是升序 (1, 2, 3...)。
```

适用于HTML5新增标签的简洁解决兼容性的方式：header、nav、section、aside、article、footer等变块diasplay:block

##### html 

```html
- manifest ="cache.manifest"（定义页面缓存离线应用文件）
- 语法：<html manifest="index.（cache.）manifest">
```

##### style 与结构与表现分离背驰 应该单独存储

```html
- scoped：内嵌css 可以写在任何位置 ，里面写css 不提倡
- <style scoped>......</style>
```

## 本地缓存和离线缓存

### wed Storage

**localStorage**
**sessionStorage**

#### 相同

###### 方法

1.  使用setItem方法设置存储内容
2. 使用getItem方法获取存储内容
3. 使用removeItem方法删除存储内容
4. 使用clear方法清楚所有内容
5. 使用key方法获取存储字段

###### 属性

使用leng 属性获取存储内容个数

#### 不同

###### 存储时效

- localStorage 存储会持久化
- sessionStorage 存储会在网页会话结束后失效 标签页的关闭数据就会消失

###### 存储容量

localStorage 容量一般在2-5m左右

sessionStorage 存储容量不一，部分浏览器不设限

::: warning 注意
1.注意存储容量超出配额 抛出 QuotaExceededError异常
2.存储类型的限制 仅能存储字符串 注意类型的转换
sessinStorage失效机制 刷新页面并不会失效 相同URL不同标签页不能共享sessionStorage
:::

#### 带有过期机制的localStorage的功能需求

1.可以设置数据的存储时间

2.过期数据清理

3.自行维护存储空间

### IndexedDB 

#### 概念

IndexedDB 很适合存储大量数据，它的 API 是异步调用的。IndexedDB 使用索引存储数据，各种数据库操作放在事务中执行。IndexedDB 甚至还支持简单的数据类型。IndexedDB 比 localstorage 强大得多，但它的 API 也相对复杂。对于简单的数据，你应该继续使用 localstorage，但当你希望存储大量数据时，IndexedDB 会明显的更适合，IndexedDB 能提供你更为复杂的查询数据的方式。

#### 特性

###### 对象仓库

有了数据库后我们自然希望创建一个表用来存储数据，但 indexedDB 中没有表的概念，而是 objectStore，一个数据库中可以包含多个 objectStore，objectStore 是一个灵活的数据结构，可以存放多种类型数据。也就是说一个 objectStore 相当于一张表，里面存储的每条数据和一个键相关联。我们可以使用每条记录中的某个指定字段作为键值（keyPath），也可以使用自动生成的递增数字作为键值（keyGenerator），也可以不指定。选择键的类型不同，objectStore 可以存储的数据结构也有差异。

###### 事务性

在 indexedDB 中，每一个对数据库操作是在一个事务的上下文中执行的。事务范围一次影响一个或多个 object stores，你通过传入一个 object store 名字的数组到创建事务范围的函数来定义。例如：db.transaction(storeName, 'readwrite')，创建事务的第二个参数是事务模式。当请求一个事务时,必须决定是按照只读还是读写模式请求访问。

###### 基于请求

对 indexedDB 数据库的每次操作，描述为通过一个请求打开数据库,访问一个 object store，再继续。IndexedDB API 天生是基于请求的,这也是 API 异步本性指示。对于你在数据库执行的每次操作,你必须首先为这个操作创建一个请求。当请求完成,你可以响应由请求结果产生的事件和错误。

###### 异步

在 IndexedDB 大部分操作并不是我们常用的调用方法，返回结果的模式，而是请求—响应的模式，所谓异步 API 是指并不是这条指令执行完毕，我们就可以使用 request.result 来获取 indexedDB 对象了，就像使用 ajax 一样，语句执行完并不代表已经获取到了对象，所以我们一般在其回调函数中处理。

#### 接口

##### IDBFactory 数据库工厂 负责打开或创建数据库

提供对数据库的访问。这是全局对象实现的接口indexedDB，因此是API的入口点。

###### 实现

实现接口的对象是window.indexedDB 而不是直接使用IDBFactory。

###### 方法

IDBFactory.open 方法发送一个打开或者创建一个数据库的请求

IDBFactory.deleteDatabase 发送一个删除数据库的请求。

IDBFactory.cmp 一种比较两个键并返回指示哪一个值更大的结果的方法。

##### IDBDatabase 数据库

表示与数据库的连接。这是获取数据库事务的唯一方法。检索和修改数据

###### 方法

IDBDatabase.close 方法关闭数据库。

IDBDatabase.createObjectStore 方法创建 store，相当于表

IDBDatabase.transaction 开启一个事务。

IDBDatabase.deleteObjectStore()在连接的数据库中销毁具有给定名称的对象存储库以及引用它的任何索引。

###### 属性

IDBDatabase. name   只读DOMString包含已连接数据库名称的A.

IDBDatabase.version  只读一个64位整数，包含已连接数据库的版本。首次创建数据库时，此属性为空字符串。

IDBDatabase.objectStoreNames  只读一个DOMStringList包含的名称的列表对象存储当前连接的数据库中。

###### 事件处理时发生的程序

IDBDatabase.onabort中止访问数据库时触发。

IDBDatabase.oncloseclose事件发生时触发; 当数据库意外关闭时，例如在应用程序关闭期间，会发生这种情况。

IDBDatabase.onerror访问数据库失败时触发。

IDBDatabase.onversionchange当数据库结构发生更改时触发（IDBOpenDBRequest.onupgradeneeded事件或IDBFactory.deleteDatabase()在其他地方请求（最可能在同一台计算机上的另一个窗口/选项卡中）。这与版本更改事务（请参阅参考资料IDBVersionChangeEvent）不同，但它是相关的。

##### IDBTransaction 事务

表示事务。您在数据库上创建事务，指定范围（例如您要访问的对象存储），并确定所需的访问类型（只读或读写）。

###### 方法

IDBTransaction.objectStore 返回IDBObjectStore表示对象存储的对象，该对象存储是此事务范围的一部分。

##### IDBObjectStore 数据库表

表示允许访问IndexedDB数据库中的一组数据的对象存储，通过主键查找。

###### 方法

IDBObjectStore.add()

返回一个IDBRequest对象，这是为了向对象库添加新记录。

IDBObjectStore.clear()

创建并立即返回一个IDBRequest对象，并在单独的线程中清除此对象库。这是为了从对象库中删除所有当前记录。

IDBObjectStore.delete()

返回一个IDBRequest对象，并在一个单独的线程中删除由指定键选择的商店对象。这用于从对象库中删除单个记录。

IDBObjectStore.get()

返回一个IDBRequest对象，并在单独的线程中返回由指定键选择的存储对象库。这用于从对象库中检索特定记录。

IDBObjectStore.getAll()

返回一个IDBRequest 对象，如果没有给出参数，则检索与指定参数匹配的对象库中的所有对象或商店中的所有对象。

IDBObjectStore.getKey()

返回一个IDBRequest对象，并在一个单独的线程中检索并返回与指定参数匹配的对象中的对象的记录键。

IDBObjectStore.openCursor()

返回一个IDBRequest对象，并在一个单独的线程中返回一个新IDBCursorWithValue对象。用于通过主键和游标迭代对象存储。

IDBObjectStore.openKeyCursor() 

返回一个IDBRequest对象，并在一个单独的线程中返回一个新对象IDBCursor。用于使用键遍历对象库。

IDBObjectStore.put()

返回一个IDBRequest对象，并且，在一个单独的线程，创建了一个结构化的克隆的value，并存储在对象存储克隆值。这是用于在事务模式下更新对象库中的现有记录readwrite。

IDBObjectStore.count()

返回一个IDBRequest对象，并在一个单独的线程中返回与提供的键或匹配的记录总数IDBKeyRange。如果未提供参数，则返回商店中的记录总数。

##### IDBRequest 是所有indexedDB操作的返回值，indexdDB操作请求

通用接口，用于处理数据库请求并提供对结果的访问。

###### 属性

IDBRequest.error 只读DOMException如果请求失败，则返回a ，指示出错的地方。

IDBRequest.result 只读返回请求的结果。如果请求失败且结果不可用，则抛出InvalidStateError异常。

IDBRequest.source 只读请求的来源，例如a IDBIndex或IDBObjectStore。如果不存在源（例如调用时IDBFactory.open），则返回null。

###### 事件处理程序

IDBRequest.onerror 错误事件的事件处理程序。IDBRequest.onsuccess 成功事件的事件处理程序。

##### IDBIndex 索引

还允许访问IndexedDB数据库中的数据子集，但使用索引来检索记录而不是主键。这有时比使用更快IDBObjectStore。



###### ::: tip基本逻辑

IDBFactory,open负责创建数据库的对象，返回IDBDatabase对象实列,通过IDBDatabase.transaction 开启事务，获得IDBTransaction对象的实列，通过IDBTransaction.objectStore获取数据库表 数据表的各种方法对数据进行增删改查， 方法返回的对象时IDBRequest对象，对数据进行结果的查询访问

:::

##### 不是重要

###### IDBEnvironment

提供对IndexedDB功能的访问。它由window和worker对象实现。此接口不是2.0规范的一部分。

###### IDBOpenDBRequest

表示打开数据库的请求。

###### IDBCursor

迭代对象存储和索引。

###### IDBCursorWithValue

迭代对象存储和索引并返回游标的当前值。

###### IDBKeyRange

定义可用于从特定范围内的数据库检索数据的键范围。

###### IDBLocaleAwareKeyRange

 定义一个键范围，可用于从特定范围内的数据库中检索数据，并根据为特定索引指定的语言环境的规则进行排序（请参阅createIndex()的optionalParameters。）。此接口不是2.0规范的一部分。

#### 完整案列

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
  <script src="./lib/art_template.js"></script>
</head>
<body>
  <table>
    <tr>
      <td>
        <label for="name">用户名</label>
      </td>
      <td>
        <input type="text" name="name" id="name">
      </td>
    </tr>
    <tr>
      <td>
        <label for="phone">电话</label>
      </td>
      <td>
        <input type="text" name="phone" id="phone">
      </td>
    </tr>
    <tr>
      <td>
        <label for="address">地址</label>
      </td>
      <td>
        <input type="text" name="address" id="address">
      </td>
    </tr>
  </table>
  <input type="button" value="添加用户" id="btnAdd" onclick="addPerson()">
  <table>
    <thead>
      <tr>
        <th>id</th>
        <th>name</th>
        <th>address</th>
        <th>phone</th>
        <th>编辑</th>
      </tr>
    </thead>
    <tbody id="tbd">
    </tbody>
  </table>
  <script id="tbTmpl" type="text/html">
    <tr>
      <td>{{id}}</td>
      <td>{{name}}</td>
      <td>{{phone}}</td>
      <td>{{address}}</td>
      <td><a href="#">修改</a>
      <a href="#" onclick="delById({{id}})">删除</a></td>
    </tr>
  </script>
  <script>
    var db, dbName = 'demoDb', dbVersion = 1, personStore = 'person';
    // 创建indexedDB对象，兼容各种浏览器
    var indexedDB = window.indexedDB || window.webkitIndexedDB || window.mozIndexedDB || window.msIndexedDB;
    if (!indexedDB) {
      console.log("你的浏览器不支持IndexedDB");
    }

    openIndexedDB(loadTableData);

    // 配合游标遍历表中数据，并配合art-template生成html
    function loadTableData() {
      document.getElementById('tbd').innerHTML = "";
      var trans = db.transaction(personStore, 'readwrite');
      var store = trans.objectStore(personStore);
      var cursorRequest = store.openCursor();
      cursorRequest.onsuccess = function (e) {
        var cursor = e.target.result;
        if (cursor) {
          var html = template('tbTmpl', cursor.value);
          document.getElementById('tbd').innerHTML += html;
          cursor.continue(); // 游标继续往下 搜索，重复触发 onsuccess方法，如果到到返回null
        }
      }
    }

    function delById(id) {
      if (!db || !id) {
        return;
      }
      // 创建一个事务
      var transaction = db.transaction(personStore, 'readwrite');

      // 通过事务来获取store
      var store = transaction.objectStore(personStore);

      // 删除请求
      var delPersonRequest = store.delete(id);
      delPersonRequest.onsuccess = function (e) {
        loadTableData(); // 删除成功后，重新加载数据
      }
      delPersonRequest.onerror = function (e) {
        console.log(e.target.error);
      }
    }

    // 添加用户
    function addPerson() {
      if (!db) {
        return;
      }
      var pName = document.getElementById('name').value;
      var pPhone = document.getElementById('phone').value;
      var pAddress = document.getElementById('address').value;
      // 创建一个事务
      var transaction = db.transaction(personStore, 'readwrite');

      // 通过事务来获取store
      var store = transaction.objectStore(personStore);

      var addPersonRequest = store.add({ name: pName, phone: pPhone, address: pAddress });
      addPersonRequest.onsuccess = function (e) {
        console.log(e.target);
        loadTableData(); // 添加成功后重新加载数据
      }
      addPersonRequest.onerror = function (e) {
        console.log(e.target.error);
      }
    }

    // 打开数据库
    function openIndexedDB(callback) {
      // 打开一个数据库
      var request = indexedDB.open(dbName, dbVersion);

      // 打开失败
      request.onerror = function (e) {
        console.log(e.currentTarget.error.message);
      };

      // 打开成功！
      request.onsuccess = function (e) {
        db = e.target.result;
        console.log('成功打开DB');
        callback();
      };

      // 打开成功后，如果版本有变化自动执行以下事件
      request.onupgradeneeded = function (e) {
        var db = e.target.result;
        if (!db.objectStoreNames.contains(personStore)) {
          console.log("我需要创建一个新的存储对象");
          //如果表格不存在，创建一个新的表格（keyPath，主键 ； autoIncrement,是否自增），会返回一个对象（objectStore）
          var objectStore = db.createObjectStore(personStore, {
            keyPath: "id",
            autoIncrement: true
          });

          //指定可以被索引的字段，unique字段是否唯一, 指定索引可以加快搜索效率。
          objectStore.createIndex("name", "name", {
            unique: true
          });
          objectStore.createIndex("phone", "phone", {
            unique: false
          });
        }
        console.log('数据库版本更改为： ' + dbVersion);
      };
    }
  </script>
</body>
</html>
```

