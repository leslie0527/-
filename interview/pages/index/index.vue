<template>
	<view class="content">
		<view class="userInfo">
			<image src="../../static/userImg.png" mode=""></image>
			<text class="name">{{userName}}</text>
            <text class="phone">{{phone}}</text>
        </view>
		<view class="rider">
			<uni-list>
				<uni-list-item ><image src="/static/开启.png" mode="" class="icon"></image>开始接单
					<switch style="transform: scale(0.6);" color="#1BD5C3" @change="switch1Change" class="btn"/>
				</uni-list-item>
				<uni-list-item ><image src="/static/骑手.png" mode="" class="icon"></image>骑手接单<image  :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
				<uni-list-item ><image src="/static/历史.png" mode="" class="icon"></image>历史订单</image>骑手接单<image  :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
			</uni-list>
		</view>
		<view class="set rider">
			<uni-list>
				<uni-list-item ><image src="/static/地址.png" mode="" class="icon"></image>地址管理<image  :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
				<uni-list-item ><image src="/static/密码.png" mode="" class="icon"></image>修改密码<image :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
				<uni-list-item ><image src="/static/修改.png" mode="" class="icon"></image>修改资料<image :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
				<uni-list-item ><image src="/static/代理.png" mode="" class="icon"></image>代理中心<image :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
				<uni-list-item ><image src="/static/抽奖.png" mode="" class="icon"></image>抽奖中心<image :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
				<uni-list-item ><image src="/static/优惠券.png" mode="" class="icon"></image>我的优惠券<image :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
				<uni-list-item ><image src="/static/推荐码.png" mode="" class="icon"></image>我的推荐码<image :src="imgUrl" mode="" class="zhuandao"></image></uni-list-item>
			</uni-list>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				phone: '12312156484',
				userName:'张三',
				imgUrl:'../../static/转到.png',
			}
		},
		methods: {
			switch1Change:function(){
				console.log(1);
			}
		}
	}
</script>

<style scoped>
	.content {
		background: #FAFAFA;
		font-weight: 100;
		font-size: 14px;
	}
	.userInfo{
		background:#fff;
		line-height: 52px;
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		padding: 13px 6px;
	}
	.name{
		float: left;
		margin-left: 18px;
	}
	.phone{
		position: absolute;
		left: 65%;
	}
	.userInfo image{
		width: 50px;
		height: 50px;
	}
	.rider{
		margin-top: 57px;
		background: white;
	}
	.rider .icon{
		width: 30px;
		height: 24px;
		margin-left: 16px;
		margin-right: 18px;
		vertical-align: middle;
	}
	.rider uni-list-item{
		height: 39px;
		line-height: 39px;
		border-bottom: 1px solid #f4f4f4;
		display: block;
	}
	.btn{
		float: right;
	}
	.zhuandao{
		/* float: right; */
		height: 15px;
		width: 10px;
		vertical-align: middle;
		float: right;
		margin-top: 13px;
		margin-right: 20px;
	}
	.set{
		margin-top: 48px;
	}
</style>
