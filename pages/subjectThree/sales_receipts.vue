<!-- 销售凭证 -->
<template>
	<view class="pt20">
		<view class="pd bgff">
			<view class="pt30 pm20 fz32 z3">
				基本信息
			</view>
			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					收入类型
				</view>
				<view class="ov z3 fz28 ">
					对外经营收入
				</view>
			</view>

			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					姓名
				</view>
				<view class="ov z3 fz28">
					豆豆
				</view>
			</view>

			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					手机号码
				</view>
				<view class="ov z3 fz28">
					15296584565
				</view>
			</view>


			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					经手人
				</view>
				<view class="ov z3 fz28">
					豆豆
				</view>
			</view>



			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					所属合名
				</view>
				<view class="ov z3 fz28">
					豆豆
				</view>
			</view>



			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					购买人
				</view>
				<view class="ov z3 fz28">
					豆豆
				</view>
			</view>


			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					购买人电话
				</view>
				<view class="ov z3 fz28">
					15296584565
				</view>
			</view>





		</view>


		<view class="pd bgff mt20" v-for="(sd,idx) in sd_kh_df">
			<view class="pt20 pm20 fz32 z3">
				销售清单{{idx+1}}
			</view>
			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					商品名称
				</view>
				<view class="ov z3 fz28">
					电缆线材料
				</view>
			</view>

			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					购买方
				</view>
				<view class="ov z3 fz28">
					杨XX
				</view>
			</view>

			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					联系方式
				</view>
				<view class="ov z3 fz28">
					152xxxx6543
				</view>
			</view>


			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					商品单价
				</view>
				<view class="ov z3 fz28 pl10">
					<input type="number" value="100" class="dsf_ddertx ab f_b cz">
				</view>
			</view>

			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					数量
				</view>
				<view class="ov z3 fz28 pl10">
					<input type="number" value="2" class="dsf_ddertx f_b cz"> 件
				</view>
			</view>


			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					销售地点
				</view>
				<view class="ov z3 fz28">
					广东省广州
				</view>
			</view>


			<view class="dx_row dfsd_ddererrtt fz30">
				<view class="sddsff  z6">
					总价格
				</view>
				<view class="ov z3 fz28">
					200元
				</view>
			</view>



		</view>


		<view class="cen pt10 pm10 bgff ls fz32 mt20" @click="sd_kh_df++">
			<text class="fz50">+</text> 添加商品
		</view>



		<view class="btm pd pt20 pm20 bgff mt20">
			<view class="fz30 z3">
				证据链 <text class="fz26 z9">(请上传发票及数据等相关相片)</text>
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


		<view class="mt20 pt20 pm20 pd bgff fz30 tr">
			销售商品 2件 销售总额：￥300.00
		</view>

		<view class="mt20 bgff">
			<view class="pt20 pm20 pd bbm fz32">
				反腐审计异常
			</view>

			<view class="pt20 pm20 pd bbm box fz30">
				<view class="box_b">
					反腐金额
				</view>
				<view class="box_a tr fz30">
					100.00
				</view>
			</view>
			
			<view class="pt20 pm20 pd bbm ln fz30">
				反腐备注
				<view class="z6 fz26">
					销售材料时低价高卖，赚钱回扣
				</view>
			</view>
			
			


		</view>


<view class=" pd pt20 pm20 bgff ">
			<view class="fz30 z3">
			反腐证据
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
</template>
<script>
	export default {
		data() {
			return {
				sd_kh_df:1
			}
		},
		components: {},
		methods: {},
		mounted() {},
	}
</script>
<style scoped>
	.dsf_ddertx.ab {
		width: 180upx;
	}
	.dfsd_ddererrtt{
		line-height: 70upx;
	}
</style>
