<template style="color: #FEF2E2;">
	<view style="background-color: #FEF2E2;font-family: Didact Gothic;">
		
		<cu-custom>
			<view slot="backText">Notes</view>
		</cu-custom>
		<view style="margin-top: 192rpx;">
			<messageItem v-for="(item,index) in messageItems" v-bind:key= "index" :imgUrl="item.avatar"></messageItem>
		</view>
		
		
		<bottom-bar></bottom-bar>
	</view>
	
</template>

<script>
	import messageItem from '@/pages/component/message-item.vue';
	import bottomBar from '@/pages/component/bottom-bar.vue'
	export default {
		components: {
			messageItem,
			bottomBar
		},
		data(){
			return{
				messageItems:[
					{
						id:1,
						avatar:"https://s1.ax1x.com/2019/11/20/MRyIoj.jpg",
						text:"晚上出来玩吗？",
						name:"李丹",
						time:"5 min"
					},{
						id:1,
						avatar:"https://s1.ax1x.com/2019/11/20/MR616f.jpg",
						text:"晚上出来玩吗？",
						name:"李丹",
						time:"5 min"
					},{
						id:1,
						avatar:"https://s1.ax1x.com/2019/11/20/MR6GnS.jpg",
						text:"晚上出来玩吗？",
						name:"李丹",
						time:"5 min"
					},{
						id:1,
						avatar:"https://s1.ax1x.com/2019/11/20/MR6J0g.jpg",
						text:"晚上出来玩吗？",
						name:"李丹",
						time:"5 min"
					},{
						id:1,
						avatar:"https://s1.ax1x.com/2019/11/20/MR6ahn.jpg",
						text:"晚上出来玩吗？",
						name:"李丹",
						time:"5 min"
					},{
						id:1,
						avatar:"https://s1.ax1x.com/2019/11/20/MR6wpq.jpg",
						text:"晚上出来玩吗？",
						name:"李丹",
						time:"5 min"
					},{
						id:1,
						avatar:"https://s1.ax1x.com/2019/11/20/MR6010.jpg",
						text:"晚上出来玩吗？",
						name:"李丹",
						time:"5 min"
					}
				]
			}
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
	page {
		background-color: #FEF2E2;
	}
</style>
