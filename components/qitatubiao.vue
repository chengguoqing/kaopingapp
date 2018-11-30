<template>

	<mpvue-echarts :echarts="echarts" :onInit="pieInit" :canvasId="canvasId" />

</template>
<script>
	import * as echarts from './echarts/echarts.simple.min.js';
	import mpvueEcharts from './mpvue-echarts/src/echarts.vue';
	export default {
		props: {
			canvasId: '',
			PieOption:""
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

		},
		onLoad: function() {
			let th = this
			this.pieInit = function(canvas, width, height) {
				let pieChart = echarts.init(canvas, null, {
					width: width,
					height: height
				})
				canvas.setChart(pieChart)

				pieChart.setOption(th.PieOption)
				return pieChart
			}
		}
	}
</script>
<style scoped></style>
