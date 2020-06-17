<template>
	<view class="container">
		<uni-card title="uni-ui" note="Tips">
				<view class="nav_bottom">
					<view class="btnbox" @tap='btnclick'>
						11
					</view>
					<view class="btnbox" @tap="btnclick">
						2
					</view>
					<view class="btnbox" @tap="btnclick">
						3
					</view>
				</view>
		</uni-card>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/collocation/pages?id=easycom'
			}
		},
		  onLoad() {  
		            var innerAudioContext = this.innerAudioContext = uni.createInnerAudioContext();  
		            innerAudioContext.autoplay = false;  
		            innerAudioContext.src = './../../static/btn.mp3';  
		            innerAudioContext.onPlay(() => {  
		                console.log('开始播放');  
		            });  
		            innerAudioContext.onError((res) => {  
		                console.log(res.errMsg);  
		                console.log(res.errCode);  
		            });  
		        },  
		        methods: {  
		            btnclick() {  
		                this.innerAudioContext.play();  
		            }  
		        }  
	}
</script>

<style>
	.btnbox {
		width: 100px;
		background-color: #007AFF;
		text-align: center;
		margin: 10px;
	}
</style>
