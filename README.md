<html><head>
		<meta http-equiv="Content-Type" content="text/html; charset=gbk">
	<script id="picviewer-page-script">(function (messageID){
"use strict";

		var frameID=Math.random();
		var frames={
			top:window.top,
		};

		window.addEventListener('message',function(e){
			var data=e.data;
			if( !data || !data.messageID || data.messageID != messageID )return;
			var source=e.source;
			if(source===window){
				if(data.to){
					data.from=frameID;
					frames[data.to].postMessage(data,'*');
				}else{
					switch(data.command){
						case 'getIframeObject':{
							var frameWindow=frames[data.windowId];
							var iframes=document.getElementsByTagName('iframe');
							var iframe;
							var targetIframe;
							for(var i=iframes.length-1 ; i>=0 ; i--){
								iframe=iframes[i];
								if(iframe.contentWindow===frameWindow){
									targetIframe=iframe;
									break;
								};
							};
							var cusEvent=document.createEvent('CustomEvent');
							cusEvent.initCustomEvent('pv-getIframeObject',false,false,targetIframe);
							document.dispatchEvent(cusEvent);
						}break;
					};
				};

			}else{
				frames[data.from]=source;
			};
		},true)
	})("pv-0.5106795670312598")</script></head> 
	<body>
		
		
		<table width="100%">
  <tbody><tr>
    <td align="right"><font color="#FF0000">*</font>用户名:</td>
    <td><input size="30" type="text"> <font color="red">用户名不得小于3个字符</font></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>密码:</td>
    <td><input name="text" size="30" type="text"></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>确认密码:</td>
    <td><input name="text2" size="30" type="text"></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>Email:</td>
    <td><input name="text3" size="30" type="text"></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>真是姓名:</td>
    <td><input name="text4" size="30" type="text"></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>性别:</td>
    <td>
		<select>
			<option selected="selected">男</option>
			<option>女</option>			
		</select>
	</td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>生日:</td>
    <td><select name="select">
      <option selected="selected">1980</option>
      <option>1981</option>
      <option>1982</option>
      <option>1983</option>
      <option>1984</option>
      <option>1985</option>
      <option>1986</option>
      <option>1987</option>
      <option>1988</option>
      <option>1989</option>
      <option>1990</option>
      <option>1991</option>	
	  <option>1992</option>
	  <option>1993</option>	  	  	  	  	  	  	  	  
    </select>
      <select name="select2">
        <option selected="selected">1</option>
        <option>2</option>
        <option>...</option>
        <option>12</option>				
      </select>
      <select name="select3">
        <option selected="selected">1</option>
        <option>2</option>
        <option>...</option>
        <option>31</option>						
      </select></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>手机:</td>
    <td><input name="text7" size="30" type="text"></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>居住地:</td>
    <td><select name="select4">
      <option selected="selected">上海市</option>
      <option>河南省</option>
      <option>广东省</option>
      <option>河北省</option>
      <option>黑龙江省</option>
      <option>海南省</option>
      <option>安徽省</option>
      <option>内蒙古省</option>
      <option>广西省</option>
      <option>湖南省</option>
      <option>湖北省</option>
      <option>浙江省</option>
    </select>
      <select name="select5">
        <option selected="selected">浦东新区</option>
        <option>重庆市</option>
        <option>...</option>
        <option>北京市</option>
      </select> <select name="select6">
        <option selected="selected">南汇区</option>
        <option>虹口区</option>
        <option>...</option>
        <option>金牛区</option>
      </select> <select name="select7">
        <option selected="selected">惠南镇</option>
        <option>老港镇</option>
        <option>...</option>
        <option>祝桥镇</option>
      </select></td>
  </tr>
  <tr>
    <td align="right"><font color="#FF0000">*</font>QQ:</td>
    <td><input name="text9" size="30" type="text">
	<br>
		<font color="#0099FF" size="-1">设置我的QQ在线状态</font>
	</td>
  </tr>
</tbody></table>

		
	


</body></html>
