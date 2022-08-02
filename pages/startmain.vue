<template>
	<view class="content">
		<view>title:{{title}}</view>
		<view>received params: {{params}}</view>
		<view>fullname: {{fullname}}</view>
	</view>
	<Users />
</template>

<script setup>
	import {onShow, onReady, onHide, onLoad} from '@dcloudio/uni-app'
	import {ref, onMounted, reactive, computed} from 'vue'
	
	let params = null
	let person = reactive({first:'firstname', last:'lastname'})
	const title = ref(1)
	const fullname = computed(() => {
		return `${person.first}-${person.last}`
	})
	onLoad((options) => {
		params = options
	})
	onShow(()=>{  
		console.log('onShow')
	})  
	onMounted(() => {
		console.log(params)
	})
	onReady(()=>{  
		console.log('onReady')
	})
</script>
<script>	
	import Users from './components/Users.vue'
	export default {
	  components: {
		  Users
	  }
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
</style>