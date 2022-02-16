<template>
    <view class="container">
        <view>
            <form @submit="formSubmit" @reset="formReset">
				<!-- 
				<view class="uni-form-item uni-column">
				    <view class="title" style="font-weight: bold; font-size: large;">充值</view>
				    <input class="uni-input" name="input" placeholder="請输入充值金額" />
				</view>
				
				<br/><br/>  -->
				
				
				
				<view class="c1">
					<view class="uni-btn-v">
						<button class="b2" @click="navItemClick">$ 50</button>
						<button class="b2"@click="navItemClick">$ 200</button>
						<button class="b2"@click="navItemClick">$ 1000</button>
						<button class="b2"@click="navItemClick">$ 1500</button>
						<button class="b2"@click="navItemClick">$ 2000</button>
						<button class="b2"@click="navItemClick">$ 1000 送 188(春節限定)</button>
						<!-- <button class="b1" form-type="submit">Submit</button> -->
						<!-- <button type="default" form-type="reset">Reset</button> -->
					</view>
				</view>
			</form>
		</view>
	</view>
</template>				
				
<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui'
			}
		},
		mounted() {
			document.querySelector('.uni-page-head-hd').style.display = 'none'
		},
			
		methods: {
			navItemClick (){
				console.log('tiaozhan')
				location.href = 'http://localhost:8080/#/pages/test/test'
				
			}

		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
	.uni-form-item .title {
        padding: 20rpx 0;
    }
	.b1 {
		background: #e2062c;
		color: white;
	}
	.r1 {
		margin-right:;
	}
	
	.c1 {
		display: flex;
	
	}
	.b2 {
		width: 50%;
		display: inline-flex;
	}
</style>
