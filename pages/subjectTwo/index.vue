<template>
	<view class="pd pt40">

		<view class="cen">

			<image src="../../static/img/left.png" class="sdf_deert mr40 cz"></image>

			<text class="cz">2018年10月</text>

			<image src="../../static/img/right.png" class="sdf_deert ml40 cz"></image>

		</view>

		<view class="mt20">

			<van-row gutter="10">
				<van-col span="12" v-for="(sd,idx) in 4">
				
					<navigator url="/pages/subjectTwo/examination_hall" class="s_kasdrt pd pt30 pm20 mt20 pr ov">
						<view class="sanjaio">
							<text class="cf fz32 pr">4</text>
							<image src="../../static/img/sanjaio.png"></image>
						</view>

						<image src="../../static/img/user_icon.png" class="yj user_iconser fl mt10"></image>
						<view class="ov pl20">
							<view class="fz32 z3">
								陈献机
							</view>
							<view class="fz26 z9 df_dertxfcr mt5">
								软件事业部<br>
								架构师
							</view>
						</view>
						<view class="qc pm40"></view>

						<view class="dx_row_e">
							<text class="cz">客户评价</text>
							<image src="../../static/img/star.png" class="xingxing_e cz mr5" v-for="sd in 5"></image>
						</view>

						<view class="dx_row_e">
							<text class="cz">平级评价</text>
							<image src="../../static/img/star.png" class="xingxing_e cz mr5" v-for="sd in 5"></image>
						</view>

						<view class="dx_row_e ">
							<text class="cz">下级评价</text>
							<image src="../../static/img/star.png" class="xingxing_e cz mr5" v-for="sd in 5"></image>
						</view>



					</navigator>

				</van-col>

			</van-row>




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
						cls: "act",
						href: "",
						name: "我要考评被人"
					}, {
						cls: "",
						href: "/pages/subjectTwo/my_evaluation",

						name: "我的考评情况"
					},
					{
						cls: "",
						href: "",

						name: "下属考评情况"
					}
				]
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
				uni.navigateTo({
					url: sd.href
				});
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.sdf_deert {
		width: 36upx;
		height: 36upx;
	}

	.s_kasdrt {
		background: #fff;
		height: 330upx;
		border-radius: 10upx;
	}

	.user_iconser {
		width: 90upx;
		height: 90upx;

	}

	.df_dertxfcr {
		line-height: 1.2;
	}

	.xingxing_e {
		width: 24upx;
		height: 24upx;
	}

	.dx_row_e {
		color: #999;
		font-size: 26upx;
	}

	.dx_row_e text {
		margin-right: 20upx;
	}

	.sanjaio {
		width: 104upx;
		height: 104upx;
		position: absolute;
		right: 0px;
		top: 0px;
	}

	.sanjaio {
		text-align: center;
		padding-left: 50upx;
		padding-bottom: 30upx;
		line-height: 80upx;
	}

	.sanjaio text {}

	.sanjaio image {
		width: 100%;
		height: 100%;
		position: absolute;
		left: 0;
		top: 0;
	}

	
</style>
