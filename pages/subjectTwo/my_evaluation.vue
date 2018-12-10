<template>
	<div class="container">
		<view class="pd pt30 pm20 box bgff">
			<view class="box_b">
				<image src="../../static/img/user_icon.png" class="user_icon fl"></image>
				<view class="ov pl20">
					<view class="fz32 z3 mt20">
						刘峰
					</view>
					<view class="mt30 fz28 z9">
						软件事业部 <text class="ml10">经理</text>
					</view>
				</view>
				<view class="qc pm30"></view>
				<view class="dx_row_e">
					<text class="cz">客户评价</text>
					<image src="../../static/img/star.png" class="xingxing_e cz mr10" v-for="sd in 5"></image>
				</view>

				<view class="dx_row_e">
					<text class="cz">平级评价</text>
					<image src="../../static/img/star.png" class="xingxing_e cz mr10" v-for="sd in 5"></image>
				</view>

				<view class="dx_row_e ">
					<text class="cz">下级评价</text>
					<image src="../../static/img/star.png" class="xingxing_e cz mr10" v-for="sd in 5"></image>
				</view>
			</view>
			<view class="box_a">
				<view class="df_jh_deertert ">
					<mpvue-echarts :echarts="echarts" :onInit="huanxing" canvasId="pie_er" />
				</view>
			</view>
		</view>


		<view class="canvasView">
			<view class="pd dsfd_dderty fz30">客户评价</view>
			<view class="df_jh_deert bgff">
				<mpvue-echarts :echarts="echarts" :onInit="pieInit" canvasId="pie" />
			</view>

			<view class="pd dsfd_dderty fz30">平级评价</view>
			<view class="df_jh_deert bgff">
				<mpvue-echarts :echarts="echarts" :onInit="pieInit" canvasId="pieon" />
			</view>


			<view class="pd dsfd_dderty fz30">下级评价</view>
			<view class="df_jh_deert bgff">
				<mpvue-echarts :echarts="echarts" :onInit="pieInit" canvasId="pieer" />
			</view>

		</view>

	</div>
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
			textStyle: {
				fontSize: 18,
				color: '#666'
			},
			grid: {
				left: '3%',
				right: '4%',
				bottom: "3%",
				height: "100%",
				containLabel: true
			},
			xAxis: [{
				type: 'value',
				maxInterval: 5,
				axisLine: {
					lineStyle: {
						
						color: "#ededed"
					}
				},
				splitLine: {
					lineStyle: {
						color: "#ededed"
					}
				}

			}],
			yAxis: [{
				type: 'category',
				data: ['讲解清晰明了', '咨询态度好', '平易近人', '耐心', '其他'],

				axisLine: {
					lineStyle: {
						color: "#ededed"
					}
				},
				axisTick: {
					alignWithLabel: true
				}
			}],
			series: [{
				name: '直接访问',
				type: 'bar',
				barWidth: '45%',
				data: [5, 45, 40, 25, 40]
			}],
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
						show: true,
						color: "#333",
						fontSize: '26',
						position: 'center'
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
		methods: {

		},
		components: {
			mpvueEcharts
		}
	}
</script>

<style scoped>
	.df_jh_deert {
		padding-top: 30upx;
		padding-bottom: 10upx;
		height: 360upx;
	}

	.xingxing_e {
		width: 30upx;
		height: 30upx;
	}

	.dx_row_e {
		margin-top: 15upx;
		font-size: 30upx;
	}

	.dx_row_e text {
		margin-right: 20upx;
	}

	.df_jh_deertert {
		width: 200upx;
		float: right;
		height: 200upx;
	}
	.dsfd_dderty{
		line-height: 90upx;
		background: #EFEFEF;
	}
</style>
