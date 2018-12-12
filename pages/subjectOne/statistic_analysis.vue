<!-- 统计分析 -->
<template>
	<view class=" pm100">
		<view class="bgff pm20">


			<tab_qh :sd_dfg="sd_dfg"></tab_qh>
			<view class="dsf_jh_deeretxcrf ">

				<view class="box pd mt20">
					<view class="box_a pr20">
						<view class="pr dsf_jh_ddrtxf br ab">
							<text class="z6 fz26 ml20 cz">软件事业部</text>
							<icon class="dx icon-down cz"></icon>
						</view>
					</view>
					<view class="box_a pl20">
						<view class="pr dsf_jh_ddrtxf br " @click="is_riqi=true">
							<text class="z6 fz26 ml20 cz">{{kaishi}}</text>
							<icon class="dx icon-down cz"></icon>
						</view>
					</view>


				</view>

			</view>
		</view>

		<view class="bgff mt20">

			<view class="sd_jh_listd" v-for="(sd,idx) in ze_sdf">
				<view class="dsf_kh_df_drer pd pr fz32 bbm" @click="serfdr(sd)">
					{{sd.name}}
					<icon class="dx icon-down diwn_ddfer" :class="sd.cls"></icon>
				</view>

				<view class="dx_row dsf_jh_dffrx pd  pm20" v-if="sd.cls">
					<view class="dx_col_12" v-for="SD in 4">
						<view class="bk yj4 pd pt20 pm20 pr fz26 bgff fdg_kj_dert z6">
							<view class="red fz30 dsf_drrtxrtt">
								￥
								<text class="fz60">50</text>
							</view>
							金额: <br>
							事由：迟到 <br>
							时间：2018-11-8
						</view>
					</view>
				</view>

			</view>



		</view>



		<view class="box sd_deert">
			<view class="box_a df_kse fz32" :class="sd.cls" v-for="sd in  sd_sdf" @click="xzdfd(sd)">
				{{sd.name}}
			</view>

		</view>
	<view class="df_rili_deeret" v-if="is_riqi">
			<xuzriqi @huitiao="huitiao"></xuzriqi>
		</view>

	</view>
</template>
<script>
	import tab_qh from "@/components/tab_qh.vue"
	import xuzriqi from "@/components/xuzriqi.vue"
	export default {
		data() {
			return {
				kaishi: "2018-11-4 2018-11-6",
				is_riqi:false,
				sd_sdf: [{
						cls: "",
						href: "/pages/subjectOne/send_bill_me",
						name: "开给我的"
					}, {
						cls: "",
						href: "/pages/subjectOne/leave_the",

						name: "我开出的"
					},
					{
						cls: "act",
						href: "",

						name: "统计分析"
					}
				],
				sd_dfg: [{
					name: "罚",
					cls: "act"
				}, {
					name: "奖",
					cls: ""
				}],
				ze_sdf: [{
					name: "陈献机",
					cls: ""
				}, {
					name: "管玉华",
					cls: "act"
				}, {
					name: "许润龙",
					cls: ""
				}, ]
			}
		},
		components: {
			tab_qh,
			xuzriqi
		},
		methods: {
			huitiao(e){
				this.is_riqi=false
				this.kaishi=e
			},
			serfdr(sd) {
				if (sd.cls) {
					sd.cls = ""
				} else {
					sd.cls = "act"
				}
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
	.dsf_jh_deeretxcrf {
		padding-top: 110upx;
	}

	.dsf_jh_ddrtxf {
		border-radius: 20px;
		width: 402upx;
		line-height: 50upx;
		height: 60upx;
	}

	.dsf_jh_ddrtxf .dx {
		position: absolute;
		right: 20upx;
	}

	.dsf_jh_ddrtxf.ab {
		width: 260upx;
		float: right;
	}

	.dsf_jh_deeretxcrf {
		padding-top: 110upx;
	}

	.sd_quyg_ert {
		width: 370upx;
		height: 370upx;
		border: 20upx solid #E9F6FF;
		border-radius: 50%;
		position: relative;
		margin: auto;
		margin-top: 50upx;
	}

	.sd_hjinduer {
		position: absolute;
		left: 0px;
		bottom: 0px;
		width: 100%;
		height: 132upx;
	}

	.dsf_kh_df_drer {
		line-height: 90upx;

	}

	.diwn_ddfer {
		position: absolute;
		right: 20upx;
		top: 0;
	}

	.dsf_jh_dffrx {
		background: #FFFDFA;
	}

	.fdg_kj_dert {
		line-height: 2;

	}

	.dsf_jh_dffrx {
		margin-left: -10upx;
		margin-right: -10upx;
	}

	.dsf_jh_dffrx .dx_col_12 {
		padding-left: 10upx;
		padding-right: 10upx;
		margin-top: 20upx;
	}

	.dsf_drrtxrtt {
		color: #f96162;
		position: absolute;
		right: 20upx;
		top: 0upx;
	}

	.diwn_ddfer.act {
		transform: rotate(180deg);
	}
</style>
