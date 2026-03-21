# html

- https://steam.oxxostudio.tw/category/html/index.html

## Html即編即所見

- Vscode下載外部插件(快捷鍵Ctrl + Shift + X)
  - 下載Live Server → Install → 點擊Trust Publisher & Install
  - 可選擇：Disabie開啟程式／Disabie(Workspace)關閉程式
  - 使用方式：在Vscode上的.html檔案上，按右鍵後，選Open with Live Server

## 標籤語法

|        語法         | 說明                           |
| :-----------------: | ------------------------------ |
|    \<h1\>~\<h6\>    | <h3>h3標題大小</h3>            |
|       \<hr\>        | 分割線<hr>                     |
|       \<img\>       | 圖片                           |
|       \<br\>        | 換行                           |
|     \<p\>\</p\>     | 段落                           |
|     \<u\>\</u\>     | <u>底線</u>                    |
|     \<b\>\</b\>     | <b>粗體</b>                    |
|     \<s\>\</s\>     | <s>刪除線</s>                  |
|  \<mark\>\</mark\>  | <mark>螢光標示</mark>          |
|     \<a\>\</a\>     | 超連結                         |
|    \<ul\>\</ul\>    | 無序列表                       |
|    \<ol\>\</ol\>    | 有序列表                       |
|    \<ol\>\</ol\>    | 清單項目(放在\<ul>\<ol>裡使用) |
| \<table\>\</table\> | 表格                           |
|  \<video>\</video>  | 影片建立、連結                 |

### html特殊符號

|  語法   | 說明 |
| :-----: | ---- |
| \&nbsp; | 空格 |

---

### \<a>標籤 => 屬性設定

> \<a target="" title="" href="">XXXXXXX\</a>

- target="\_blank" ==> 超連結另開網頁

  ```
  <a target="\_blank" href="https://www.youtube.com">youtube連結</a>

  ※ target還有提供其他3選項 _parent / _self / _top
  ```

- title="youtube" ==> 提示文字(滑鼠移至連結文字上)
  ```
  <a title="youtube" href="https://www.youtube.com">youtube連結</a></a>
  ```
- href="" ==> 不帶網址時，代表「直接刷新本頁」
  ```
  <a href="">youtube連結</a>
  ==>滑鼠點擊 youtube連結，網頁會刷新。
  ```

---

### \<img>標籤 => 屬性設定

> \<img width="" src="" alt="">

- src="" ==> 放圖片網址
- alt="" ==> 超連結的提示文字
- width="" 圖片大小
  - 數字 + px ==> **width="45px"** 設定寬度通常會和 **height=""** 搭配調整大小
  - 數字 + % ==> **width="45%"** 自動縮放長寬

---

### \<ul>容器標籤 => 建立「無序清單」

- 容器內使用 \<li> \</li> 建立清單項目

### \<ol>容器標籤 => 建立「有序清單」

- 容器內使用 \<li> \</li> 建立清單項目
  > \<ol type="">\</ol>
  - type提供5種編碼類別 ==> 1 / A / a / I / i

---

### \<table>表格標籤

> \<table border=""> \</table>

- border="" ==> 框線粗細
- 搭配下列語法建立表格
  |語法|說明|
  |:-:|:-:|
  |\<thead> \</thead>|設定表頭(即欄位)|
  |\<tr> \</tr>||
  |\<th> \</th>|欄位名稱|
  |\<tbody> \</tbody>|設定表身|
  |\<tr> \</tr>||
  |\<td> \</td>|表身內容 ※有多少\<th>，就要有多少的\<td>|

---

### \<video>影片連結

> \<video controls width="" height="" src=""> \</video>

- controls
  - 使用/寫入後，會出現影片控制器，影片才會是動畫的，要不然只是一張圖
- src=""
  - 影片網址
- width="" height="" **無法使用百分比%**
  - 影片寬度，若只設定寬度，則高度會按照原始影片長寬比例縮放
  - 影片高度，若只設定高度，則寬度會按照原始影片長寬比例縮放
