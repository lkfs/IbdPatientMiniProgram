<template>
	<view class="container">
		<uni-search-bar></uni-search-bar>
		<view class="page-section-spacing">
			<swiper class="swiper" 
				indicator-dots="true" 
				autoplay="true" 
				interval="5000" 
				duration="1500"	>
				<swiper-item v-for="item in swiperList">
					<image :src="item.url" mode="aspectFill"></image>
				</swiper-item>
			</swiper>
		</view>
		<div>
			<template v-for="item in swiperList">
				<uni-link :href="item.url" :text="item.name"></uni-link><br>
			</template>
			<uni-link href="https://baidu.com" text="go baidu"></uni-link>
		</div>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiperList:[
					{name:"图像1", url:"https://t7.baidu.com/it/u=1956604245,3662848045&fm=193&f=GIF"},
					{name:"图像2", url:"https://t7.baidu.com/it/u=2529476510,3041785782&fm=193&f=GIF"},
					{name:"图像3", url:"https://t7.baidu.com/it/u=727460147,2222092211&fm=193&f=GIF"}
				],
				show:false
				
			}
		},
		methods: {

		}
	}
</script>

<style>
	.container {
		display: grid;
		grid-template-columns: 1fr;
	}
	
</style>
