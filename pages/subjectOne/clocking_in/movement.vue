<template>

	<view class="pm50">

		<view class="pr dfg_drrt" :class="iy_sdf">
			<rili :is_ddf="is_ddf" @sddffff="sddffff" is_down="act" is_hd="act"></rili>

		</view>

		<view class="qc">

		</view>
		<view class="map_diteeretu pr" v-if="iy_sdf">
			<map style="width: 100%; height: 100%;" :latitude="latitude" :longitude="longitude" :markers="covers">
			</map>
		</view>
		<view class="map_diteeretu pr" v-if="!iy_sdf">
			<map style="width: 100%; height: 100%;" :latitude="latitude" :longitude="longitude" :polyline="covers">
			</map>
		</view>


		<view class="df_fdf_row btm pt20 pm20 bgff pd" v-for="(sd,idx) in 3">
			<view class="f_b pr fl">
				<text class="sd_jh_deertxr">{{idx+1}}</text>
				<image src="../../../static/img/map_er.png" class="map_er"></image>
			</view>
			<view class="ov pl20 ln">
					<view class="z3 fz30">
						8:30：05  <text class="fz26 z9">(停留时间：30分钟)</text>
					</view>
					<view class="fz26 z9">
						海南省海口市迎宾路棕榈公寓
					</view>
			</view>
			
		</view>


	</view>




	</view>
</template>
<script>
	import rili from "@/components/rili.vue"
	export default {
		data() {
			return {
				iy_sdf: "",
				is_ddf: true,
				title: 'map',
				latitude: 39.909,
				longitude: 116.39742,
				polyline: [{
					latitude: 39.909,
					longitude: 116.39742,
					iconPath: '/static/img/map_ww.png'
				}, {
					latitude: 39.90,
					longitude: 116.39,
					iconPath: '/static/img/map_ww.png'
				}],
				covers: [{
					latitude: 39.909,
					longitude: 116.39742,
					iconPath: '/static/img/map_ww.png'
				}, {
					latitude: 39.90,
					longitude: 116.39,
					iconPath: '/static/img/map_ww.png'
				}]

			}
		},
		components: {
			rili
		},
		methods: {
			sddffff() {
				this.iy_sdf ? this.iy_sdf = '' : this.iy_sdf = 'act'
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.dfg_drrt {
		height: 250upx;
	}

	.dfg_drrt.act {
		height: 800upx !important;
	}

	.map_diteeretu {
		height: 460upx;
	}

	.map_er {
		width: 46upx;
		height: 57upx;
	}

	.sd_jh_deertxr {
		color: #fff;
		position: absolute;
		left: 16upx;
		top: 10upx;
		font-size: 24upx;
	}
</style>
