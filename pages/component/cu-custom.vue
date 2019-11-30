<template>
	<view class="body">
		<view class="cu-custom" :style="[{height:CustomBar + 'px'}]">
			<view class="cu-bar fixed" :style="style" :class="[bgImage!=''?'none-bg text-white bg-img':'',bgColor]">
				<view class="action" @tap="BackPage" v-if="isBack">
					<text class="cuIcon-back text-bold"></text>
					<slot name="backText"></slot>
				</view>
				<view class="content text-bold" :style="[{top:StatusBar + 'px'}]">
					<slot name="content"></slot>
				</view>
				<view>
					<text class="cuIcon-info info-btn text-bold"></text>
				</view>
				<slot name="right"></slot>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				StatusBar: this.StatusBar,
				CustomBar: this.CustomBar1
			};
		},
		name: 'cu-custom',
		computed: {
			style() {
				var StatusBar= this.StatusBar;
				var CustomBar= this.CustomBar1;
				var bgImage = this.bgImage;
				var style = `height:${CustomBar}px;padding-top:${StatusBar}px;`;
				if (this.bgImage) {
					style = `${style}background-image:url(${bgImage});`;
				}
				return style
			}
		},
		props: {
			bgColor: {
				type: String,
				default: ''
			},
			isBack: {
				type: [Boolean, String],
				default: false
			},
			bgImage: {
				type: String,
				default: ''
			},
		},
		methods: {
			BackPage() {
				uni.navigateBack({
					delta: 1
				});
			}
		}
	}
</script>

<style>
	.cu-bar .content {
	    font-size: 40rpx;
	}
	.info-btn {
		margin-right: 56rpx;
		font-size: 40rpx;
	}
	.cu-bar .action:first-child {
	    margin-left: 72rpx;
	}
	.body {
	    background-color: #f3f3f3;
	    font-size: 14px;
	    color: #4a5467;
	    font-family: Didact Gothic;
	}
</style>
