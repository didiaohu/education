<template>
	<div class="detail-page">
		<div class="video">
			<video src="http://v3.mukewang.com/shizhan/59f8498ae420e5be578b459b/H.mp4" controls="controls"></video>
			<router-link to="/home">
				<div class="video-back"><</div>
			</router-link>
		</div>
		<ul class="nav">
			<li v-for="item in arr">{{item}}</li>
		</ul>
		<div class="title">
			<h1>{{title}}</h1>
			<p>{{des}}</p>
		</div>
		<ul class="question">
			<li v-for="(item, index) in arrQuestion">
				<h1>{{arrTitle[index]}}</h1>
				<p v-html="item"></p>
			</li>
		</ul>
	</div>
</template>
<script>
	export default{
		data(){
			return{
				arr: [],
				title: '',
				des: '',
				arrQuestion:[],
				arrTitle: ["课程须知", "老师告诉你能学到什么？"]
			}
		},
		mounted(){
			this.arr = ["章节", "详情", "评论", "问答", "记"];
			this.title = "iOS基础教程之-Camera摄像头";
			this.des = "从实例出发介绍我们的Camera，可以实现Camera属性检测，照片拍摄，视频录制，图片展示，录制视频";
			this.arrQuestion = ["本课程适合客户端产品经理，研发人员以及对iOS新特性感兴趣的人群", `
			(1）数码相机相关的所有API<br/> 
			(2）利用Camera实现相机的各种属性检测<br/> 
			(3）利用Camera拍照、保存、遍历相册等功能<br/>
			(4）利用Camera拍摄视频、视频剪切功能`];
		}
	}
</script>
<style lang="scss" scoped>
	@import "../components/function/index.scss";
	.detail-page{
		.video{
			position: relative;
			height: ptr(191);
			video{
				width: 100%;
				height: 100%;
			}
			&-back{
				position: absolute;
				top: ptr(21);
				left: ptr(16);
				text-align: center;
				color: #fff;
				font-size: ptr(18);
				line-height: ptr(32);
				border-radius: 3px;
				width: ptr(32);
				height: ptr(32);
				background: rgba(0,0,0,.5);
			}
		}
		.nav{
			display: flex;
			box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
			li{
				flex: 1;
				text-align: center;
				height: ptr(44);
				line-height: ptr(44);
				background: #fff;

			}
		}
		.title{
			padding: ptr(24) 0 0 ptr(20);
			background : #fff;
			margin-bottom: ptr(8);
			h1{
				font-size: ptr(16);
				color: #2B333B ;
			}
			p{
				font-size: ptr(14);
				color: #71777D;
				padding : ptr(16) 0 ptr(34);
				width: ptr(335);
			}
		}
		.question{
			padding:ptr(20);
			background: #fff;
			li{
				h1{
					font-size: ptr(14);
					color: #2B333B; 
				}
				p{
					padding:ptr(12) 0 0 ptr(30);
					font-size: ptr(14);
					color: #71777D ; 
				}
			}
			li:nth-child(1){
				padding-bottom: ptr(24);
			}
		}
	}
</style>