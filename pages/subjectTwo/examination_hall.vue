<template>
	<view>
		<view class="bgff">
			<view class="pt20 pm20 fz32 z3 cen">
				当前在10月份的复盘阶段
			</view>

			<view class="pd pt20 pm20 box bgff btm">
				<view class="box_b pt40">
					<image src="../../static/img/user_icon.png" class="user_icon fl"></image>
					<view class="ov pl20">
						<view class="fz32 z3 ">
							刘峰
						</view>
						<view class="mt20 ln fz26 z9">
							软件事业部 <br> <text class="">经理</text>
						</view>
					</view>
					<view class="qc pm20"></view>
				</view>
				<view class="box_a">
					<view class="df_jh_deertert pr">
						<mpvue-echarts :echarts="echarts" :onInit="huanxing" canvasId="pie_er" />
						<view class="z9 dsf_jjh_eer">
							<text class="fz50 z3 b">80</text>分
							<view class="fz22 ">
								当前已进行<br>
								<text class="ye">1:05:30:20</text>
							</view>
						</view>
					</view>
				</view>
			</view>

			<view class="dsf_dfdfrs ">
				<mpvue-echarts :echarts="echarts" :onInit="pieInit" canvasId="pieon" />
			</view>


		</view>

<view class="pd pt20">
	<view class="bgff yj4 pd pt20 pm20">
		<view class="fz32 z3">
			我的评论
		</view>
		<view class="dx_row mt20" v-for="sd in 3">
			<image src="../../static/img/user_icon.png" class="yj user_dertx fl" ></image>
			<view class="ov pl20 fz30 z6">
				目标不系统扣1分
			</view>
		</view>
	</view>
</view>

<view class="pd sdf_dfrtd mt40">
	<view class="dx_row  yj4 ov bgff">
		
		<view class="bjhg_sddf fr">
			评论
		</view>
		<view class="ov df_dertxfcrdr pd">
			<input type="text"  placeholder ="我来说几句"  />
		</view>
	</view>
</view>

	</view>
</template>
<script>
	import * as echarts from '../../components/echarts/echarts.simple.min.js';
	import mpvueEcharts from '../../components/mpvue-echarts/src/echarts.vue';

	function getPieOption() {
		return {
			tooltip: {
				trigger: 'axis',
				axisPointer: { // 坐标轴指示器，坐标轴触发有效
					type: 'shadow' // 默认为直线，可选为：'line' | 'shadow'
				}
			},
			grid: {
				left: '3%',
				right: '4%',
				bottom: "3%",
				height: "100%",

				containLabel: true
			},
			xAxis: [{
				type: 'category',
				data: ['王欢', '李峻秀', '张也', '张世杰'],
				axisTick: {
					alignWithLabel: true
				}

			}],
			yAxis: [{
				type: 'value'

			}],
			series: [

				{ // For shadow
					type: 'bar',
					itemStyle: {
						normal: {
							color: 'rgba(0,0,0,0.05)'
						}
					},
					barGap: '-100%',
					barWidth: '50%',
					barCategoryGap: '40%',
					data: [100, 100, 100, 100],
					animation: false
				},
				{
					type: 'bar',
					barWidth: '50%',

					label: {
						normal: {
							show: true,
						}
					},
					data: [70, 60, 55, 50]
				}
			],
			color: ["#6BB5F2"]

		}
	}

	function getPieOption_er() {
		return {
			series: [{
				type: 'pie',
				radius: ['80%', '90%'],
				avoidLabelOverlap: true,
				label: {
					normal: {
						show: false,
					}
				},
				labelLine: {
					normal: {
						show: false
					}
				},
				data: [{
						value: 0.7,
					},
					{
						value: 4.3,
						name: '4.3'
					}
				],
				color: ["#E2F2FF", "#499DF2"]
			}]
		}
	}
	export default {
		data() {
			return {
				echarts,
				pieInit: function(canvas, width, height) {
					let pieChart = echarts.init(canvas, null, {
						width: width,
						height: height
					})
					canvas.setChart(pieChart)

					pieChart.setOption(getPieOption())
					return pieChart
				},

				huanxing: function(canvas, width, height) {
					let pieChart = echarts.init(canvas, null, {
						width: width,
						height: height
					})
					canvas.setChart(pieChart)

					pieChart.setOption(getPieOption_er())
					return pieChart
				},
			}
		},
		components: {
			mpvueEcharts
		},
		methods: {},
		mounted() {

		},
	}
</script>
<style scoped>
	.df_jh_deertert {
		width: 220upx;
		float: right;
		height: 220upx;
	}

	.dsf_jjh_eer {
		position: absolute;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
		text-align: center;
		padding-top: 40upx;
	}

	.dsf_dfdfrs {
		padding-top: 20upx;
		height: 440upx;
		padding-bottom: 20upx;

	}
	.user_dertx{
		width: 50upx;
		height: 50upx;
	}
	


	
</style>
