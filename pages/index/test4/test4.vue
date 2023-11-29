<template>
	<view>
		<scroll-view :scroll-y="true" :lower-threshold="100" @scroll="scroll()" @scrolltolower="lower()">
			<view v-for="item in list" :key="item">{{item}}</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list:[]
			}
		},
		methods: {
			lower()
			{
				console.log("到底了");
				const index=this.list.length;
				for (var i = index; i < index+50; i++) {
					this.list.push(i)
				}
			},
			scroll(e)
			{
				console.log("滚动事件触发");
			}
		},
		onLoad() {
			for (var i = 0; i < 50; i++) {
				this.list.push(i)
			}
		}
	}
</script>

<style>
scroll-view{
	height: 500px;
	background-color: antiquewhite;
}
</style>
