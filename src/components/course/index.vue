<template>
	<ul class="c-course">
		<router-link to="/detail" v-for="item in arrList">
			<li>
				<img :src="item.imgUrl" />
				<h1>{{item.title}}</h1>
				<p>{{item.msg}}</p>
			</li>
		</router-link>
	</ul>
</template>
<script>
	export default{
		props:{
			arrList: Array
		}
	}
</script>
<style lang="scss" scoped>
	@import "../function/index.scss";
	.c-course{
		padding: ptr(24) 0;
		background: #fff;
		li{
			position: relative;
			width: ptr(335);
			height: ptr(72);
			margin : 0 auto ptr(24);
			img{
				position: absolute;
				width: ptr(108);
				border-radius: 5px;
			}
			h1{
				font-size: ptr(15);
				padding-left: ptr(124);
				color: #2B333B;
			}
			p{
				font-size: ptr(12);
				padding: ptr(8) 0 0 ptr(124);
				color: #71777D;
			}
		}
	}
</style>