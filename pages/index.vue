<template>
	<view class="content">
		<image class="logo" src="/static/logo.jpg"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
<!-- 		<navigator url="/pages/main?id=1&name=test" hover-class="navigator-hover">
			<button type="default">跳转到新页面并传参</button>
		</navigator> -->
		<view>
			<button type="primary" @click="startmain">Start</button>
		</view>
	</view>
</template>

<script setup>
	import {onShow, onReady, onHide, onLoad} from '@dcloudio/uni-app'
	import {ref, onMounted, reactive, computed} from 'vue'
	
	const title = 'Welcome to KuLiao'
	function startmain(){
		uni.navigateTo({
			url: '/pages/startmain?id=2&name=test2'
		})
	}
	onLoad((options) => {
	})
	onMounted(() => {
	})
	onShow(()=>{
	})  
	onReady(()=>{
	})
	
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
