<template>
	<view class="content">
		<button type="default" @click="getDate">getDate</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			getDate(){
				const db = uniCloud.database();
				// 获取名为 `table1` 数据表的引用
				db.collection("user").add({name: 'Ben'})
				// const collection = db.collection('user');
				// console.log(JSON.stringify(collection));
			}
		}
	}
</script>

<style>
	page{
		background-color: skyblue;
		width: 100%;
		height: 2000rpx;
		
	}
</style>
