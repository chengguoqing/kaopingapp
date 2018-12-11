<template>
	<view>
		<view class="box cen dsf_ddrertxc bbm" :class="is_sdf==1?'act':''">
			<view class="box_a df_fd_sdrert" :class="sd.cls" v-for="sd in sd_dfg" @click="sd_sddf(sd)">
				<view class="pd fz28 z9 pr f_b df_ddeertxc">
					<text class="cz">{{sd.name}} </text>
					<text v-if="sd.num" class="yj cf num_jgg_deer fz22 cz f_b">{{sd.num}}</text> </view>
			</view>
		</view>

		<view class="df_jh_drrttxert bgff">

			<view class="pd pt20 pm20 bgff bbm ln" v-for="sd in 10">
				<view class="pr fl dsf_jh_deertxxrtt ">
					<text class="yj sd_jh_ffrg_dian"></text>
					<image src="../../static/img/dsfsdf_a.png" class=""></image>

				</view>
	
				<view class="ov pl20 pt5">
					<view class="box">
						<view class="box_b fz32">
							申述
						</view>
						<view class="box_a fz28 z9 fz26 tr">
							10/25 8:00
						</view>
					</view>
					<view class="fz28 z6">
						你收到一条申诉
					</view>
				</view>
				<view class="qc">
					
				</view>

			</view>



		</view>

		<!-- <van-tabs>
			<van-tab title="全部" sticky swipeable>
				<view class="pd pt20 pm20 bgff bbm ln" v-for="sd in 10">
					<view class="box">
						<view class="box_b fz32">
							申述
						</view>
						<view class="box_a fz30 z9 fz26 tr">
							10/25 8:00
						</view>
					</view>
					<view class="fz26 z6">
						你收到一条申诉
					</view>
				</view>

			</van-tab>
			<van-tab title="未读">
				<view class="pd pt20 pm20 bgff bbm ln" v-for="sd in 2">
					<view class="box">
						<view class="box_b fz32">
							申述
						</view>
						<view class="box_a fz30 z9 fz26 tr">
							10/25 8:00
						</view>
					</view>
					<view class="fz26 z6">
						你收到一条申诉
					</view>
				</view>
			</van-tab>
			<van-tab title="已读">
				<view class="pd pt20 pm20 bgff bbm ln" v-for="sd in 5">
					<view class="box">
						<view class="box_b fz32">
							申述
						</view>
						<view class="box_a fz30 z9 fz26 tr">
							10/25 8:00
						</view>
					</view>
					<view class="fz26 z6">
						你收到一条申诉
					</view>
				</view>
			</van-tab>
		</van-tabs> -->



	</view>
</template>
<script>
	export default {

		data() {
			return {
				sd_dfg: [{
					name: "全部",
					num: "",
					cls: "act"
				}, {
					name: "未读",
					num: "5",
					cls: ""
				}, {
					name: "已读",
					num: "",
					cls: ""
				}]
			}
		},
		components: {},
		methods: {
			sd_sddf(sd) {
				this.sd_dfg.map(a => {
					a.cls = ""
				})
				sd.cls = "act"
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.dsf_ddrertxc {
		position: fixed;
		left: 0;
		top: 0;
		z-index: 10000;
		background: #fff;
		line-height: 100upx;
		height: 100upx;
		width: 100%;
	}

	.dsf_ddrertxc.act {
		position: relative;
	}

	.df_ddeertxc {}

	.df_fd_sdrert.act .df_ddeertxc {

		color: #459FF7;
		border-bottom: 1px solid #459FF7;
	}

	.num_jgg_deer {
		/* position: absolute;
		right: 10upx;
		top: 5upx; */
		color: #fff;
		background: #FF0026;
		width: 31upx;
		height: 31upx;
		text-align: center;
		line-height: 31upx;
	}

	.df_jh_drrttxert {
		padding-top: 100upx;
	}
	.dsf_jh_deertxxrtt{
		width: 100upx;
		height: 100upx;
	}
	.dsf_jh_deertxxrtt image{
		width: 100%;
		height: 100%;
	}
	.sd_jh_ffrg_dian{
		width: 20upx;
		height: 20upx;
		position: absolute;
		right: -6upx;
		top: -6upx;
		background: #FF0026;
	}
</style>
