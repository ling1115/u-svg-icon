# u-svg-icon
基于字体的图标集，支持uni-icon字体库，支持自定义icon，支持svg

## 1. Props
| 参数	| 说明	| 类型	| 默认值	| 是否必填 | 
| -- | -- | -- | -- | -- | 
type |	图标名称，支持uni-icon字体库，支持自定义icon，支持svg，如名称带有/，会被认为是图片图标 |	String |	- |	是 |
color |	图标颜色 |	String |	#3c9cff |	- |
size |	图标字体大小，单位默认rpx |	String / Number	 | 48rpx |	-
bold |	是否显示粗体 |	Boolean |	false |	- |
index |	一个用于区分多个图标的值，点击图标时通过click事件传出 |	String / Number |	- |	- |
width |	name为图片路径时图片的宽度，单位默认rpx |	String / Number |	- |	- |
height | name为图片路径时图片的高度，单位默认rpx |	String / Number	 |-	 |- |
stop |	是否阻止事件传播，仅支持自定义图标和图片图标 |	Boolean |	false |	- |

## 2. Event

| 事件名	| 说明	| 回调参数	|
| --- | --- | --- |
| svg-click	| 点击图片图标 | 返回当前图标索引index，若未传index, 则返回undefined |
| click	| 点击icon图标 | 返回当前图标索引index，若未传index, 则返回undefined |