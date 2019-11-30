<template>
	<view style="background-color: #f3f3f3;font-family: Didact Gothic;display: -webkit-flex;-webkit-flex-direction: column;">
		
		<cu-custom style="position: relative;" :isBack="true"><block slot="backText"></block><block slot="content">Touming Jiao</block></cu-custom>
		
		
		<chat-bottom></chat-bottom>
	</view>
</template>

<script>
	import cuCustom from '@/pages/component/cu-custom.vue';
	import chatBottom from '@/pages/component/chat-bottom.vue'
	export default{
		components:{
			cuCustom,
			chatBottom
		},
		onLoad:function(options){
			uni.loadFontFace({
			  family: 'Didact Gothic',
			  source: 'url("https://lib.baomitu.com/fonts/didact-gothic/didact-gothic-regular.ttf")',
			  success() {
			      console.log('success')
			  }
			})
		},
		onPullDownRefresh:function(){
			setTimeout(function() {
				uni.stopPullDownRefresh()
			}, 1000);
			console.log("pull")
		}
	}
</script>

<style>
	
</style>
