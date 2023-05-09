<template>
	<view class="content">
		<!-- uni-icons -->
		<view class="item">
			<text>uni-icon</text>		
			<u-svg-icon
				:type="uniIconType"
				size="48rpx" 
				index='0'
				:stop="true"
				:bold="true"
				@click="handleClick"
			></u-svg-icon>
		</view>
		<!-- 自定义icon -->
		<view class="item">
			<text>自定义icon</text>
			<u-svg-icon
				:type="qdIconType"
				size="48rpx" 
				color="#CC1317"
				index='1'
				:stop="true"
				:bold="true"
				@click="handleClick"
			></u-svg-icon>
		</view>
		<!-- svg -->
		<view class="item">
			<text>svg图片</text>
			<u-svg-icon 
				:type="svgType"
				size="64rpx"
				index='2'
				:stop="true"
				@svg-click="handleClick"
			></u-svg-icon>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				uniIconType:'checkmark-circle',
				qdIconType:'qdfont qd-delivery',
				svgType:'/static/register.svg',
			}
		},
		methods: {
			handleClick(index){
				console.log(`点击了第${index}个图标`)
			},
			handleSvgClick(index){
				console.log(`点击了第${index}个svg图标`)
			}
		}
	}
</script>

<style lang="scss" scoped>
.content{
	margin: 20rpx;
	.item{
		margin: 20rpx;
	}
}
</style>
