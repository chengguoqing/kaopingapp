<template>
	<view class="bgff pm100">
	
		

		<tab_qh :sd_dfg="sd_dfg"></tab_qh>
	
		<view class="dsf_jh_deeretxcrf ">
			<view class="box pd mt20">
				<view class="box_a pr20">
					<view class="pr dsf_jh_ddrtxf br">
						<text class="z6 fz26 ml20 cz">分之合智库/海口  总公司</text>
						<icon class="dx icon-down cz"></icon>
					</view>
				</view>
				<view class="box_a pl20">
					<view class="pr dsf_jh_ddrtxf br ab">
						<text class="z6 fz26 ml20 cz">软件事业部</text>
						<icon class="dx icon-down cz"></icon>
					</view>
				</view>
				
				
			</view>
			
			
			<view class="sd_quyg_ert cen ov">
				<view class="fz30 mt70">
					余额
				</view>
				<view class="ls fz50 mt20">
					15000
				</view>
				
				<image src="../../../static/img/jindutiao.png" class="sd_hjinduer"></image>
			</view>
			
			
			<tab_qh :sd_dfg="sd_dfg_er" is_sdf="1"></tab_qh>

		<view class="pd pt20 pm20 bbm box" v-for="sd in 10">
				<view class="box_b ln">
						<view class="fz32 z3">
							考试罚单
						</view>
						<view class="fz26  z9 mt5">
							2018-10-30  15:04
						</view>
				</view>
				<view class="box_a pt30 fz30 z3 tr">
					+150
	</view>


		</view>

			
		</view>




		<!-- 右上角的菜单 -->
		<view class="yopushangjiao fz30" v-if="is_kh_d">
			<text class="uy_rrttxcdd"></text>
			<view class="fkiy_list cf" @click="is_kh_d=false">
				<icon class="dx icon-add fz40 cz"></icon>
				<text class="cz">使用申请</text>
			</view>
			<view class="fkiy_list cf ab btm" @click="is_kh_d=false">
				<icon class="dx icon-add fz40 cz"></icon>
				<text class="cz">使用记录</text>
			</view>
		</view>





	</view>
</template>
<script>
	import tab_qh from "@/components/tab_qh.vue"
	export default {
		data() {
			return {
				is_kh_d: false,
				sd_dfg: [{
					name: "当天",
					cls: "act"
				}, {
					name: "七天",
					cls: ""
				}, {
					name: "一个月",
					cls: ""
				}, {
					name: "更多筛选",
					cls: ""
				}],
				sd_dfg_er:[{
					name: "收入明细",
					cls: "act"
				}, {
					name: "支出明细",
					cls: ""
				}]
			}
		},
		components: {
			tab_qh
		},
		methods: {},
		mounted() {},
		onNavigationBarButtonTap() {
			this.is_kh_d = true
		}
	}
</script>
<style scoped>
	.yopushangjiao {
		position: fixed;
		right: 0;
		top: 40upx;
		width: 245upx;
		z-index: 10000;
		background: #67B7F9;
	}

	.fkiy_list {
		line-height: 80upx;
		padding-left: 20upx;
	}

	.uy_rrttxcdd {
		width: 40upx;
		height: 40upx;
		transform: rotate(45deg);
		position: absolute;

		right: 20upx;
		margin: auto;
		top: -20upx;
		background: #67B7F9;
	}

	.dsf_jh_ddrtxf {
		border-radius: 20px;
		width: 402upx;
		line-height: 50upx;
		height: 60upx;
	}

	.dsf_jh_ddrtxf .dx {
		position: absolute;
		right: 20upx;
		top: 8upx;
	}
	.dsf_jh_ddrtxf.ab{
		width: 260upx;
		float: right;
	}
	.dsf_jh_deeretxcrf{
		padding-top: 110upx;
	}
	
	.sd_quyg_ert{
		width: 370upx;
		height: 370upx;
		border: 20upx solid #E9F6FF;
		border-radius: 50%;
		position: relative;
		margin: auto;
		margin-top: 50upx;
	}
	.sd_hjinduer{
		position: absolute;
		left: 0px;
		bottom: 0px;
		width: 100%;
		height: 132upx;
	}
</style>
