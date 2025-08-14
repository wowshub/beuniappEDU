<template>
	<view class="scroll-row-item course course-two">
		<view class="position-relative">
<!--            <image :src="item.cover"></image> -->
            <image src="/static/demo/cover/1.png "></image>
            <view class="text-white font-sm">{{item.type | formatType}}</view>
        </view>
        <view class="flex flex-column flex-shrink"></view>
            <text class="text-ellipsis font-md mt-1" style="width: 300rpx;">{{item.title}}</text>
            <view class="font-sm text-light-muted my-1">10人已抢</view>
            <view class="flex flex-1 align-end">
                <text class="font-md text-danger">{{item.price}}</text>
                <text class="font-sm text-light-muted">{{item.t_price}}</text>
            </view>
	</view>
</template>

<script>
    
    let opt  = {
        media:"图文",
        audio:"音频",
        video:"视频",
        column:"专栏"
           
    }
	export default {
		name:"course-list",
        props: {
            item:Object,
        },
        filters: {
            formatType(k){
                return opt[k];
            } 
        },   
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.course{

    
    
    
    
}

.course-two{
      width: 340rpx; 
      margin-left: 20rpx;
      margin-bottom: 20rpx;
       
}

.course-two image, .course-two>view:first-child{
    width: 340rpx;
    height: 180rpx;
    
}

.course>view:first-child>view{
    position: absolute;
    right: 10rpx;
    bottom: 10rpx;
    background-color: rgb(0,0,0,0.4);
    padding: 0 10rpx;
    
    
}
</style>
