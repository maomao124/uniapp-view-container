<template>
	<view>
		<movable-area>
			<movable-view direction="all" @change="change" :out-of-bounds="true" :inertia="true"></movable-view>
		</movable-area>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			change(e)
			{
				console.log("事件触发,",e);
			}
		}
	}
</script>

<style>
movable-area{
	width: 300px;
	height: 600px;
	background-color: aqua;
}
movable-view{
	width: 30px;
	height: 30px;
	background-color: red;
}
</style>
