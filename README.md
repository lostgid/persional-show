<html><head>
		<meta http-equiv="Content-Type" content="text/html; charset=gbk">
	<script id="picviewer-page-script">(function (messageID){"use strict";

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
