<template>
	<view>
		<tab_qh :sd_dfg="sd_dfg"></tab_qh>

		<view class="sdf_jh_der pd">

			<view class="yj4 bgff mt20" v-for="(sd,idx) in 10">
				<view class="pd dx_row pt20 pm20">
					<view class="dx_col_20 fz26 z6">
						订单编号: <text>20181009623245896</text>
					</view>
					<view class="dx_col_4 ls fz26 ">
						交易成功
					</view>
				</view>

				<view class="dx_row pd pt20 pm20 btm" v-for="sd in 2">
					<image src="https://duxinggj-2018-1251133427.cos.ap-guangzhou.myqcloud.com/upload_ef46110abaeaa912e2d1d2f0cd0dd641.jpg"
					 class="femh_dert fl"></image>
					<view class="ov pl20 box">
						<view class="box_b fz30 ln z6">
							<text class="z3">电缆线原材料</text><br>
							<text>商品编号:sp1001</text><br>
							<text>规格:50*40</text>
						</view>
						<view class="box_b fz30 ln z6 tr">
							<text>￥60.00</text><br>
							<text>x1</text>
						</view>
					</view>
				</view>

				<view class="btm pt20 pd tr fz28">
					共2件商品 <text class="ml10">合计:</text> <text class="fz32">300.00</text>
					<view class="mt10 pm20 ">
						<view class="sd_hhg_der">
							再来一单
						</view>
						<view class="sd_hhg_der ab ml10">
							索赔索酬
						</view>
					</view>
				</view>




			</view>


		</view>

	</view>
</template>
<script>
	import tab_qh from "@/components/tab_qh"
	export default {
		data() {
			return {
				sd_dfg: [{
					name: "全部",
					cls: "act"
				}, {
					name: "待收款",
					cls: ""
				}, {
					name: "待付款",
					cls: ""
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
	.sdf_jh_der {
		padding-top: 100upx;
	}

	.femh_dert {
		width: 125upx;
		height: 125upx;
	}

	.sd_hhg_der {
		width: 175upx;
		height: 51upx;
		text-align: center;
		line-height: 51upx;
		border-radius: 30upx;
		border: 1px solid #B3B3B3;
		color: #B3B3B3;
		font-size: 30upx;
		display: inline-block;
	}
	.sd_hhg_der.ab{
		border: 1px solid #489FF7;
		color: #489FF7;
	}
</style>
