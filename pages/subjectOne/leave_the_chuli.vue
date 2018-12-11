<template>
	<view>
		<view class="bgff pt20">

			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					被罚人：
				</view>
				<view class="ov">
					<view class="df_jh_ddfrxe br">
						<picker class="picker-item" mode="selector" :range="textList">

							<text class="cz z6">管玉华 JAVA开发</text>
							<icon class="dx icon-down cz"></icon>
						</picker>
					</view>
				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					金额：
				</view>
				<view class="ov">
					<input type="number" value="10" class="df_jh_ddfrxe br ab" />

				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					事由：
				</view>
				<view class="ov pr20">
					<input type="text" value=" 上班瞌睡" class="df_jh_ddfrxe br ac z6" />

				</view>
			</view>

			<view class="dx_row pd pt10 pm10 fz28 ">
				<view class="dx_col_5 df_df_dsrtxr">
					证据：
				</view>
				<view class="ov pr20">
					<image src="../../static/img/bg_sdf.jpg" class="zhengju_der mr10 cz" v-for="sd in 3"></image>
					<view class="f_b sd_ddr br cz" @click="xztu">
						<image src="../../static/img/add_icon.png"></image>
					</view>

				</view>
			</view>


			<view class="dx_row pd pt10 pm10 fz28 pm40">
				<view class="dx_col_5 df_df_dsrtxr">
					发起人：
				</view>
				<view class="ov pr20 df_df_dsrtxr z6">

					刘峰 软件事业部经理
				</view>
			</view>




		</view>


		<view class="df_jh_drrtxrt pd">
			<navigator url="" class="dx_btn">确认开出罚单</navigator>
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
				textList: [
					'text1',
					'text2',
					'text3'
				],
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
			xztu() {
				uni.chooseImage({
					count: 6, //默认9
					sizeType: ['original', 'compressed'], //可以指定是原图还是压缩图，默认二者都有
					sourceType: ['album'], //从相册选择
					success: function(res) {
						console.log(JSON.stringify(res.tempFilePaths));
					}
				});
			},
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
		width: 60upx;
	}

	.sd_ddr image {
		width: 100%;
		height: 100%;
	}

	.df_jh_drrtxrt {
		margin-top: 400upx;
	}
</style>
