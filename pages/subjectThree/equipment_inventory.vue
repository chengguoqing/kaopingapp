<template>
	<view>

		<view class="sheb_page">
			<view class="pt20 pm20 pd box">
				<view class="box_a fz32">
					扳手
				</view>
				<view class="box_a tr">
					<icon class="dx icon-close fz45 red "></icon>
					<icon class="dx icon-gouhao fz50 ls ml10"></icon>
				</view>
			</view>

			<view class="pd bgff">
				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						昨日库存
					</view>
					<view class="ov  z3">
						2
					</view>
				</view>
				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						今日库存
					</view>
					<view class="ov  z3">
						2
					</view>
				</view>

				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						异常类型
					</view>
					<view class="ov  z3">
						<radio-group class="radio-group">
							<label class="radio" v-for="item in items">
								{{item.value}}
								<radio :value="item.name" :checked="item.checked" class="sd_dreertxc" />

							</label>
						</radio-group>
					</view>
				</view>


				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						扣除合币
					</view>
					<view class="ov  z3">
						100元
					</view>
				</view>

				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						总扣合币
					</view>
					<view class="ov  z3">
						100元
					</view>
				</view>

				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						负责人
					</view>
					<view class="ov  z3">
						王宝志
					</view>
				</view>



			</view>

		</view>



		<view class="sheb_page">
			<view class="pt20 pm20 pd box">
				<view class="box_a fz32">
					羊角锤
				</view>
				<view class="box_a tr">
					<icon class="dx icon-close fz45 red "></icon>
					<icon class="dx icon-gouhao fz50 ls ml10"></icon>
				</view>
			</view>

			<view class="pd bgff">
				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						昨日库存
					</view>
					<view class="ov  z3">
						2
					</view>
				</view>
				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						今日库存
					</view>
					<view class="ov  z3">
						2
					</view>
				</view>

				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						异常类型
					</view>
					<view class="ov  z3">
						<radio-group class="radio-group">
							<label class="radio" v-for="item in items">
								{{item.value}}
								<radio :value="item.name" :checked="item.checked" class="sd_dreertxc" />

							</label>
						</radio-group>
					</view>
				</view>


				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						扣除合币
					</view>
					<view class="ov  z3">
						100元
					</view>
				</view>

				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						总扣合币
					</view>
					<view class="ov  z3">
						100元
					</view>
				</view>

				<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						负责人
					</view>
					<view class="ov  z3">
						王宝志
					</view>
				</view>
			</view>
		</view>
		<view class="btm pd pt20 pm20 bgff">
			<view class="fz30 z3">
				上传盘点照片
			</view>
			<view class="mt20">
				<view class="df_jhh_deert" @click="pz_dert">
					<image :src="zaop_df" v-if="zaop_df"></image>

					<icon class="dx icon-xiangji z9 cz" v-else></icon>
				</view>
			</view>
		</view>

		<view class="pd pt20 btm mt20 bgff tr">
			<view class="pt10 pm10 fz30 z3">
				盘点异常项:2
			</view>
			<view class="pt10 pm10 fz30 z3">
				异常扣除总额:<text class="red">￥400.00</text>
			</view>
		</view>

		<view class="pd bgff pt100 pm100 box">
			<view class="box_a">
				<view class="sdf_dfgxe yj4">
					均异常
				</view>
			</view>
			<view class="box_a cen">
				<view class="sdf_dfgxe yj4 ab">
					均正常
				</view>
			</view>
			<view class="box_a tr">
				<view class="sdf_dfgxe yj4 ac">
					确认盘点
				</view>
			</view>
		</view>

	</view>
</template>
<script>
	export default {
		data() {
			return {
				zaop_df: "",
				items: [{
						name: 'ssdd_a',
						value: '人为损坏',
						checked: 'true'
					},
					{
						name: 'ssdd_b',
						value: '非人为损坏'

					},
					{
						name: 'ssdd_c',
						value: '丢失',
					}
				]
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
