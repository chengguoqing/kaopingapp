<template>
	<view class="content">
		<van-notice-bar left-icon="https://img.yzcdn.cn/public_files/2017/8/10/6af5b7168eed548100d9041f07b7c616.png" text="足协杯战线连续第2年上演广州德比战，上赛季半决赛上恒大以两回合5-3的总比分淘汰富力。" />

		<view class="swiper_xdfg ">
			<swiper :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration" circular="true"
			 :indicator-active-color="active_color" :indicator-color="indicator">
				<block v-for="item in imgUrls">
					<swiper-item>
						<image :src="item" class="slide-image" width="355" height="150" />
					</swiper-item>
				</block>
			</swiper>
		</view>

		<view class="bgff">


			<view class="pd pt20 pm20">
				<view class="fz26 z9">
					本月合附加值
				</view>
				<view class="fz40 ls mt10">
					1438.00
				</view>
			</view>

			<van-row>
				<van-col span="12">
					<view class="pd pt20 pm20 brm">
						<view class="fz32 z3">
							合累计收入
						</view>
						<view class="fz26 z9">
							1600.00
						</view>
					</view>

				</van-col>
				<van-col span="12">
					<view class="pd pt20 pm20">
						<view class="fz32 z3">
							合累计费用
						</view>
						<view class="fz26 z9">
							1600.00
						</view>
					</view>

				</van-col>


				<van-col span="12">
					<view class="pd pt20 pm20 btm brm">
						<view class="fz32 z3">
							合附加价值同比
						</view>
						<view class="fz26 z9">
							+300
						</view>
					</view>

				</van-col>



				<van-col span="12">
					<view class="pd pt20 pm20 btm">
						<view class="fz32 z3">
							合附加价值环比
						</view>
						<view class="fz26 z9">
							562.00
						</view>
					</view>

				</van-col>
			</van-row>


		</view>

		<view class="dsf_jh_det pt30">

			<van-row>
				<van-col span="6" v-for="sd in 6">
					<view class="cen mb30">


						<image src="../../static/img/mai.png" class="sd_derttxc"></image>
						<view class="fz30 ">
							我要买
						</view>
					</view>
				</van-col>
			</van-row>

		</view>


	</view>
</template>

<script>
	export default {
		data() {
			return {

				imgUrls: [ //轮播图
					'https://duxinggj-2018-1251133427.cos.ap-guangzhou.myqcloud.com/upload_ef46110abaeaa912e2d1d2f0cd0dd641.jpg',
					'https://duxinggj-2018-1251133427.cos.ap-guangzhou.myqcloud.com/upload_ef46110abaeaa912e2d1d2f0cd0dd641.jpg',
					'https://duxinggj-2018-1251133427.cos.ap-guangzhou.myqcloud.com/upload_ef46110abaeaa912e2d1d2f0cd0dd641.jpg'
				],
				indicatorDots: true, //是否显示点点
				autoplay: true, //自动播放
				active_color: "#DB1D3C", //点选中的颜色
				indicator: "#B4B4B4", //点的颜色
				interval: 5000,
				duration: 1000,

			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style scoped>
	.swiper_xdfg image {
		width: 100%;
		height: 100%;
	}

	.swiper_xdfg swiper {
		height: 285upx
	}

	.dsf_jh_det {
		border-top: 20upx solid #F5F5F5;
	}

	.sd_derttxc {
		width: 95upx;
		height: 95upx;
	}
</style>
