<template>
	<view class="content">
		<view class="swiper-wrap">
			<swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="5000" :duration="500">
				<swiper-item>
					<view class="swiper-item uni-bg-red">认识自己的无知是认识世界的最好方法</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item uni-bg-green">每一个不曾起舞的日子，都是对生命的辜负</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item uni-bg-blue">种一棵树的最好时间是十年前，其次是现在</view>
				</swiper-item>
			</swiper>
		</view>

		<view class="search-wrap">
			<input class="uni-input" confirm-type="text" placeholder="搜索" />
		</view>

		<view class="books-wrap">
			<view class="book" v-for="(book,index) in bookList" :key="index">
				<view class="image-view">
					<image class="book-image" :src="book.image"></image>
				</view>
				<view class="book-title">{{book.title}}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				bookList: [{
						title: '人间失格',
						image: 'http://img3m5.ddimg.cn/56/4/23761145-1_l_2.jpg'
					},
					{
						title: '活着',
						image: 'http://img3m0.ddimg.cn/7/27/25137790-1_l_2.jpg'
					},
					{
						title: '追风筝的人',
						image: 'http://img3m5.ddimg.cn/26/14/25238195-1_l_3.jpg'
					},
					{
						title: '小熊和最好的爸爸',
						image: 'http://img3m1.ddimg.cn/31/4/20039611-1_l_9.jpg'
					},
					{
						title: '夏洛的网',
						image: 'http://img3m6.ddimg.cn/7/21/23546266-1_l_6.jpg'
					},
					{
						title: '我喜欢生命本来的样子(周国平经典散文作品集)',
						image: 'http://img3m0.ddimg.cn/28/30/24198400-1_l_4.jpg'
					},
					{
						title: '摆渡人',
						image: 'http://img3m3.ddimg.cn/27/0/27849123-1_b_3.jpg'
					}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;

		width: 750rpx;
		margin: 0;
		background: #e7e7e7;
	}

	.swiper-wrap {
		width: 100%;
		height: 350rpx;
	}

	.swiper {
		height: 350rpx;
	}

	.swiper-item {
		display: block;
		height: 350rpx;
		line-height: 350rpx;
		text-align: center;
	}

	.search-wrap {
		width: 710rpx;
		margin: 10rpx 30rpx;
	}

	.books-wrap {
		width: 100%;
		box-sizing: border-box;
		padding: 10rpx 10rpx;
		background: #ffffff;

		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
	}

	.book {
		width: 240rpx;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.image-view {
		width: 100%;
		height: 240rpx;
	}

	.book-image {
		width: 100%;
		height: 100%;
	}
	
	.book-title {
		width: 100%;
		text-align: center;
		text-overflow: ellipsis;
		white-space: nowrap;
		overflow: hidden;
	}
</style>
