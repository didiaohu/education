<template>
	<div class="home-page">
		<v-header></v-header>
		<ul class="nav">
			<li>
				<img src="../assets/web.png" />
				<span>前端开发</span>
			</li>
			<li>
				<img src="../assets/webservice.png" />
				<span>后端开发</span>
			</li>
			<li>
				<img src="../assets/move.png" />
				<span>移动开发</span>
			</li>
			<li>
				<img src="../assets/data.png" />
				<span>数据库</span>
			</li>
			<li>
				<img src="../assets/bigdata.png" />
				<span>云计算</span>
			</li>
		</ul>
		<v-course :arrList="array"></v-course>
		<v-footer></v-footer>
	</div>
</template>
<script>
	import course from "@/components/course/"; 
	import course1 from "@/assets/course1.jpg";
	import course2 from "@/assets/course2.jpg";
	import course3 from "@/assets/course3.jpg";
	import course4 from "@/assets/course4.jpg";
	import course5 from "@/assets/course5.jpg";
	import Header from "@/components/header/";
	import Footer from "@/components/footer/";

	export default{
		data(){
			return{
				array: []
			}
		},
		mounted(){
			this.array = [
			{
				imgUrl: course1,
				title: '实例妙解Sed和Awk的秘密',
				msg: '中级 · 330人在学'
			},
			{
				imgUrl: course2,
				title: '实例妙解Sed和Awk的秘密',
				msg: '中级 · 330人在学'
			},
			{
				imgUrl: course3,
				title: '实例妙解Sed和Awk的秘密',
				msg: '中级 · 330人在学'
			},
			{
				imgUrl: course4,
				title: '实例妙解Sed和Awk的秘密',
				msg: '中级 · 330人在学'
			},
			{
				imgUrl: course5,
				title: '实例妙解Sed和Awk的秘密',
				msg: '中级 · 330人在学'
			},
			{
				imgUrl: course1,
				title: '实例妙解Sed和Awk的秘密',
				msg: '中级 · 330人在学'
			},
			{
				imgUrl: course1,
				title: '实例妙解Sed和Awk的秘密',
				msg: '中级 · 330人在学'
			}
			];
		},
		components:{
			'v-course' : course,
			'v-header': Header,
    		'v-footer': Footer
		}
	}
</script>
<style lang="scss" scoped>
	@import "../components/function/index.scss";

	.home-page{
		.nav{
			height: ptr(100);
			padding-top: ptr(44);
			background: #F3F5F7;
			overflow-x: scroll;
			white-space: nowrap;
			li{
				width: ptr(88);
				display: inline-block;
				text-align: center;
				img{
					display: block;
					width: ptr(32);
					margin: ptr(20) auto ptr(12);
				}
			}
		}
	}
</style>