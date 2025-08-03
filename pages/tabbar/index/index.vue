<template>
	<view >
		<f-search-bar></f-search-bar>
        <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" style="height: 300rpx;">
<!--        <swiper-item class="flex justify-center">
                <image src="/static/demo/banner/banner1.png" mode="aspectFill" style="width: 720rpx;height: 300rpx;" class="rounded shadow"></image>
            </swiper-item>
            
            <swiper-item class="flex justify-center">
                <image src="/static/demo/banner/banner2.png" mode="aspectFill" style="width: 720rpx;height: 300rpx;" class="rounded shadow"></image> -->
            <swiper-item class="flex justify-center" v-for="(item,index) in swiper":key="index">
                 <image :src="item.src" mode="aspectFill" style="width: 720rpx;height: 300rpx;" class="rounded shadow"></image>
            </swiper-item>    
                          
        </swiper>
        
        <icon-nav :list="iconNav"></icon-nav>   
         
        <coupon-list></coupon-list>
        
        <view class="divider"></view>
        
        <view class="flex align-center py-3 px-2"> 
              <text class="font-md font-weight-bold">拼团</text>
        </view>

        <scroll-view scroll-x="true"  class="scroll-row">
            <course-list></course-list>
        </scroll-view>
        
        
        
<!-- 		<view class="flex align-center justify-center flex-column  flex-suojing2 py-3 bg-danger">
        <text class="text-white"> 在线教育-执业医师一类题库 视频 资料站</text>
		<text class=" text-white"> 详见：</text> 
         <uni-link
            class="be-link"
            :href="href"
            :text="href"
            target="_blank"
            color="#000" 
         />
        </view> -->
        
<!--        <view class="bg-main flex align-center justify-center py-3 animate__animated animate__bounce">
            <text class="iconfont icon-xiayibu" style="font-size: 30px;">  在线教育-执业医师一类题库 视频 资料站</text>
          
        </view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
                swiper:[
                    {src:"/static/demo/banner/banner1.png"},
                    {src:"/static/demo/banner/banner2.png"}
               ],
               iconNav:[
                   {name:"活动",
                   src:"/static/demo/icon/hd.png"
                   },
                   {name:"考试",
                   src:"/static/demo/icon/test.png"
                   },
                   {name:"秒杀",
                   src:"/static/demo/icon/ms.png"
                   },
                   {name:"拼团",
                   src:"/static/demo/icon/pt.png"
                   },
                   {name:"直播",
                   src:"/static/demo/icon/course.png"
                   },
                   {name:"专栏",
                   src:"/static/demo/icon/column.png"
                   },
                   {name:"电子书",
                   src:"/static/demo/icon/book.png"
                   },
                   {name:"社区",
                   src:"/static/demo/icon/ask.png"
                   }
               ]
				// href: 'https://chatgpt.yangyanghub.com'
			}
		},
		methods: {

		}
	}
</script>

<style>
/* 	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	} */
    


</style>


