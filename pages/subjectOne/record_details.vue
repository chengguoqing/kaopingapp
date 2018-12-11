<template>
	<view>
		<view class="pd pt20 pm20 bgff ">
			<view class="dx_row">
				<image src="../../static/img/user_icon.png" class="user_df yj fl"></image>
				<view class="ov pl20 ln">
					<view class="fz36 mt10">
						刘峰
					</view>
					<view class="fz28 z9">
						软件事业部
					</view>
				</view>
			</view>

			<view class="mt40 box ln cen">
				<view class="box_a">
					<view class="fz46 ls">
						9分
					</view>
					<view class="fz28 z9">
						本次成绩
					</view>
				</view>

				<view class="box_a">
					<view class="fz46 ls">
						2
					</view>
					<view class="fz28 z9">
						当前排名
					</view>
				</view>

			</view>


		</view>


		<view class="bgff mt20 cen">

			<view class="box pt20 pm20">
				<view class="box_a">
					<view class="fz32 z3">
						95%
					</view>
					<view class="fz28 z9 mt10">
						击败全部门
					</view>
				</view>

				<view class="box_a">
					<view class="fz32 z3">
						8%
					</view>
					<view class="fz28 z9 mt10">
						进步率
					</view>
				</view>


				<view class="box_a">
					<view class="fz32 z3">
						80%
					</view>
					<view class="fz28 z9 mt10">
						进步率排名
					</view>
				</view>


			</view>


			<view class="box btm pt20 pm20">
				<view class="box_a">
					<view class="fz32 z3">
						95%
					</view>
					<view class="fz28 z9 mt10">
						击败全部门
					</view>
				</view>

				<view class="box_a">
					<view class="fz32 z3">
						98
					</view>
					<view class="fz28 z9 mt10">
						进步率
					</view>
				</view>


				<view class="box_a">
					<view class="fz32 z3">
						88
					</view>
					<view class="fz28 z9 mt10">
						公司平均分
					</view>
				</view>


			</view>

		</view>

		<view class="mt20 pt30 pm30 bgff pd">
			<view class="fz32 z3">
				个人能力分布状况
			</view>

			<view class="d_h_g_fer mt20 box">
				<view class="sh_dfd_dre box_a">
					<qitatubiao canvasId="f_df_dtr" :PieOption="pei_da"></qitatubiao>
				</view>
				<view class="box_a tr gfd_eeertxc pt20">
					<view class="fz28 z6 mb20">
						<text class="sd_jhg_dr cz"></text>
						<text class="sd_deertxcrt">专业能力</text>
						<text class="sd_deertxcrt ab">50%</text>
					</view>

					<view class="fz28 z6 mb20">
						<text class="sd_jhg_dr cz ab"></text>
						<text class="sd_deertxcrt">管理能力</text>
						<text class="sd_deertxcrt ab"> 10%</text>
					</view>

					<view class="fz28 z6 mb20">
						<text class="sd_jhg_dr cz ac"></text>
						<text class="sd_deertxcrt">问题能力</text>
						<text class="sd_deertxcrt ab">5%</text>
					</view>

					<view class="fz28 z6 mb20">
						<text class="sd_jhg_dr cz ad"></text>
						<text class="sd_deertxcrt">经营能力</text>
						<text class="sd_deertxcrt ab">20%</text>
					</view>

					<view class="fz28 z6 mb20">
						<text class="sd_jhg_dr cz ae"></text>
						<text class="sd_deertxcrt">文化能力</text>
						<text class="sd_deertxcrt ab">5%</text>
					</view>


				</view>

			</view>



		</view>


		<view class="mt20 pt20 pm20 bgff pd">
			<view class="fz32 z3">
				个人成绩走势
			</view>
			<view class="dsd_jh_dertx">
				<qitatubiao canvasId="f_df_dtr_er" :PieOption="pei_da_er"></qitatubiao>
			</view>

		</view>

	</view>
</template>
<script>
	import qitatubiao from "../../components/qitatubiao.vue"
	export default {
		data() {
			return {
				pei_da: {
					series: [{
						type: 'pie',
						radius: '85%',
						label: {
							normal: {
								show: false,
								position: 'center'
							},
							emphasis: {
								show: false,
							}
						},
						labelLine: {
							normal: {
								show: false
							}
						},
						data: [{
								value: 20
							},
							{
								value: 10
							},
							{
								value: 5
							},
							{
								value: 5,
							},
							{
								value: 50,
							}
						]
					}],
					seriesIndex: 0,
					dataIndex: 0,
					color: ["#D4F060", '#A3B3BE', '#FF4566', '#F5B32F', '#76B3EF']
				},
				pei_da_er: {
					xAxis: {
						type: 'category',
						boundaryGap: false,
						axisLine: {
							show: false
						},
						axisTick: {
							show: false
						},



						data: ['01', '05', '10', '15', '20', '25', '30']
					},
					yAxis: {
						type: 'value',
						show: false
					},
					grid: {
						left: '-4%',
						right: '2%',
						bottom: "0%",
						top: "1%",
						height: "100%",
						containLabel: true
					},
					series: [{
						data: [8, 9, 10, 8, 8, 9, 10],
						type: 'line',

 
					

						areaStyle: {}
					}],
					color: "#489CF3"
				}
			}
		},
		components: {
			qitatubiao
		},
		methods: {


		},
		mounted() {

		},
	}
</script>
<style scoped>
	.gfd_eeertxc{
		line-height: 1.3;
	}
	.user_df {
		width: 114upx;
		height: 114upx;
	}

	.d_h_g_fer {
		height: 330upx;
	}

	.sh_dfd_dre {
		width: 360upx;
		height: 360upx;
	}

	.sd_jhg_dr {
		width: 25upx;
		height: 25upx;
		display: inline-block;
		border-radius: 50%;
		margin-right: 10upx;
		background: #76B3EF;
	}

	.sd_jhg_dr.ab {
		background: #A3B3BE;
	}

	.sd_jhg_dr.ac {
		background: #F5B32F;
	}

	.sd_jhg_dr.ad {
		background: #D4F060;
	}

	.sd_jhg_dr.ae {
		background: #FF4566;
	}

	.sd_deertxcrt {
		display: inline-block !important;
		width: 140upx;
		text-align: left;
		overflow: hidden;
	}

	.sd_deertxcrt.ab {
		width: 80upx;
	}

	.dsd_jh_dertx {
		width: 100%;
		height: 375upx;
	}
</style>
