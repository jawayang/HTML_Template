網頁樣板
=============
適用於各種不同瀏覽器版本網站樣板

#### 說明

**文件宣告** (該設定適用於所有瀏覽器。)
```HTML 
<!DOCTYPE html>
```

**根據IE版本設定 class name**
```HTML 
<!--[if IE 6]><html class="ie6 lte9 lte8 lte7" lang="zh-tw"><![endif]-->
<!--[if IE 8]><html class="ie8 lte9 lte8" lang="zh-tw"><![endif]-->
<!--[if IE 9]><html class="ie9 lte9" lang="zh-tw"><![endif]-->
<!--[if IE 7]><html class="ie7 lte9 lte8 lte7" lang="zh-tw"><![endif]-->
<!--[if !(IE 6) | !(IE 7) | !(IE 8) | !(IE 9)  ]><!--><html  lang="zh-tw"><!--<![endif]-->
```
早期的CSS HACK 是使用前綴字做區分，不太容易記憶。
例如：
```CSS
.className {
   width:100px;
   width:103px\9;
   *width:105px;
   _width:110px;
 }
```
與class 搭配，就能換成
```CSS
.test{
    width:100px;
  }
.ie8 .test{
  width:103px;
}
.ie7 .test{
  width:105px;
}
.ie6 .test{
  width:110px;
} 
```
能更容易理解

**meta 標簽**  

  設定編碼方式
  ``` html
  <meta charset="utf-8" />
  ```
  
  設定語系
  ``` html
  <meta charset="utf-8" />
  ```
  
  設定IE兼容模式
  ``` html
  <meta content='IE=edge,chrome=1' http-equiv='X-UA-Compatible' />
  ```
  
  設定避免快取
  ``` html
  <meta http-equiv="Pragma" content="no_cache">
  ```
  
  設定電話號碼偵測
  ``` html
  <meta name="format-detection" content="telephone=no"/>
  ```
  
  設定IE6轉址提示
  ``` html
  <!--[if lt IE 7 ]><meta content='0; url=ie6.html' http-equiv='refresh' /><![endif]-->
  ```
  
  設定手持裝置顯示方式
  ```
  <meta content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable:no" name="viewport">
  ```

  設定facebook推薦內容
  ``` html
  <meta property="og:title" content=""/>
  <meta property="og:description" content=""/>
  <meta property="og:url" content=""/>
  <meta property="og:image" content=""/>
  ```
  
  載入css 與 js
  ``` html
  <link href="css/normalize.css" rel="stylesheet" />
  <link href="css/style.css" rel="stylesheet" />
  <link href="css/hack.css" rel="stylesheet" />
  <link href="css/responsive.css" rel="stylesheet" />
  <script src="js/ga_public.js"></script> 
  <!--[if lt IE 9]>
      <script src="js/libs/html5shiv.js"></script> 
      <script src="js/libs/IE9.js" ></script>  
      <script src="js/libs/PIE.js" ></script>   
  <![endif]-->
  ```
  
