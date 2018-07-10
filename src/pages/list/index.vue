<template>
	<div>
		<div v-for="(item, index) in lists" :key="item.id" class="item" @click="gotoDetail">
			<img :src="item.picUrl" class="item-pic-url"></img>
			<div class="item-title-desc">
				<div class="item-title">{{item.title}}</div>
				<div class="item-desc">{{item.desc}}</div>
			</div>
		</div>
	</div>
</template>

<script>
export default{
	data () {
		return {
			lists: [
				{
					id : '1',
					title: 'title',
					desc: 'desc',
					picUrl: 'http://mat1.gtimg.com/www/qq2018/imgs/qq_logo_2018x2.png'
				},
				{
					id : '2',
					title: 'title',
					desc: 'desc',
					picUrl: 'http://mat1.gtimg.com/www/qq2018/imgs/qq_logo_2018x2.png'
				},
				{
					id : '3',
					title: 'title',
					desc: 'desc',
					picUrl: 'http://mat1.gtimg.com/www/qq2018/imgs/qq_logo_2018x2.png'
				}
			]
		}
	},

	methods: {
		gotoDetail () {
			const url = '../detail/main'
      		wx.navigateTo({ url })
		}
	}
}
</script>

<style>
.item{
	height: 200rpx;
	display: flex;
}
.item-pic-url{
	width: 180rpx;
	height: 180rpx;
	margin: 10rpx;
}
.item-title-desc{
	display: flex;
	flex-direction: column;
	flex: auto;
	justify-content: center;
}


</style>