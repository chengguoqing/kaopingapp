<template>
	<view class=" pm100">
		<view class="bgff pm20">


			<view class="box cen dsf_ddrertxc bbm">
				<navigator url="/pages/subjectOne/statistical_analysis_fa" class="box_a df_fd_sdrert ">
					<text class="pd fz32 z6">罚</text>
				</navigator>

				<navigator url="/pages/subjectOne/statistical_analysis_jiang" class="box_a df_fd_sdrert act">
					<text class="pd fz32 z6">奖</text>
				</navigator>


			</view>




			<!-- 	<tab_qh :sd_dfg="sd_dfg"></tab_qh> -->

			<view class="dsf_jh_deeretxcrf ">

				<view class="box pd mt20">
					<view class="box_a pr20">
						<view class="pr dsf_jh_ddrtxf br ab">
							<picker class="picker-item" mode="selector" :range="textList">
								<text class="z6 fz26 ml20 cz">软件事业部</text>
								<icon class="dx icon-down cz"></icon>
							</picker>
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


			<view class="fz32 z3 cen mt60">
				罚单金额统计
			</view>

			<view class="wdd_jh_deret mt40">
				<qitatubiao canvasId="sd_sd_a" :PieOption="PieOption"></qitatubiao>
			</view>


		</view>

		<view class="pt20 mt20 bgff pm50">
			<view class="fz32 z3 cen ">

				人员占比
			</view>
			<view class="wdd_jh_deret mt40">

				<qitatubiao canvasId="sd_sd_b" :PieOption="PieOption_b"></qitatubiao>
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
	import qitatubiao from "@/components/qitatubiao.vue"
	import xuzriqi from "@/components/xuzriqi.vue"

	export default {
		data() {
			return {
				textList: [
					'text1',
					'text2',
					'text3'
				],
				kaishi: "2018-11-4 2018-11-6",
				is_riqi: false,
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
				PieOption: "",
				PieOption_b: ""
			}
		},
		components: {
			tab_qh,
			qitatubiao,
			xuzriqi
		},
		methods: {
			huitiao(e) {
				this.is_riqi = false
				this.kaishi = e
			}
		},
		mounted() {

			this.PieOption = {
				xAxis: {
					type: 'category',
					boundaryGap: false,


					data: ['迟到', '早退', '上班瞌睡', '3S问题'],
					axisLine: { //最外面的边框颜色
						lineStyle: {
							color: "#666"
						}
					},
				},
				grid: {
					left: '3%',
					right: '4%',
					width: "90%",
					bottom: "3%",
					height: "100%",
					containLabel: true
				},

				yAxis: {
					type: 'value',
					show: false, //去掉背景线
				},
				series: [{
					data: [120, 200, 150, 80],
					type: 'bar'
				}],
				barWidth: "30%",
				color: ["#489EF5"]
			};








			this.PieOption_b = {
				title: {
					text: '某站点用户访问来源',
					subtext: '纯属虚构',
					x: 'center'
				},
				legend: {
					orient: 'vertical',
					left: 'left',
					data: ['覃正', '许润龙', '管玉华']
				},


				series: [{
					name: '访问来源',
					type: 'pie',
					radius: '90%',
					data: [{
							value: 20,
							name: '覃正'
						},
						{
							value: 10,
							name: '许润龙'
						},
						{
							value: 70,
							name: '管玉华'
						},
					],
					itemStyle: {
						normal: {
							borderWidth: 2,
							borderColor: '#fff'
						}
					},
				}],
				color: ["#68ADF1", '#A2CDF7', '#489EF5'],

			};

		},
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

	.wdd_jh_deret {
		width: 540upx;
		height: 250upx;
		margin: auto;
	}

	.wdd_jh_deret.ab {
		width: 350upx;
		height: 350upx;
	}


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

	.df_fd_sdrert.act text {
		padding-bottom: 26upx;
		color: #459FF7;
		border-bottom: 1px solid #459FF7;
	}
</style>
