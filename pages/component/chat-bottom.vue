<template>
	<view style="height: inherit;position: relative;">
		<view class="cu-bar tabbar bg-white foot round-bar">
			
		</view>
	</view>

</template>

<script>
	export default{
		methods:{
			newMessage:function(){
				uni.navigateTo({
					url:'../chat/index'
				})
			}
		}
	}
</script>

<style>
	.message-btn {
		margin-top: 38rpx;
	}
	.bg-purple-blue {
		background-image: linear-gradient(225deg, #40d4e6, #6584fd);
		color: #ffffff;
	}
	.action-new-message-btn {
		font-size: 11px;
		position: relative;
		-webkit-box-flex: 1;
		-webkit-flex: 1;
		-ms-flex: 1;
		flex: 1;
		text-align: center;
		padding: 0;
		display: block;
		height: auto;
		line-height: 1;
		margin: 0;
		/* background-color: inherit; */
		overflow: initial;
		top: -100rpx;
		background-color: transparent;
	}
	.new-message-btn {
		width: 140rpx;
		height: 140rpx;
		border-radius: 50%;
		position: relative;
		margin-left: 10rpx;
		top: 10rpx;
		display: block;
		line-height: 1;
	}
	.new-message-blank {
		width: 160rpx;
		height: 160rpx;
		border-radius: 50%;
		position: relative;
		margin: auto;
		display: block;
		line-height: 1;
		background-color: #f3f3f3;
	}

	.home-button {
		margin-left: 140rpx;
	}

	.bar-button {
		width: 60rpx;
		height: 60rpx;
	}

	.my-button {
		margin-right: 140rpx;
	}

	.round-bar {
		border-radius: 70rpx 70rpx 0 0;
	}
</style>
