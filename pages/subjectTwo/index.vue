<template>
	<view class="df_df_ddrert pt40">

		<view class="cen">

			<image src="../../static/img/left.png" class="sdf_deert mr40 cz"></image>

			<view class="cz f_b"><picker class="picker-item" mode="date"  @change="dateChange" end="2020-01-01" start="2010-01-01">
					        
								 {{time}} 
					
					        </picker></view>

			<image src="../../static/img/right.png" class="sdf_deert ml40 cz"></image>

		</view>

		<view class="mt10">

			<van-row gutter="10">
				<van-col span="12" v-for="(sd,idx) in 4">
				
					<navigator url="/pages/subjectTwo/examination_hall" class="s_kasdrt pd pt30 pm20 mt20 pr ov">
						<view class="sanjaio">
							<text class="cf fz32 pr">4</text>
							<image src="../../static/img/sanjaio.png"></image>
						</view>

						<image src="../../static/img/user_icon.png" class="yj user_iconser fl "></image>
						<view class="ov pl20">
							<view class="fz28 z3 ">
								陈献机
							</view>
							<view class="fz24 z9 df_dertxfcr mt5">
								软件事业部<br>
								架构师
							</view>
						</view>
						<view class="qc pm40"></view>

						<view class="dx_row_e">
							<text class="cz">客户评价</text>
							<image src="../../static/img/star.png" class="xingxing_e cz mr5" v-for="sd in 4"></image>
							<image src="../../static/img/star_k.png" class="xingxing_e cz mr5" ></image>
						</view>

						<view class="dx_row_e mt10">
							<text class="cz">平级评价</text>
							<image src="../../static/img/star.png" class="xingxing_e cz mr5" v-for="sd in 4"></image>
							<image src="../../static/img/star_k.png" class="xingxing_e cz mr5" ></image>
						</view>

						<view class="dx_row_e mt10">
							<text class="cz">下级评价</text>
							<image src="../../static/img/star.png" class="xingxing_e cz mr5" v-for="sd in 4"></image>
							<image src="../../static/img/star_k.png" class="xingxing_e cz mr5" ></image>
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
				time:"2018年10月",

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
			dateChange(evt){
				let date_e=evt.detail.value.split("-")
				this.time = date_e[0]+"年"+date_e[1]+"月";
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
	.df_df_ddrert{
		padding-left: 30upx;
		padding-right: 30upx;
	}
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
		font-size: 24upx;
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
