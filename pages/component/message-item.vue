<template>
	<view class="margin-xl item padding-lg">
		<view class="flex item-middle justify-between">
			<view class="name-text text-bold ">标题</view>
			<view class="time-text text-bold ">5 min</view>
		</view>


		<view class="item-end">
			

		</view>
		<view class="content-text text-bold margin-top-sm">A man was saying must be true, but he did not need to say that he knows it.A man was saying must be true, but he did not need to say that he knows it.A man was saying must be true, but he did not need to say that he knows it.A man was saying must be true, but he did not need to say that he knows it.</view>
	</view>
</template>

<script>
	export default {
		props: [
			'imgUrl'
		]
	}
</script>

<style>
	.item {
		background-color: #fec674;
		border-radius: 50rpx;
		height: 210rpx;
	}

	.time-text {
		color: #403833;
		font-size: 26rpx;
		white-space: nowrap;

	}

	.content-text {
		height: 65rpx;
		font-size: 26rpx;
		color: #403833;
		-webkit-line-clamp: 2; //设置 需要显示的行数
		overflow: hidden;
		text-overflow: ellipsis; //文字隐藏后添加省略号
		line-height: 36rpx;
	}

	.name-text {
		color: #403833;
		font-size: 32rpx;
	}

	.item-middle {
		
	}

	.item-end {
		margin-right: 0;
		padding-right: 0rpx;
	}
</style>
