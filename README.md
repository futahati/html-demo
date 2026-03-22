# html

- 學習參考網站 https://steam.oxxostudio.tw/category/html/index.html
```html
<html lang="en"> 要改→→ <html lang="zh-tw">
```

## Html即編即所見

- Vscode下載外部插件(快捷鍵Ctrl + Shift + X)
  - 下載Live Server → Install → 點擊Trust Publisher & Install
  - 可選擇：Disabie開啟程式／Disabie(Workspace)關閉程式
  - 使用方式：在Vscode上的.html檔案上，按右鍵後，選Open with Live Server
  - 設定 HTML 在Ctrl + S時，會自動縮排程式碼
    1. File => Preferences => Settings
    1. 搜尋 format
    1. Editor:Format On Save →→ 打勾勾
    1. Editor:Default Formatter →→ 選 HTML Language Features

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
```html
<a target="" title="" href=""> XXXXXXX </a>
```
- target="\_blank" ==> 超連結另開網頁

  ```html
  <a target="\_blank" href="https://www.youtube.com">youtube連結</a>

  ※ target還有提供其他3選項 _parent / _self / _top
  ```

- title="youtube" ==> 提示文字(滑鼠移至連結文字上)
  ```html
  <a title="youtube" href="https://www.youtube.com">youtube連結</a>
  ```
- href="" ==> 不帶網址時，代表「直接刷新本頁」
  ```html
  <a href="">youtube連結</a>
  ==>滑鼠點擊 youtube連結，網頁會刷新。
  ```

---

### \<img>標籤 => 屬性設定
```html
<img width="" src="" alt="">
```
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
```html
<table border=""> </table>
```
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

# CSS_20260322

- 學習參考網站 https://steam.oxxostudio.tw/category/css/index.html

  - \<footer> \</footer> + \&copy;
  - 版權宣告
  - 放在頁面的最下方（Footer）
  ```html
  <footer>
      <p>&copy; 2026 Write by IRW. All Rights Reserved.</p>
  </footer>

  &copy; 是 HTML 的特殊符號代碼，用來顯示 © 這個符號
  ```

## 樣式設計
- 可先設定「全域」後，再部份設定『區域』
- 區域設定 → 各別在標籤內設定
  ```html
  例：
    <h3 id="news" style="color: brown;background-color: aqua;">三立新聞網</h3>

  將 style="color: brown;background-color: aqua;" 直接寫在 H3標籤裡
  ```
- 全域設定 → 在 \</head> 之上，增加 \<style> \</style> 區塊，在這區塊裡做設定(與上述區域設定對比差異處)
  ```html
  例：
    <head>
      <title>我的第一個網頁</title>
      <!-- 引用外部CSS -->
      <link rel="stylesheet" href="style.css">

      <style>
          /* id專屬：使用方式 # + id內容 */
          #news {
              color: brown;
          }
      </style>

    </head>
  ```
  - 對應的使用方式
    - *{ }
    ```html
    * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
    }
    ```

    - \# + id的名稱(id是唯一)
    ```html
    例：<h3 id="news">三立新聞網</h3>

    #news{
          color: brown;
      }
    ```

    - \# + id的名稱 + 任何標籤
    ```html
    例：
    <div id="image">
    <!-- width="100%" 代表自動縮放圖片 -->
    <img width="45%" alt="新聞圖片"
        src="https://s.yimg.com/ny/api/res/1.2/bpgkz39YwWiw7pasIuoNMg--/YXBwaWQ9aGlnaGxhbmRlcjt3PTk2MDtoPTU0MA--/https://media.zenfs.com/zh-tw/setn.com.tw/7cee196a63813055030a21c814fb1667">

      #image img{
        border: 1px solid black;
        padding: 6px;
        background-color: darkolivegreen;
    }
      
    ```

    - . + class的名稱(class是複數！)
    ```html
    例：<div class="content">無論如何，我們很快就會讓荷莫茲海峽重新開放、安全且自由通行。</div>
    
    .content{
          background-color: cyan;
    }

    亦可將2組class共用一個設計
    .loan-form, .result {
        background-color: #ffffff;
    }
    ```
    - . + class的名稱 + 任何標籤名稱
    ```html
    例：
    <table class="summary-table">
      <thead>
          <tr>
              <th>項目</th>
              <th>金額</th>
          </tr>
      </thead>

    .summary-table th {
        background-color: #2589c9;
        color: #ffffff;
    }
    ```
    - 任何標籤名稱
    ```html
    例：<li>新聞連結1</li>

    li{
        list-style-type: none; 
      }
    
    亦可將2個標籤共用一個設計
    h1,h2 {
        font-size: 2.5rem;
        color: #063e5f;
        margin-bottom: 1rem;
    }
    ```

      - 任何標籤 + [type=""]
      ```html
      例：<input required type="number" id="amount" name="amount" value="100" step="10" min="10">

      input[type="number"], select {
        padding: 8px 10px;
      }
      ```
      - **按鈕標籤_特殊用法**：Button過渡動畫效果
      ```html
      例：<button type="submit" id="clacBtn">計算</button>

      ↓↓下述 2 段是要搭配使用，才能見到「過渡動畫效果」
      #clacBtn {
        /* 過渡動畫搭配 */
        transition: background-color 5.0s ease;
      }

      #clacBtn:hover {
        background-color: #0f4a6e;
      }
      ```

      - **表格標籤_特殊用法**：td列成為「帶狀列」
      ```html
      例：
      <table border="1" class="detial-table">
        <thead>
            <tr>
                <th>期數</th>
                <th>月付金額</th>
            </tr>
        </thead>
        <tbody id="scheduleBody">
            <tr>
                <td>1</td>
                <td>10000</td>
            </tr>

      .detial-table tr:nth-child(even) {
        background-color: #94a1ad;
        color: #5024c9;
      }
      ```

---

## 樣式設計_引用外部CSS
- 新增.css檔案，並將需共用的設定寫入該檔案內，例：
  ```html
  /* 背景色 body可視範圍區 */
  body {
      text-align: center;
      background-color: antiquewhite;
      font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  }

  a {
      color: cornflowerblue;
      text-decoration: none;
  }

  a:hover {
      color: blueviolet;
      text-decoration: underline;
  }
  ```

- 在需求的 .html檔案 引用.css檔案
  - \<link rel="stylesheet" href="">
  ```html
  例：
    <head>
      <title>我的第一個網頁</title>

      <!-- 引用外部CSS -->
      <link rel="stylesheet" href="style.css">

      <style>
          /* id專屬：使用方式 # + id內容 */
          #news {
              color: brown;
          }
      </style>
    </head>
  ```