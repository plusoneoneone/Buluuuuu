<template>
	<view class="content">
		<image class="logo" src="/static/V_Logo.jfif"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
			<view class="nav">
				<view class="nav_item" v-for="(item,index) in navs" :key="index" @click="navItemClick">
					<view :class="item.icon"></view>
					<p>{{item.title}}</p>
				</view>
			</view>
		</view>	
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				navs:[
					{
						icon: 'iconfont icon-chuzhi',
						title: 'customer charge',
						path: '/pages/vender/vender'
					}
				]
				
			}
		},
		mounted() {
			document.querySelector('.uni-page-head-hd').style.display = 'none'
		},
			
		onLoad() {

		},
		methods: {
			navItemClick (){
				location.href = 'http://localhost:8080/#/pages/payment/payment'
			}

		}
	}
</script>

<style lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	
	.nav {
		display: flex;	
		.nav_item{
			width: 50%;
			text-align: center;
			margin: 50rpx;
			view{
				width: 100rpx;
				height: 100rpx;
				border-radius: 50rpx;
				background-color:#ff584F;
				margin: 50rpx auto;
				line-height: 100rpx;
				color:#FFFFFF;
				font-size: 50rpx;
			}
			text{
				font-size: 1rpx;
				
			}
			p {
				font-size: 10px;
			}
			 
		}
		
		
	}

	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
		border-radius: 100rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
