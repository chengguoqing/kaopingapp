<template>



	<mpvue-echarts :echarts="echarts" :onInit="pieInit" :canvasId="canvasId" />


</template>
<script>
	import * as echarts from './echarts/echarts.simple.min.js';
	import mpvueEcharts from './mpvue-echarts/src/echarts.vue';




	export default {
		props: {
			canvasId:"",
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
				let sd_dsdf=[]
				date_d.map(a=>{
					sd_dsdf.push(10)
				})
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
						data: tet_m,
						axisTick: {
							alignWithLabel: true
						}

					}],
					yAxis: [{
						type: 'value',


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
							data: sd_dsdf,
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
							data: date_d
						}
					],
					color: ["#6BB5F2"]

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
