<template>
	<div id="experience">
		<Title v-bind:headerFour="'What I did'" v-bind:headerThree="'experience'" v-bind:color="'#000'"></Title>
		<div>
			<div class="time-list">
				<ul>
					<li v-for='item in experience'>
						<span>{{item.time}}</span>
						
					</li>
				</ul>
			</div>
			<div class="experience-list">
				<ul>
					<li v-for="item in experience">
						<i class="fa fa-briefcase" :style="{backgroundColor:item.color}"></i>
						<div class="experience-content">
								<h3>{{item.company}}</h3>
								<span class="doWhat">{{item.doWhat}}</span>
						</div>
					</li>
				</ul>
			</div>
		</div>
	
	</div>
</template>
<script>
	import Title from './title.vue';
	export default{
		components:{
			Title
		},
		data(){
			return{
				experience:[
					{time:'2018.8',color:'rgb(68,199,244)',company:'自主开发',doWhat:'使用vue搭建了个人主页2018版本，同时使用webpack作为打包工具。'},
					{time:'2018.8',color:'rgb(235,84,36)',company:'东软集团',doWhat:'实习期间完成项目IT论坛，其中运用了ES6语法，使用nodejs搭建图片上传接口。在完成项目的过程中，封装了一些可复用插件，例如富文本编辑器，登录模态框，动态魔方背景等。'},
					{time:'2018.7',color:'rgb(187,30,16)',company:'阅读资料',doWhat:'在github阅读阮一峰项目时，发现语法错误，提出后被阮一峰采纳'},
					{time:'2018.3',color:'rgb(35,127,82)',company:'自主开发',doWhat:'使用原生js和css搭建在线音乐平台，使用php作为后台脚本语言，mysql为数据库，同时注册域名bukesiyi.top并申请阿里云服务器。'},
					{time:'2017.10',color:'rgb(253,189,16)',company:'自主开发',doWhat:'使用JQuery和Bootstrap开发个人主页2017版本，采用php作为后台脚本语言，mysql为数据库。'},
				]
			}
		}
	}
</script>
<style scoped>
		#experience{
			font-size:0;
			padding: 1rem 0 4rem 0;
			min-height: 580px;
			background-color:rgb(255,255,255);
		}
		#experience>div{
			margin-top:3rem;
		}
		@media screen and (min-width: 760px){
			.time-list{
				display: inline-block;
				box-sizing: border-box;
				font-size:1rem;
				width:50%;
				height: 100%;
				
				vertical-align: top;
			}
			.time-list li{
				position: relative;
				width: 100%;
				height: 200px;
			}
			.time-list li>span{
				display: inline-block;
				position: absolute;
				top:48px;
				left:60%;
				padding: .5rem;
				width: 150px;
				text-align: center;
				background-color:rgb(27,36,47);
				color:#fff;
			}
			.experience-list li>i{
				position: absolute;
				left:-105px;
				top:2.7rem;
				text-align: center;
				width: 50px;
				height: 50px;
				font-size: 1.5rem;
				line-height: 50px;
				border-radius:50%;
				color:#fff;
				background-color:rgb(68,199,244);
			}
			.experience-list{
				padding-left:63px;
				display: inline-block;
				border-left: 1px solid #999;
				box-sizing: border-box;
				vertical-align: top;
				font-size:1rem;
				width: 50%;
				height: 100%;
			}
			.experience-list>ul{
				padding:0 1rem;
			}
			.experience-list li{
				position: relative;
				width: 440px;
				max-width: 100%;
				height: 200px;
			}
			.experience-list li:before{
				position: absolute;
				content:'';
				left: -1rem;
				top:50px;
				border-width: 1rem 1rem 1rem 0;
				border-style: solid;
				border-color:transparent #00a78e transparent transparent;
			}
			.experience-content{
				position: absolute;
				top:25px;
				padding:1.5rem  3rem 1.5rem 1rem;
				margin-bottom: 1rem;
				box-shadow:0px 0px .5rem #999;
				border-bottom:.2rem solid #00a78e;
				height: 68%;
				overflow: hidden;
				text-overflow: ellipsis;
			}
			.experience-content h3{
				margin-bottom: 1rem;
			}
		}
		@media screen and (max-width: 759px){
			.time-list{
				display: inline-block;
				box-sizing: border-box;
				font-size:1rem;
				width:20%;
				height: 100%;
				vertical-align: top;
			}
			.time-list li{
				position: relative;
				width: 100%;
				height: 300px;
			}
			.time-list li>span{
				display: inline-block;
				position: absolute;
				top:48px;
				padding: .5rem;
				width: 100%;
				text-align: center;
				background-color:rgb(238,201,185);
				color:#000;
			}
			.experience-list li>i{
				display: none;
			}
			.experience-list{
				display: inline-block;
				box-sizing: border-box;
				vertical-align: top;
				font-size:1rem;
				width: 80%;
				height: 100%;
			}
			.experience-list li{
				position: relative;
				width:90%;
				height: 300px;
			}
			.experience-list li:before{
				position: absolute;
				content:'';
				left: 0rem;
				top:50px;
				border-width: 1rem 1rem 1rem 0;
				border-style: solid;
				border-color:transparent rgb(250,180,191) transparent transparent;
			}
			.experience-content{
				padding:1.5rem  3rem 1.5rem 2rem;
				margin-bottom: 1rem;
				box-shadow:4px 0px .5rem #999;
				border-bottom:.2rem solid #00a78e;
				width: 80%;
				height: 68%;
				overflow: hidden;
				text-overflow: ellipsis;
			}
			.experience-content h3{
				margin-bottom: 1rem;
			}
		}
</style>