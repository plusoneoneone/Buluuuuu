<template>
		<view class="content">
				<view class="ecard">
					<view class="canvas">
								<ayQrcode ref="qrcode" :modal="modal_qr" :url="url" @hideQrcode="hideQrcode" 
								:is_themeImg="true"
								themeImg="../../static/images.jfif"
								:h_w_img="40"
								style="align-items: center;"/>
							</view>
				</view>
			</view>
			
		
</template>

<script>
	import ayQrcode from "@/components/ay-qrcode/ay-qrcode.vue"
		export default {
			components: {
				ayQrcode,
	
			},
			data() {
				return {
					//二维码相关参数
					modal_qr: false,
					url: 'https://pixabay.com/images/search/?order=ec', // 要生成的二维码值
					
				}
			},
			mounted() {
				document.querySelector('.uni-page-head-hd').style.display = 'none'
			},
				
	
			onLoad() {
				let that = this;
				that.showQrcode();//一加载生成二维码
				
			},
			methods: {
				
				// 展示二维码
				showQrcode() {
					let _this = this;
					this.modal_qr = true;
					// uni.showLoading()
					setTimeout(function() {
						// uni.hideLoading()
						_this.$refs.qrcode.crtQrCode()
					}, 10)
				},
	
				//传入组件的方法
				hideQrcode() {
					this.modal_qr = false;
				},
			}
	 
		}
</script>

<style scoped>
	.content {
		display: -webkit-flex;
		display: flex;
		flex: 1;
		flex-direction: column;
		align-content: center;
		flex-wrap: wrap;
		background-color: #efeff4;
	}

	.ecard {
		display: -webkit-flex;
		display: flex;
		flex-direction: column;
		flex-wrap: wrap;
		justify-content: center;
		align-content: center;
		background-color: #ffffff;
		margin: 60rpx 40rpx 40rpx 40rpx;
		width: 800rpx;
		height: 500rpx;
		border-radius: 25px;
	}

	.canvas {
		width: 400rpx;
		height: 400rpx;
		justify-content: center
		
	}
</style>



