<template>
	<view>
		<view class="sheb_page">
			<view class="pt20 pm20 pd box">
				<view class="box_a fz32">
					成品区
				</view>
			</view>
			<view class="sd_rowsertt mb20" v-for="sd in ['A','B']">
				<view class="pt20 pm10 box bbm bgff pd">
					<view class="box_b">
						电缆线型号{{sd}}
					</view>
					<view class="box_a tr">
						<icon class="dx icon-gouhao fz50 ls cz"></icon>

					</view>
				</view>


				<view class="dx_row bgff  bgff pd pt10">
					<view class="dx_col_12">
						<view class="dx_row pt10 pm10 fz30">
							<view class="sddsff  z6">
								昨日库存
							</view>
							<view class="ov  z3">
								2件
							</view>
						</view>
						<view class="dx_row pt10 pm10 fz30">
							<view class="sddsff  z6">
								总量
							</view>
							<view class="ov  z3">
								2件
							</view>
						</view>

					</view>

					<view class="dx_col_12">
						<view class="dx_row pt10 pm10 fz30">
							<view class="sddsff  z6">
								今日产量
							</view>
							<view class="ov  z3">
								2件
							</view>
						</view>
						<view class="dx_row pt10 pm10 fz30">
							<view class="sddsff  z6">
								售出
							</view>
							<view class="ov  z3">
								2件
							</view>
						</view>

					</view>
				</view>
				<view class="btm pt10 pm10 tr fz30 bgff pd">
					应结余:1件
					<view class="f_b ml20">
						实际结余:
						<input type="number" value="1" class="dsf_ddertx f_b" /> 件
					</view>
				</view>
			</view>




			<view class=" fz32 pd pm20">
				异常汇总
			</view>
			<view class="btm pd bgff" v-for="sd in 2">

				<view class="dx_row  pt10 pm10 fz30">

					<view class="sddsff  z6">
						异常名称
					</view>
					<view class="ov  z3">
						电缆线型号B
					</view>
				</view>

				<view class="dx_row pt10 pm10 fz30">
					<view class="sddsff  z6">
						异常数量
					</view>
					<view class="ov  z3">
						2件
					</view>
				</view>


			</view>





			<view class="btm pd pt20 pm20 bgff mt20">
				<view class="fz30 z3">
					证据链
				</view>
				<view class="mt20">
					<view class="df_jhh_deert" @click="pz_dert">
						<image :src="zaop_df" v-if="zaop_df"></image>

						<icon class="dx icon-xiangji z9 cz" v-else></icon>
					</view>
				</view>
			</view>




			<view class="mt100 pm50 pd">
				<navigator url="/pages/subjectThree/goods_inventory_er" class="dx_btn ">
			
					下一步
				</navigator>
			</view>


		</view>


	</view>
</template>
<script>
	export default {
		data() {
			return {
				zaop_df: "",

			}
		},
		components: {},
		methods: {
			pz_dert() {
				let th = this
				uni.chooseImage({
					count: 1,
					success(res) {
						th.zaop_df = res.tempFilePaths
					}
				})
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	
</style>
