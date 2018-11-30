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
				let sd_dsdf = [],
					th=this
				date_d.map(a => {
					sd_dsdf.push(10)
				})
				return {
					series: [{
						type: 'pie',
					
						radius: ['70%', '90%'],
						avoidLabelOverlap: false,
						label: {
							normal: {
								show: false,
								position: 'center'
							},
							emphasis: {
								show: true,
								textStyle: {
									fontSize: '30',
									fontWeight: 'bold'
								}
							}
						},
						labelLine: {
							normal: {
								show: false
							}
						},
						data: [{
								value: 143.26,
								name: '143.26'
							},
							{
								value: 70.23,
								name: '702.26'
							},
							{
								value: 120.23,
								name: '120.23'
							},
							{
								value: 90.23,
								name: '90.23'
							}
						]
					}], 
				seriesIndex: 0,
				dataIndex: 0,
					
					
					color:["#EA478E",'#47C3EE','#54ABF3','#FB9B69']

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
