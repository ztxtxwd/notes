<template>
	<view>
		<view class="cu-custom" :style="[{height:CustomBar + 'rpx'}]">
			<view class="cu-bar fixed round-bar tabbar aero" :style="style" :class="[bgImage!=''?'none-bg text-white bg-img':'',bgColor]" style="background-color: #FFF3E2;">
				<view style="width: 100%;" class="bar-shadow">
					<view class="flex padding-lr-xxl padding-bottom-xl padding-top-xl justify-between">
						<view class="bar-text">
							<slot name="backText"></slot>
						</view>
						<view>
							<image src="../../static/icons/more.svg" class="more-button" mode="aspectFit"></image>
						</view>
					</view>
					<view class="padding-lr-lg">
						<view class="search-form round search">
							<image src="../../static/icons/search.svg" class="search-button" mode="aspectFit"></image>
							<input @focus="InputFocus" style="margin-left: 16rpx;" @blur="InputBlur" :adjust-position="false" type="text"
							 placeholder="搜索内容" confirm-type="search" placeholder-class="ph-text"></input>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				StatusBar: this.StatusBar,
				CustomBar: this.CustomBar
			};
		},
		name: 'cu-custom',
		computed: {
			style() {
				var StatusBar = this.StatusBar;
				var CustomBar = this.CustomBar;
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
	

	.padding-lr-xxl {
		padding-left: 60rpx;
		padding-right: 60rpx;
	}

	.search-button {
		width: 38rpx;
		height: 38rpx;
		margin-left: 60rpx;
	}

	.ph-text {
		font-size: 24rpx;
		color: #403833;
	}

	.cu-bar .search-form {
		background-color: #FFFFFF;
	}

	.round-bar {}

	.bar-shadow {
		height: 100%;
	}

	.search {
		padding-top: 44rpx;
		padding-bottom: 44rpx;
		color: #0081FF;
	}

	.more-button {
		width: 55rpx;
		height: 55rpx;
		border-radius: 27rpx;
	}

	.bar-text {
		color: #403833;
		font-size: 55rpx;
		font-weight: bold;
	}

	.search-form {
		margin: 0 0;
	}

	.more-button:active {
		background-color: #fff3e2;
	}
</style>
