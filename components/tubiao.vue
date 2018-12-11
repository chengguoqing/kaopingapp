<template>



	<mpvue-echarts :echarts="echarts" :onInit="pieInit" :canvasId="canvasId" />


</template>
<script>
	import * as echarts from './echarts/echarts.simple.min.js';
	import mpvueEcharts from './mpvue-echarts/src/echarts.vue';




	export default {
		props: {
			canvasId: "",
			date_d: "",
			tet_m: ""
		},
		data() {
			return {
				echarts,
				pieInit: '',
			}
		},
		components: {
			mpvueEcharts
		},
		methods: {
			getPieOption(date_d, tet_m) {
				let sd_dsdf = []
				date_d.map(a => {
					sd_dsdf.push(10)
				})
				return {



					tooltip: {
						trigger: 'axis',
						axisPointer: { // 坐标轴指示器，坐标轴触发有效
							type: 'shadow' // 默认为直线，可选为：'line' | 'shadow'
						}
					},
					textStyle: { //设置字体颜色
						fontSize: 12,
						color: '#666'
					},
					grid: {
						left: '3%',
						right: '4%',
						bottom: "3%",
						height: "90%",
						containLabel: true
					},
					xAxis: [{
						type: 'category',
						data: tet_m,
						axisTick: {
							alignWithLabel: true
						},
						

						axisLine: { //最外面的边框颜色
							lineStyle: {
								
								color: "#ededed"
							}
						},
						splitLine: { //间隔线
							lineStyle: {
								color: "#ededed" //间隔线的颜色
							}
						}

					}],
					yAxis: [{
						type: 'value',
						show: false, 
						axisLine: { //最外面的边框颜色
							lineStyle: {
								color: "#ededed"
							}
						},
						splitLine: { //间隔线
							lineStyle: {
								color: "#ededed" //间隔线的颜色
							}
						}


					}],
					series: [

						{ // For shadow
							type: 'bar',
							itemStyle: {
								normal: {
									color: 'rgba(0,0,0,0.0)'
								}
							},
							barGap: '-100%',
							barWidth: '45%',
							barCategoryGap: '40%',
							data: sd_dsdf,
							animation: false
						},
						{
							type: 'bar',
							barWidth: '45%',
							
							label: {
								normal: {
									show: true,
									 position: ['45%',-15]
								}
							},
							data: date_d
						}
					],
					color: ["#449EF4"]

				}
			}

		},
		mounted() {
			let th = this
			this.pieInit = function(canvas, width, height) {
				let pieChart = echarts.init(canvas, null, {
					width: width,
					height: height
				})
				canvas.setChart(pieChart)

				pieChart.setOption(th.getPieOption(th.date_d, th.tet_m))
				return pieChart
			}
		},
	}
</script>
<style scoped>
	.dsf_dfdfrs {
		padding-top: 20upx;
		height: 440upx;
		padding-bottom: 20upx;

	}
</style>
