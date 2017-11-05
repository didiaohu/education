<template>
	<div class="c-header">
		<ul class="header-ul">
			<li>推荐</li>
			<li>课程</li>
			<li>实战</li>
			<li>职业路线</li>
			<li class="header-search"><img src="../../assets/search.png"></li>
			<li class="header-history"><img src="../../assets/history.png" /></li>
		</ul>
	</div>
</template>
<script>
	export default{
		data(){
			return{

			}
		}
	}
</script>
<style lang="scss" scoped>
	@import "../function/index.scss";

	.c-header{
		position: fixed;
		z-index: 3;
		width: ptr(375);
		top: 0;
		background: #fff;
		box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
		.header-ul{
			li{
				display: inline-block;
				padding-left: ptr(20);
				color: #71777D;
				font-size: ptr(14);
				height: ptr(44);
				line-height: ptr(44);
			}
			.header-search{
				padding-left: ptr(59);
				img{
					width: ptr(18);
				}
			}
			.header-history{
				padding-left: ptr(20);
				img{
					width: ptr(18);
				}
			}
		}
	}
</style>
