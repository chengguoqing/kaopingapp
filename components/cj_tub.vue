<!-- 抽检图表 -->
<template>
	<view class=" pt20 ">
		<view class="pd">
			
		
		<view class="fz28 z3">
			软件事业部
		</view>
		<view class="box">
			<view class="box_a">
				<view class="sd_jh_dertxcrt">
					<qitatubiao :canvasId="'f_df_dtr_e'+id_id" :PieOption="pei_da"></qitatubiao>
				</view>
			</view>
			<view class="box_a tr gfd_eeertxc ">
							<view class="fz28 z6 mb10">
								<text class="sd_jhg_dr cz"></text>
								<text class="sd_deertxcrt cz">正常</text>
							</view>
		
							<view class="fz28 z6 mb10">
								<text class="sd_jhg_dr cz ab"></text>
								<text class="sd_deertxcrt cz">迟到</text>
							</view>
		
							<view class="fz28 z6 mb10">
								<text class="sd_jhg_dr cz ac"></text>
								<text class="sd_deertxcrt cz">早退</text>
							</view>
		
							<view class="fz28 z6 mb10">
								<text class="sd_jhg_dr cz ad"></text>
								<text class="sd_deertxcrt cz">旷工</text>
							</view>
		
						
		
		
						</view>
						
						
		</view>
		
		<view class="box ln cen mt10">
			<view class="box_a">
				<view class="fz26 z6">
					正常率
				</view>
				<view class="fz32">
					80%
				</view>
			</view>
			
			<view class="box_a">
				<view class="fz26 z6">
					抽查通过率
				</view>
				<view class="fz32">
					80%
				</view>
			</view>
		</view>
		</view>
		<view class="mt20 btm dx_row cen fz26 z6">
			<view class="dx_col_12  pt10 pm10 brm">
				正常（2）
			</view>
			<view class="dx_col_12  pt10 pm10 ">
				请假（0）
			</view>
		</view>
		
		<view class=" btm dx_row cen fz26 z6 sdfs_df_eert">
			<view class="dx_col_12  pt10 pm10 ">
				已处理
			</view>
			<view class="dx_col_12  pt10 pm10 ab">
				异常打卡
			</view>
		</view>
		
		

	</view>
</template>
<script>
	import qitatubiao from "./qitatubiao.vue"

	export default {
		props:{
			id_id:""
		},
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
					color: ["#5DBAF9", '#F2D6AF', '#F7C0B7',  '#A6E8E2']
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
	.sd_jh_dertxcrt {
		width: 180upx;
		height: 180upx;
		margin-top: 20upx;
	}
	
	
	
	.sd_jhg_dr {
			width: 18upx;
			height: 18upx;
			display: inline-block;
			margin-right: 10upx;
			background: #76B3EF;
		}
	
		.sd_jhg_dr.ab {
			background: #A6E8E2;
		}
	
		.sd_jhg_dr.ac {
			background: #F2D6AF;
		}
	
		.sd_jhg_dr.ad {
			background: #F7C0B7;
		}
	
		.sd_deertxcrt {
			display: inline-block !important;
			
			text-align: left;
			overflow: hidden;
		}
	
	
	
		.dsd_jh_dertx {
			width: 100%;
			height: 375upx;
		}
		.sdfs_df_eert view{
			background: #9E9E9F;
			color: #fff;
		}
		.sdfs_df_eert view.ab{
			background: #E50011;
		}
		
</style>
