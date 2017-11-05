<template>
	<div class="c-footer">
		<ul class="footer-ul">
			<li>
				<img src="../../assets/home.png">
				<span>123</span>
			</li>
			<li>
				<img src="../../assets/home.png">
				<span>123</span>
			</li>
			<li>
				<img src="../../assets/home.png">
				<span>123</span>
			</li>
			<li>
				<img src="../../assets/home.png">
				<span>123</span>
			</li>
		</ul>
	</div>
</template>
<style lang="scss" scoped>
	@import "../function/index.scss";
	.c-footer{
		position: fixed;
		z-index: 3;
		width: ptr(375);
		background: #fff;
		border-top: 1px solid #F3F5F7;
		bottom: 0;
		.footer-ul{
			display: flex;
			li{
				display: flex;
				height: ptr(50);
				flex: 1;
				flex-direction: column;
				justify-content: center;
				align-items: center;
				img{
					width: ptr(24);
				}
			}
		}
	}
</style>