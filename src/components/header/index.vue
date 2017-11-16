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
<style scoped>

	.c-header{
		position: fixed;
		z-index: 3;
		width: 7.5rem;
		top: 0;
		background: #fff;
		box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
	}
	.header-ul li{
		display: inline-block;
		padding-left: 0.4rem;
		color: #71777D;
		font-size: 0.28rem;
		height: 0.88rem;
		line-height: 0.88rem;
	}
	.header-ul .header-search{
		padding-left: 1.18rem;
	}
	.header-search img{
		width: 0.36rem;
	}
	.header-ul .header-history{
		padding-left: 0.4rem;
	}
	.header-history img{
		width: 0.36rem;
	}
</style>
