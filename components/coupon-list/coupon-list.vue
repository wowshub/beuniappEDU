<template>
        <view class="p-2">
            <scroll-view scroll-x="true" class="scroll-row" >
                <view  v-for="i in 3" :key="i" class="coupon">
                    
                    <view>
                        <text>¥100元</text>
                        <text class="font">¥满200元可用</text>
                    </view>
                    
                    <view hover-class="bg-hover-warning" >
                    领取
                    </view>
                    
                </view>
            </scroll-view>
            
            
            
        </view>
</template>

<script>
	export default {
		name:"coupon-list",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
    .coupon{
        width: 310rpx; 
        display: inline-flex;
        color: #ffffff;
        margin-right: 20rpx;
        
    }
    .coupon>view:first-child{
        display: flex;
        flex-direction:column!important;
        align-items: center!important;
        justify-content:center;
        background-color: #d39e00;
        padding-left: 30rpx; padding-right: 30rpx;
        padding-top: 20rpx; padding-bottom: 20rpx;
        border-right:4rpx dashed; 
    }
    .coupon>view:last-child{
        width: 120rpx;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background-color: #ffc107;
        font-size: 30rpx!important;
    }
    .bg-hover-warning{
        background-color: #d39e00!important; /* 按下时背景变色测试 */
    }

</style>
