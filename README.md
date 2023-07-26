# u-svg-icon
基于字体的图标集，支持uni-icon字体库，支持自定义icon，支持svg，支持base64

## 1. Props
| 参数	| 说明	| 类型	| 默认值	| 是否必填 | 
| -- | -- | -- | -- | -- | 
type |	图标名称，支持uni-icon字体库，支持自定义icon，支持svg，如名称带有/，会被认为是图片图标 |	String |	- |	是 |
color |	图标颜色 |	String |	#3c9cff |	- |
size |	图标字体大小，单位默认rpx |	String / Number	 | 48rpx |	- |
index |	一个用于区分多个图标的值，点击图标时通过click事件传出 |	String / Number |	- |	- |
width |	name为图片路径时图片的宽度，单位默认rpx |	String / Number |	- |	- |
height | name为图片路径时图片的高度，单位默认rpx |	String / Number	 |-	 |- |
stop |	是否阻止事件传播，仅支持自定义图标和图片图标 |	Boolean |	false |	- |
bold |	是否显示粗体, 不支持图片图标 |	Boolean |	false |	- |

## 2. Event

| 事件名	| 说明	| 回调参数	|
| --- | --- | --- |
| svg-click	| 点击图片图标 | 返回当前图标索引index，若未传index, 则返回undefined |
| click	| 点击icon图标 | 返回当前图标索引index，若未传index, 则返回undefined |

## 3. 使用
```html
<template>
	<view class="content">
		<!-- uni-icons -->
		<view class="item">
			<text>uni-icon</text>		
			<u-svg-icon
				:type="uniIconType"
				size="48rpx" 
				index='0'
				stop="true"
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
				stop="true"
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
				stop="true"
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
```