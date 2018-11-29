<!-- 产量 -->
<template>
	<view>
		<view class="pd pt40 bgff">
			<view class="yj4 dsf_hg_der dx_row ov">
				<view class="dx_col_12 df_sd_dert " @click="sd_jh_eet">
					本周
				</view>
				<view class="dx_col_12 df_sd_dert act">
					本月
				</view>

			</view>
		</view>






		<view class="pd  bgff">
			<view class="cen fz32 z6 pt40">
				电缆型号A
			</view>
			<view class="fz30 z6 pd mt20">
				成品数<br>
				共计:20

			</view>
			<view class="dsf_dfdfrs">
				<tubiao :date_d="date_d_san" :tet_m="tet_m_er" canvasId="qd_dfg_a"></tubiao>
			</view>
		</view>


		<view class="mt20 bgff pt20">
			<view class="fz30 z6 pd mt20">
				成品废品数<br>
				共计:20

			</view>
			<view class="dsf_dfdfrs">
				<tubiao :date_d="date_d_si" :tet_m="tet_m_er" canvasId="qd_dfg_b"></tubiao>
			</view>
		</view>


		<view class="mt20 bgff pt20">
			<view class="fz30 z6 pd mt20">
				成品废品数<br>
				共计:20

			</view>
			<view class="dsf_dfdfrs">
				<tubiao :date_d="date_d_si" :tet_m="tet_m_er" canvasId="qd_dfg_c"></tubiao>
			</view>
		</view>







	</view>
</template>
<script>
	import tubiao from '../../components/tubiao.vue'

	export default {
		data() {
			return {
				idx_sd: 0, //本周  1本月

				tet_m_er: [1, 2, 3, 4, 5, 6, 7, 8, 9],
				date_d_san: [
					8, 8, 3, 6, 8, 5, 8, 9, 5
				],
				date_d_si: [
					1, 1, 2, 3, 2, 3, 3, 3, 2
				],
				sd_dsdf: [{
						cls: "act",
						name: "本周"
					},
					{
						cls: "",
						name: "本月"
					}
				]
			}
		},
		components: {
			tubiao
		},
		methods: {
			sd_jh_eet() {
				uni.redirectTo({
					url: '/pages/subjectThree/yield'
				});
			},
			sd_sdf(sd, idx) {
				this.sd_dsdf.map(a => {
					a.cls = ""
				})
				this.idx_sd = idx
				sd.cls = "act"
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.dsf_dfdfrs {
		padding-top: 20upx;
		height: 440upx;
		padding-bottom: 20upx;

	}
</style>
