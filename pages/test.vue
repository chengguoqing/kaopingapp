<template>
	<view>
		<view class="box cen fz30 bbm bgff sd_jh_deettxcr">
			<view class="box_b" :class="kjh_sdf?'ls':''" @click="kjh_sdf_b=false;kjh_sdf=true">
				{{ssd_ad_a}}
				<image src="../static/img/down_po.png" class="sd_jkjh_dert cz"></image>
			</view>
			<view class="box_a">
				至
			</view>
			<view class="box_b" :class="kjh_sdf_b?'ls':''" @click="kjh_sdf_b=true;kjh_sdf=false">
				{{ssd_ad_b}}
				<image src="../static/img/down_po.png" class="sd_jkjh_dert cz"></image>
			</view>
		</view>

		<picker-view class="sd_jh_deerrttx" indicator-style="height: 50px;" :value="value" @change="bindChange">
			<picker-view-column>
				<view class="item" v-for="item in years" :key="item">{{item}}年</view>
			</picker-view-column>
			<picker-view-column>
				<view class="item" v-for="item in months" :key="item">{{item}}月</view>
			</picker-view-column>
			<picker-view-column>
				<view class="item" v-for="item in days" :key="item">{{item}}日</view>
			</picker-view-column>
		</picker-view>

		<view class="pd bgff pt30 pm20">
			<view class="dx_btn w100">
				确定
			</view>
		</view>


	</view>
</template>
<script>
	export default {
		data: function() {
			const date = new Date()
			const years = []
			const year = date.getFullYear()
			const months = []
			const month = date.getMonth() + 1
			const days = []
			const day = date.getDate()

			for (let i = 1990; i <= date.getFullYear(); i++) {
				years.push(i)
			}

			for (let i = 1; i <= 12; i++) {
				months.push(i)
			}

			for (let i = 1; i <= 31; i++) {
				days.push(i)
			}
			return {
				ssd_ad_a: "开始时间",
				ssd_ad_b: "结束时间",
				kjh_sdf: true,
				kjh_sdf_b: false,
				title: 'picker-view',
				years,
				year,
				months,
				month,
				days,
				day,
				value: [9999, month - 1, day - 1],
				visible: false,
				indicatorStyle: `height: ${Math.round(uni.getSystemInfoSync().screenWidth/(750/100))}px;`
			}
		},
		methods: {
			bindChange: function(e) {
				const val = e.detail.value
				this.year = this.years[val[0]]
				this.month = this.months[val[1]]
				this.day = this.days[val[2]]
				if (this.kjh_sdf) {
					this.ssd_ad_a = this.year + "-" + this.month + "-" + this.day
				}
				if (this.kjh_sdf_b) {
					this.ssd_ad_b = this.year + "-" + this.month + "-" + this.day
				}

			}
		},
		onLoad() {
			/**
			 * 延迟渲染picker-view组件，避免数据同步问题
			 */
			setTimeout(() => {
				this.visible = true
			}, 0)
		}
	}
</script>
<style scoped>
	.sd_jh_deerrttx {
		height: 400upx;
		text-align: center;
		background: #fff;
		line-height: 80upx;
		font-size: 28upx;
	}

	.sd_jkjh_dert {
		width: 35upx;
		height: 35upx;
	}

	.sd_jh_deettxcr {
		line-height: 100upx;
	}
</style>
