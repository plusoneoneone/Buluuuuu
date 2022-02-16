// An highlighted block
<template>
	<view class="content">
		<view class="form">
			<view class="inputWrapper">
				<input class="input" type="text" value="" placeholder="请输入用户名"/>
			</view>
			<view class="inputWrapper">
				<input class="input" type="password" value="" placeholder="请输入密码"/>
			</view>
			<view class="loginBtn" @click="navItemClick">
				<text class="btnValue">登录</text>
			</view>
			<!-- <view class="forgotBtn">
				<text>找回密码</text>
			</view> -->
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		mounted() {
			document.querySelector('.uni-page-head-hd').style.display = 'none'
		},
			
		methods: {
			navItemClick (){
				location.href = 'http://localhost:8080/#/pages/vender/vender'
				
			}
			

		}
	}
</script>

<style>
	.content {
		/* background: #377EB4; */
		width: 100vw;
		height: 100vh;
	}
	.avatorWrapper{
		height: 30vh;
		width: 100vw;
		display: flex;
		justify-content: center;
		align-items: flex-end;
	}
	.avator{
		width: 200upx;
		height: 200upx;
		overflow: hidden;
	}
	.avator .img{
		width: 100%
	}
	.form{
		padding: 0 100upx;
		margin-top: 80px;
	}
	.inputWrapper{
		width: 100%;
		height: 80upx;
		background: white;
		border-radius: 20px;
		box-sizing: border-box;
		padding: 0 20px;
		margin-top: 25px;
	}
	.inputWrapper .input{
		width: 100%;
		height: 100%;
		text-align: center;
		font-size: 15px;
	}
	.loginBtn{
		width: 100%;
		height: 80upx;
		background: #FF584F;
		border-radius: 50upx;
		margin-top: 50px;
		display: flex;
		justify-content: center;
		align-items: center;
		
	}
	.loginBtn .btnValue{
		color: white;
	}
	.forgotBtn{
		text-align: center;
		color: #EAF6F9;
		font-size: 15px;
		margin-top: 20px;
	}
</style>
