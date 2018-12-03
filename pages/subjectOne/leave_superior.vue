<template>
	<view class="pm100">
		<view class="bgff pt20">

			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					被罚人：
				</view>
				<view class="ov df_df_dsrtxr">
					管玉华 JAVA开发
				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					金额：
				</view>
				<view class="ov df_df_dsrtxr">
					10元

				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					事由：
				</view>
				<view class="ov pr20 df_df_dsrtxr">
					上班瞌睡

				</view>
			</view>

			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					证据：
				</view>
				<view class="ov pr20">
					<image src="../../static/img/bg_sdf.jpg" class="zhengju_der mr10 cz" v-for="sd in 3"></image>

				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					发起人：
				</view>
				<view class="ov pr20 df_df_dsrtxr z6">

					刘峰 软件事业部经理
				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					开单时间：
				</view>
				<view class="ov pr20 df_df_dsrtxr z6">

					2018-10-28 10:00:01

				</view>
			</view>



			<view class="dx_row pd pt10 pm10 fz28 pm20">
				<view class="dx_col_5 df_df_dsrtxr">
					罚单号：
				</view>
				<view class="ov pr20 df_df_dsrtxr z6">

					罚20181028号
				</view>
			</view>




		</view>


		<view class="mt20 bgff pt20">
			<view class="fz32 z3 pd">
				申诉理由
			</view>
			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					理由：
				</view>
				<view class="ov df_df_dsrtxr">
					昨晚宿舍员工太吵



				</view>
			</view>

			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					证据：
				</view>
				<view class="ov df_df_dsrtxr ls">
					附件1 附件2 附件3
				</view>
			</view>


		</view>



		<view class="mt20 bgff pt20">
			
			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					审查理由：
				</view>
				<view class="ov ">
					<textarea value="" placeholder="请输入审查理由" class="sd_kh_deert" />
				</view>
			</view>
			
			<view class="dx_row mt80 pl40 pr40 pm100">
					<view class="dx_col_12 pr20">
						<view class="dx_btn">
							拒绝
						</view>
					</view>
					
					<view class="dx_col_12 pl20">
						<view class="dx_btn">
							接受
						</view>
					</view>
			</view>
			
			
			
		</view>


		<view class="box sd_deert">
			<view class="box_a df_kse fz32" :class="sd.cls" v-for="sd in  sd_sdf" @click="xzdfd(sd)">
				{{sd.name}}
			</view>

		</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
				sd_sdf: [{
						cls: "",
						href: "/pages/subjectOne/send_bill_me",
						name: "开给我的"
					}, {
						cls: "act",
						href: "",

						name: "我开出的"
					},
					{
						cls: "",
						href: "",

						name: "统计分析"
					}
				],

			}
		},
		components: {},
		methods: {
			xzdfd(sd) {
				this.sd_sdf.map(a => {
					a.cls = ""
				})
				sd.cls = "act"
				if (!sd.href) {
					return
				}
				uni.redirectTo({
					url: sd.href
				});
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.df_jh_ddfrxe {
		display: inline-block;
		padding: 0upx 30upx !important;
		line-height: 60upx;
		height: 60upx;
	}

	.df_jh_ddfrxe.ab {
		width: 173upx;
	}

	.df_jh_ddfrxe.ac {
		width: 480upx;
	}

	.df_df_dsrtxr {

		line-height: 60upx;
	}

	.zhengju_der,
	.sd_ddr {
		width: 75upx;
		height: 60upx;
	}

	.sd_ddr {
		text-align: center;
		line-height: 40upx;
		font-size: 40upx;
	}

	.df_jh_drrtxrt {
		margin-top: 400upx;
	}
	
</style>
