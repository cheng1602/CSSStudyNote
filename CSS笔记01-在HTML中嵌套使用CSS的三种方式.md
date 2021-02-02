# CSS

*层叠样式表语言*

## 嵌套使用CSS的三种方式

- 内联定义方式

  *在标签内部使用style属性来设置元素的css样式*

  - 语法格式：

      ```html
      <!DOCTYPE html>
      <html>
      	<head>
      		<meta charset="utf-8">
      		<title>内联定义方式</title>
      	<body>
      		<!-- display布局样式，display: block显示，display: none隐藏 -->
      		<div style="width: 300px;height: 300px;background-color: aqua;display: block;"></div>
      		<br />
      		<div style="width: 300px;height: 300px;border-color: blue;border-width: 1px;border-style: solid;"></div>
      		<br />
      		<!-- 样式还可以写作border: blue 1px solid -->
      		<div style="width: 300px;height: 300px;border: blue 1px solid;"></div>
      	</body>
      </html>
      
      ```

      

- 样式块方式

  *在head标签中使用style块*
  
  - 语法格式：
  
    ```html
    <!DOCTYPE html>
    <html>
    	<head>
    		<meta charset="utf-8">
    		<title>样式块方式</title>
    		<style type="text/css">
    			/*
    			  这是CSS的注释：
    			  id选择器：
    			  #id{
    				  样式名:样式值;
    				   }
    			  标签选择器：
    			   标签名{
    				     样式名:样式值;
    				     }
    			  类选择器：
    				.类名{
    				     样式名:样式值;
    				     }
    			*/
    		   
    			#usernameError{
    				color: brown;
    				font-size: 12px;
    			}
    			
    			div{
    				background-color: darkseagreen;
    				width: 6.25rem;
    				height: 6.25rem;
    				border: cadetblue 0.1875rem solid;
    			}
    			
    			.class1{
    				background-color: lightblue;
    				border: #A52A2A solid 0.0625rem;
    			}
    			
    		</style>
    	</head>
    	<body>
    		<span id="usernameError">用户名输入为空！</span><br />
    		
    		<div>1</div>
    		<div>2</div>
    		<div>3</div><br />
    		
    		<input type="text" class="class1" /><br />
    		<select class="class1">
    			<option>选择1</option>
    			<option>选择2</option>
    		</select>
    		
    	</body>
    </html>
    
    ```
  
    ​                                                                                                                                                                                                                                                                                        
  
- 链入外部样式表文件

  *将样式写到一个独立的.CSS文件当中，在需要的网页上直接引入CSS文件，以此引入样式*

  这种方式易于维护，维护成本较低                                                                                                                                                                                                         

  - 语法格式：

    ```html
    <!DOCTYPE html>
    <html>
    	<head>
    		<meta charset="utf-8">
    		<title>链入外部样式表文件</title>
    		<!-- 引入CSS -->
    		<link rel="stylesheet" type="text/css" href="css/CSSTest.css" />
    	</head>
    	<body>
    		<a href="https://github.com/cheng1602">笔记</a>
    	</body>
    </html>
    ```

    ```css
    /* css/CSSTest.css */
    a{
    	text-decoration: none;
    	background-color: #ADD8E6;
        /* 鼠标样式 cursor: pointer; */
        cursor: pointer;
    }
    ```

    

- 列表样式

  ```html
  <!DOCTYPE html>
  <html>
  	<head>
  		<meta charset="utf-8">
  		<title></title>
  		<!-- 去掉列表中的符号 -->
  		<style>
  				ul{
  					list-style-type: none;
  				}
  		</style>
  	</head>
  	<body>
  		<ul>
  			<li>湖南
  				<ul>
  					<li>长沙</li>
  					<li>株洲</li>
  					<li>湘潭</li>
  				</ul>
  			</li>
  		</ul>
  	</body>
  </html>
  
  ```

  

- CSS样式的绝对定位

  ```html
  <!DOCTYPE html>
  <html>
  	<head>
  		<meta charset="utf-8">
  		<title>CSS样式的绝对定位</title>
  		<style type="text/css">
  			#div1{
  				width: 12.5rem;
  				height: 12.5rem;
  				background-color: lightslategray;
  				/* 绝对定位 */
  				position: absolute;
  				left: 12.5rem;
  				top: 12.5rem;
  			}
  		</style>
  	</head>
  	<body>
  		<div id="div1"></div>
  	</body>
  </html>
  
  ```

  