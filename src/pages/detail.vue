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
<style scoped>

	.video{
		position: relative;
		height: 3.82rem;
	}
	.video video{
		width: 100%;
		height: 100%;
	}
	.video-back{
		position: absolute;
		top: 0.42rem;
		left: 0.32rem;
		text-align: center;
		color: #fff;
		font-size: 0.36rem;
		line-height: 0.64rem;
		border-radius: 3px;
		width: 0.64rem;
		height: 0.64rem;
		background: rgba(0,0,0,.5);
	}
	.nav{
		display: flex;
		box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
	}
	.nav li{
		flex: 1;
		text-align: center;
		height: 0.88rem;
		line-height: 0.88rem;
		background: #fff;
	}
	.title{
		padding: 0.48rem 0 0 0.4rem;
		background : #fff;
		margin-bottom: 0.16rem;
	}
	.title h1{
		font-size: 0.32rem;
		color: #2B333B ;
	}
	.title p{
		font-size: 0.28rem;
		color: #71777D;
		padding : 0.32rem 0 0.68rem;
		width: 6.7rem;
	}
	.question{
		padding: 0.4rem;
		background: #fff;
		
	}
	.question li h1{
		font-size: 0.28rem;
		color: #2B333B; 
	}
	.question li p{
		padding:0.24rem 0 0 0.6rem;
		font-size: 0.28rem;
		color: #71777D ; 
	}
	.question li:nth-child(1){
		padding-bottom: 0.48rem;
	}
</style>