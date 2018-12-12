<template>
	<view class="pd bgff">
		<view class="pt20 pm20 fz32 touy_dert pr pl20">
			<text class="bian_kside"></text>
			<picker class="picker-item" mode="selector" :range="textList" >

			海口分公司
			<text class="fz26 z3 ml20">按下级部门</text>
			<icon class="dx icon-down"></icon>
			</picker>
		</view>

		<view class="dx_row dsf_roww_er">
			<view class="dx_col_12 g_jhj_deerddf " v-for="(sd,idx) in 2">
				<view class="br yj4 ov">
					<cj_tub :id_id="idx"></cj_tub>
				</view>
			
			</view>
		</view>
		
		
		
		<view class="pt20 pm20 fz32 touy_dert pr pl20 mt20">
					<text class="bian_kside"></text>
					南京分公司
					<text class="fz26 z3 ml20">按下级部门</text>
					<icon class="dx icon-down"></icon>
				</view>
		
				<view class="dx_row dsf_roww_er">
					<view class="dx_col_12 g_jhj_deerddf " v-for="(sd,idx) in 2">
						<view class="br yj4 ov">
							<cj_tub :id_id="idx+'g'"></cj_tub>
						</view>
					
					</view>
				</view>
				
				


	</view> 
</template>
<script>
	import cj_tub from "../../../components/cj_tub.vue"

	export default {
		data() {
			return {
					textList: [
					'text1',
					'text2',
					'text3'
				],
			}
		},
		components: {
			cj_tub
		},
		methods: {},
		mounted() {},
	}
</script>
<style scoped>
	.touy_dert {
		line-height: 1;
	}

	.bian_kside {
		position: absolute;
		left: 0;
		top: 38upx;
		height: 30upx;
		width: 4upx;
		background: #489FF6;
	}
	
	.dsf_roww_er{
		margin-left: -10upx;
		margin-right: -10upx;
	}
	.g_jhj_deerddf{
		padding-left: 10upx;
		padding-right: 10upx;
		margin-top: 20upx;
	}
</style>
