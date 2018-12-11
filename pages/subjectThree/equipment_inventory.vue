<template>
	<view>

		<view class="sheb_page">
			<view class="sd_kjh_dertx pd box">
				<view class="box_a fz32">
					扳手
				</view>
				<view class="box_a tr">
					<icon class="dx icon-close fz45 red "></icon>
					<icon class="dx icon-gouhao fz50 ls_er ml10"></icon>
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
						<view class="f_b mr10 fz26" v-for="item in items" @click="gouxuan(item)">
							<text class="cz">{{item.value}}</text>
							<image src="../../static/img/chas_a.png" v-if="!item.checked"  class="f_b chas_dert cz pr ml5"></image>
							<image src="../../static/img/chas_b.png"  v-else class="f_b chas_dert cz pr ml5"></image>
						</view>
					
					</view>
				</view>

	<view class="dx_row pt20 pm20 fz30">
					<view class="sddsff  z6">
						结余数量
					</view>
					<view class="ov  z3">
						<input type="number" class="jieyushuliang_e" />
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
				
				
				
					<view class="dx_row pt20 pm20 fz30">
									<view class="sddsff  z6">
										结余数量
									</view>
									<view class="ov  z3">
										<textarea value="有两个设备在使用中损坏了" placeholder=""  class="jieyushuliang_e ab"/>
									</view>
								</view>



			</view>

		</view>



		<view class="sheb_page">
			<view class="sd_kjh_dertx pd box">
				<view class="box_a fz32">
					羊角锤
				</view>
				<view class="box_a tr">
					<icon class="dx icon-close fz45 red "></icon>
					<icon class="dx icon-gouhao fz50 ls_er ml10"></icon>
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
							<view class="f_b mr10 fz26" v-for="item in itemsm" @click="gouxuaner(item)">
								<text class="cz">{{item.value}}</text>
								<image src="../../static/img/chas_a.png" v-if="!item.checked"  class="f_b chas_dert cz pr ml5"></image>
								<image src="../../static/img/chas_b.png"  v-else class="f_b chas_dert cz pr ml5"></image>
							</view>
						
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
				盘点异常项: <text class="f_b sd_jhdeertxrty">2</text>
			</view>
			<view class="pt10 pm10 fz30 z3">
				异常扣除总额:<text class="red fz36">￥400.00</text>
			</view>
		</view>

		<view class="pd bgff pt100 pm100 box">
			<view class="box_a">
				<view class="sdf_dfgxe ">
					均异常
				</view>
			</view>
			<view class="box_a cen">
				<view class="sdf_dfgxe  ab">
					均正常
				</view>
			</view>
			<view class="box_a tr">
				<view class="sdf_dfgxe  ac">
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
						checked:true
					},
					{
						name: 'ssdd_b',
						value: '非人为损坏',
						checked: false

					},
					{
						name: 'ssdd_c',
						value: '丢失',
						checked: false
					}
				],	itemsm: [{
						name: 'ssdd_a',
						value: '人为损坏',
						checked:true
					},
					{
						name: 'ssdd_b',
						value: '非人为损坏',
						checked: false

					},
					{
						name: 'ssdd_c',
						value: '丢失',
						checked: false
					}
				]
			}
		},
		components: {},
		methods: {
			gouxuan(sd){
				this.items.map(a=>{
					a.checked=false
				})
				sd.checked=true
			},gouxuaner(sd){
				this.itemsm.map(a=>{
					a.checked=false
				})
				sd.checked=true
			},
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
	.red{
		color: #fe4e0f !important;
	}
	.sd_kjh_dertx{
		line-height: 90upx;
	}
	.sd_jhdeertxrty{
		width: 130upx;
		text-align: left;
		padding-left: 20upx;
	}
	.chas_dert{
		
		width: 34upx;
		height: 34upx;
	}
	.chas_dert icon{
		position: absolute; 
		left: 0;
		top: 0;
		
	}
	.jieyushuliang_e{
		width: 200upx;
		height: 55upx;
		border: 1px solid #E6E6E6;
		padding-left: 20upx;
		font-size: 28upx;
	}
	.jieyushuliang_e.ab{
		width: 100%;
		height:95upx ;
		padding-top: 20upx;
	}
</style>
