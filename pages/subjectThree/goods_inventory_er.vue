<template>
	<view>

		<view class="pd pt40 bgff">
			<view class="yj4 dsf_hg_der dx_row ov">
				<view class="dx_col_12 df_sd_dert act">
					成品
				</view>
				<view class="dx_col_12 df_sd_dert">
					原材料
				</view>

			</view>

			<view class="box cen mt20 pm20">
				<view class="box_a z9 fz30">
					合名称: <text class="z3">电缆合</text>
				</view>

				<view class="box_a z9 fz30">
					负责人: <text class="z3">杨桂平</text>
				</view>
			</view>

		</view>


		<view class="mt20">
			<tab_qh :sd_dfg="sd_dfg" is_sdf="1"></tab_qh>
		</view>

		<view class="sd_page">


			<view class="bgff">
				<view class="pt20 pm10 box btm bgff pd">
					<view class="box_b">
						电缆线型号A
					</view>
					<view class="box_a tr">
						<icon class="dx icon-gouhao fz50 ls cz"></icon>
					</view>
				</view>
				<view class="pt20 pm20 box btm bgff pd">
					<view class="box_a">
						应结余 1件
					</view>
					<view class="box_a tr cen">
						实际结余 1件
					</view>
				</view>
				<view class="pt20 pm20 box btm bgff pd">
					<view class="box_a">
						直检结余 	 <input type="number" value="1" class="dsf_ddertx f_b" v-if="!is_dfg"/>
						 <text v-else>1</text> 件
					</view>
				</view>

				<view class="pt20 pm10 box btm bgff pd">
					<view class="box_b">
						电缆线型号B
					</view>
					<view class="box_a tr">
						<icon class="dx icon-close fz46 red cz"></icon>
					</view>
				</view>
				<view class="pt20 pm20 box btm bgff pd">
					<view class="box_a">
						应结余 1件
					</view>
					<view class="box_a tr cen">
						实际结余 1件
					</view>
				</view>
				<view class="pt20 pm20 box btm bgff pd">
					<view class="box_a">
						直检结余
						 <input type="number" value="1" class="dsf_ddertx f_b" v-if="!is_dfg"/>
						 <text v-else>1</text>
						 件
					</view>

				</view>
			</view>

			<view class="btm pd pt20 pm20 bgff mt20">
				<view class="fz30 z3">
					证据链
				</view>
				<view class="mt20">
					<view class="df_jhh_deert fl mr20">
						<image src="../../static/img/bg_sdf.jpg"></image>

					</view>

					<view class="df_jhh_deert fl mr20">
						<image src="../../static/img/bg_sdf.jpg"></image>

					</view>

					<view class="qc"></view>
				</view>
			</view>


		</view>

		<view class="mt20 bgff">


			<view class="pd pt20 pm20 fz32">
				检查
			</view>
			
			<view class="pt20 pm20 btm pd dx_row">
				<view class="dx_col_6">
					质检人
				</view>
				<view class="dx_col_6">
					任老师
				</view>
				<view class="dx_col_6">
					质检结果
				</view>
				<view class="dx_col_6 red">
					异常
				</view>
				
				
			</view>
			
			<view class="pt20 pm20 btm pd dx_row">
				<view class="dx_col_6">
					盘点负责人
				</view>
				<view class="dx_col_6">
					杨贵人
				</view>
				<view class="dx_col_6">
					触发金额
				</view>
				<view class="dx_col_6 red">
					￥200.00
				</view>
				
				
			</view>
			
			
			<view class="mt100 pm50 pd">
				<view class="dx_btn" :class="is_dfg?'act':''" @click="is_dfg=true">
					{{is_dfg?'已质检':'质检完成' }}
				</view>
			</view>
			
			
			
		</view>


	</view>
</template>
<script>
	import tab_qh from "@/components/tab_qh.vue"
	export default {
		data() {
			return {
				is_dfg:false,
				sd_dfg: [{
					cls: "act",
					name: "成品区"
				}, {
					cls: "",
					name: "残次品区"
				}, {
					cls: "",
					name: "废品区"
				}]
			}
		},
		components: {
			tab_qh
		},
		methods: {},
		mounted() {},
	}
</script>
<style scoped>
	.dx_btn.act{
		background: #CCCCCC;
	}
</style>
