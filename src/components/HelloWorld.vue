<template>
	<div class="container">
		<div class="row">
			<div class="col-md-6 resumeStyle" ref="resumeStyle">
				<div class="col-xs-12 noScroll">					
					<pre ref="resumePre">{{preMsg}}</pre>
				</div>
			</div>
			<div class="col-md-6 resumeContain" ref="resumeContain">
				<div class="col-xs-12 noScroll">
					<div ref="resumeContainRight" class="resumeContainRight">
						<p class="name">朱林峰</p>
						<div class="row">
							<div class="col-md-3">
								<p>男 | 1992/02/15</p>
							</div>
							<div class="col-md-9">
								<p>职位: 前端攻城狮</p>
							</div>
						</div>
						<div class="row">
							<div class="col-md-3">
								<p>籍贯: 梅州</p>
							</div>
							<div class="col-md-9">
								<p>政治面貌: 共青团员</p>
							</div>
						</div>
						<div class="row">
							<div class="col-md-3">
								<p>学历: 本科</p>
							</div>
							<div class="col-md-9">
								<p>学校/专业: 北京理工大学珠海学院/信息管理与信息技术</p>
							</div>
						</div>
						<p>成长历程: </p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在网页上输出Hello World后，对前端的迷恋就一发不可收拾，原来字母符号这么神奇。从此踏上漫漫编程路。。。</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;大三第二学期开始，从<code>html</code>到<code>css</code>再到<code>原生javascript</code>，一边学一边实践，一点一点积累。</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;转眼就大四了，面临找工作实习，我开始投简历、参加招聘会，很幸运在2015年11月初的时候接到了一个前端实习生的offer，从此便开始了我的前端职业生涯。</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;实习期间，我知道了<code>Jquery、Ajax、HTML5、CSS3、Bootstrap</code>并且熟练掌握了它们，期间项目由使用Jquery库转为<code>AngularJs框架</code></p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;半年后，也就是2016年6月份，我毕业了，继续留在该公司。又过了两个月，在网上看到都在说Vue.js比AngularJs好，便开始学习Vue.js，一个月后便开始用Vue.js重构项目，一边摸索一边重构。</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;渐渐地，对<code>Vue.js</code>越来越熟练，越来越喜欢，便开始学习使用Vue.js的一些生态和UI框架：<code>Vuex、VUX、ElementUI、iView、Mint UI</code>等，并用于实际项目中。</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;再后来，接触了<code>ES6</code>，对它的新特性也一下子喜欢上了：箭头函数、变量声明、解构、Set和Map数据结构、Promise对象、循环遍历等等。</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;项目中还掌握使用了<code>SVN、git、Echart、Highcharts、百度地图API、腾讯地图API、SEO、前端提高网站性能</code>等</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;工作之余学习了<code>node.js、Express、MongoDB</code>，以及<code>微信小程序</code>阅读了《高性能网站建设指南》、《JavaScript语言精粹》、《JavaScript高级程序设计》，《JavaScript权威指南》还在阅读中，此外，遇到问题我也会记录到博客，方便下次不再采坑，同时也给遇到同样问题的同行提供一点建议，博客地址：<code>http://www.cnblogs.com/zlfProgrammer/</code></p>
						<p>个人评价: </p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;热爱编程，善于学习新技术；有较强的自学能力和适应能力；能够与团队友好协作，共同进步。</p>
						<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<code>最后：咖啡泡面已备好，随时迎接新的挑战！</code></p>
						<p>感谢阅读，可在下面获取我的交流方式</p>
						<p class="linkContain">
							<span class="qqContain">							
								<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=412606846&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:2047599731:41" alt="点击这里给我发消息" title="点击这里给我发消息" /></a>
								<div class="qq-popover">
									<img src="./../../static/qq.png">
								</div>
							</span>
							
							<span class="wechatContain">
								<img class="wechat" src="./../../static/wechat.png" />
								<div class="sns-popover">
									<img src="./../../static/wechat.jpg">
								</div>
							</span>

							<span class="githua">
								<a href="https://github.com/zhuDadaa" target='_blank'>
									<img class="wechat" src="./../../static/GitHub.png" width="25"/>
								</a>
							</span>
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
    	windowHeight: $(window).height()-20,
    	preMsg: ""
    }
  },
  created: function() {
		this.$nextTick(() => {
  			this.setContentHeight();
		});
  },
  methods: {
  	setContentHeight: function(){
  		$(this.$refs.resumeStyle).height( $(window).height()-65 );
  		$(this.$refs.resumePre).height( $(window).height()-65 );
  		$(this.$refs.resumeContain).height( $(window).height()-65 );
  		$(this.$refs.resumeContainRight).height( $(window).height()-65 );
  	},
  	setChangeContentHeight: function(){
  		var _this = this;
  		window.onresize= function(){
		  	_this.$nextTick(() => {
		  		_this.setContentHeight();
			});
	  	};
  	},
  	resumeShow: function(){
  		var str = `/*
* 你好！
* 欢迎你到此一游,
* 我认为
* 作为一个前端的人员,就应该做一个网页出来,
* 哪怕简单点。。。所以我就动手做了这个。
* 不多说,来效果
* */
/**
 * 首先,先给全局加上动画效果
 */
*{
 transition: all 0.5s ease-in;
 margin: 0;
 padding: 0;
}
/**
 * 换个渐变的背景吧
 */
#particles-js{
 opacity: .8;
 background: -webkit-gradient(linear,left top,right bottom,from(#50a3a2),to(#53e3a6));
 background: linear-gradient(to bottom right,#50a3a2,#53e3a6);
 background: -webkit-linear-gradient(to bottom right,#50a3a2,#53e3a6);
}
/**
 * 给个背景色
 * 而且不能遮挡后面的背景
 */
.resumeStyle{
 background-color: rgba(85,163,184,0.3);
}
.resumeStyle .noScroll pre{
 color: white;
}
/**
 * 旋转下吧！顺便做下浏览器兼容性
 * 做个圆角,加点阴影更加完美~
 */
.resumeStyle{
 transform: perspective(1200px) rotateY(20deg) rotateX(5deg);
 -ms-transform: perspective(1200px) rotateY(20deg) rotateX(5deg);
 -moz-transform: perspective(1200px) rotateY(20deg) rotateX(5deg);
 -webkit-transform: perspective(1200px) rotateY(20deg) rotateX(5deg);
 -o-transform: perspective(1200px) rotateY(20deg) rotateX(5deg);
 border-radius: 4px;
 box-shadow: 0px 4px 3px rgba(0,0,0,0.3);
}
/**
 * 好了,到另一半。。
 */
.resumeContain{
 background-color: rgba(85,163,184,0.3);
 color: white;
 border-radius: 4px;
 box-shadow: 0px 4px 3px rgba(0,0,0,0.3);
 transform: perspective(1200px) rotateY(-20deg) rotateX(5deg);
 -ms-transform: perspective(1200px) rotateY(-20deg) rotateX(5deg);
 -moz-transform: perspective(1200px) rotateY(-20deg) rotateX(5deg);
 -webkit-transform: perspective(1200px) rotateY(-20deg) rotateX(5deg);
 -o-transform: perspective(1200px) rotateY(-20deg) rotateX(5deg);
}






`;
		this.typing(str);
	},
	typing: function(str){
		var _this = this;
		var i=0;
		var typings = function(){
			if (i <= str.length) {
		    	_this.preMsg = str.slice(0, i++) + '_\n\n\n';
		    	if(str[i] == "}"){
		    		$("#styleObject").html("");
		    		$("#styleObject").append(str.slice(0, i++) + "}");
		    	}
		    	$(".resumeStyle pre").scrollTop($(".resumeStyle pre")[0].scrollHeight);
		    	setTimeout(function(){
		    		typings();
		    	}, 20);//递归调用
		   	}else{
		    	_this.preMsg = str;//结束打字,移除 _ 光标
		    	setTimeout(function(){		    		
		    		$(".resumeContainRight").fadeIn();
		    	},1000);
		    }
		};
		typings();
	}
  },
  beforeMount: function(){
  	this.setChangeContentHeight();
  },
  mounted: function() {
  	this.resumeShow();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.resumeStyle,.resumeContain{
		margin-top: 30px;
		padding: 0;
	}
	.noScroll{
		width: 100%;
		overflow: hidden;
	}
	.resumeStyle .noScroll pre{
		margin: 0;
		margin-bottom: -20px;
		margin-right: -32px;
		padding: 0;
		padding-right: 10px;
		border: 0px;
	}
	.table{
		margin-bottom: 0px;
	}
	.name{
		font-size: 24px;
	}
	.resumeContainRight{
		overflow: auto;
		margin: 0;
		margin-bottom: -20px;
		margin-right: -32px;
		padding: 0;
		border: 0px;
	}
	.resumeContainRight p{
		margin-right: 10px;
	}
	.linkContain{
		margin-bottom: 20px;
		text-align: center;
	}
	.wechat{
		margin-left: 10px;
	}
	.wechatContain,.qqContain{
		position: relative;
    	display: inline-block;
	}
	.qq-popover img, .sns-popover img {
		width: 175px;
	}
	.wechatContain:hover .sns-popover {
		-webkit-transform: scale(1, 1);
		-moz-transform: scale(1, 1);
		-ms-transform: scale(1, 1);
		-o-transform: scale(1, 1);
		transform: scale(1, 1);
		opacity: 1;
		filter: alpha(opacity=100);
		visibility: visible;
	}
	.qqContain:hover .qq-popover {
		-webkit-transform: scale(1, 1);
		-moz-transform: scale(1, 1);
		-ms-transform: scale(1, 1);
		-o-transform: scale(1, 1);
		transform: scale(1, 1);
		opacity: 1;
		filter: alpha(opacity=100);
		visibility: visible;
	}
	.sns-popover,.qq-popover {
		width: 194px;
		height: 209px;
		position: absolute;
		left: -79px;
		top: -200px;
		visibility: hidden;
		opacity: 0;
		filter: alpha(opacity=0);
		-webkit-transform: scale(0, 0);
		-moz-transform: scale(0, 0);
		-ms-transform: scale(0, 0);
		-o-transform: scale(0, 0);
		transform: scale(0, 0);
		-webkit-transition: all .3s ease;
		-moz-transition: all .3s ease;
		-o-transition: all .3s ease;
		transition: all .3s ease;
		transform-origin: 50% 100%;
		-webkit-transform-origin: 50% 100%;
		-moz-transform-origin: 50% 100%;
		-o-transform-origin: 50% 100%;
	}
	.resumeContainRight{
		display: none;
	}
</style>
