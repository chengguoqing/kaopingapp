<template>
	<view class="pm50">
		<view class="pr dfg_drrt pm20" :class="iy_sdf">
			<rili :is_ddf="is_ddf" @sddffff="sddffff"></rili>

		</view>




		<view class="pd df_k_paher bgff mt20">
			<image src="../../../static/img/user_icon.png" class="user_icon_der fl"></image>
			<view class="ov pl20 box pt20">
				<view class="box_a">
					<view class="fz32">
						管玉华
					</view>
					<view class="fz28 z9 mt10">
						JAVA开发
					</view>
				</view>

				<view class="box_a tr z6">
					<view class="fz28">
						软件事业部
					</view>
					<view class="fz28  mt15">
						直接上级：刘峰
					</view>
				</view>



			</view>


		</view>


		<view class="pd pt20 pm20 red fz30 box">
			<view class="box_a">
				<text class="cz">总扣分：0分</text>
			</view>
			<view class="box_a tr">
				<view class="dx_btn sd_dsf_derrt  cen f_b">
					权重分配
				</view>
			</view>
		</view>

		<view class="bgff   pt20 pm20 bbm" v-for="(sd,idx) in ['考','问','监']">
			<view class="sd_jh_dfdf box " :class="'sd_sds'+idx">
				<view class="box_b">
					<view class="fz30 f_b">【<text class="ls_er">{{sd}}</text>】每日一考</view> <br>
					<text class="fz26 z9">时量：当日17：30至次日07：30<br>
						自检(-10分) 自检(-10分) 自检(-10分)
					</text>

				</view>

				<view class="box_a tr fz30">

					权重：40
					<view class="red fz28 mt60">
						20/10
					</view>
				</view>



			</view>

		</view>

		<view class="sd_jh_dsd_page">
			<view class="pt20 pm20 pd fz30">
				六补一抠
			</view>
			<view class="bgff pd pt20 pm20 d_derr_deert">
				<view class="fz28 z3">
					结果：<text class="z9 ml10">不作为</text>
				</view>
				<view class="fz28 z3 mt20">
					原因：<text class="z9 ml10">没完成工作任务</text>
				</view>
			</view>
			
		</view>
		
		
		<view class="pt20 pm20 pd fz30 pr">
			工作日记
		<icon class="dx icon-down down_defgxc"></icon>
		</view>
		
		<view class="pt20 pm20 pd fz30 pr mt20">
			工作流
		<icon class="dx icon-down down_defgxc"></icon>
		</view>

	
	
	



		<!-- 右上角的菜单 -->
		<view class="yopushangjiao fz30" v-if="is_kh_d">
			<text class="uy_rrttxcdd"></text>
			<view class="fkiy_list cf" @click="is_kh_d=false">
				<icon class="dx icon-add fz40 cz"></icon>
				<text class="cz">派临时工单</text>
			</view>
			<view class="fkiy_list cf ab"  @click="is_kh_d=false">
				<icon class="dx icon-add fz40 cz"></icon>
				<text class="cz">派计划工单</text>
			</view>
		</view>


	</view>
</template>
<script>
	import rili from "@/components/rili.vue"

	export default {
		data() {
			return {
				is_kh_d: false,
				is_ddf: true,
				kou_sdf:[
					{
						name:"六补一抠",
						cls:""
					},{
						name:"工作日记",
						cls:""
					},{
						name:"工作流",
						cls:""
					}
				]
			}
		},
		components: {
			rili
		},
		methods: {
			sddffff() {
				this.iy_sdf ? this.iy_sdf = '' : this.iy_sdf = 'act'
			}
		},
		mounted() {},
		onNavigationBarButtonTap() {
			this.is_kh_d = true
		}
	}
</script>
<style scoped>
	.down_defgxc{
		position: absolute;
		right: 20upx;
		top: 10upx;
	}
	.d_derr_deert{
		min-height: 250upx;
	}
	.sd_jh_dfdf {
		padding-left: 40upx;
		padding-right: 20upx;
		line-height: 1;
		border-left: 10upx solid #23AC3B;

	}
	.sd_dsf_derrt{
		width: 180upx;
		line-height: 55upx;
		height: 55upx;
		font-size: 28upx !important;
		}

	.sd_sds1 {
		border-left: 10upx solid #C30C24
	}

	.sd_sds2 {
		border-left: 10upx solid #F39800
	}

	.sd_sds1 .ls_er {
		color: #C30C24 !important;
	}

	.sd_sds2 .ls_er {
		color: #F39800 !important;
	}

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

	.fkiy_list.ab {
		border-top: 1px solid #55A9F7;
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

	.dfg_drrt {
		height: 250upx;
	}

	.dfg_drrt.act {
		height: 800upx !important;
	}

	.sd_jh_df_drt {
		height: 13upx;
		background: #fff;
	}

	.jidu_eertt {
		position: absolute;
		left: 0;
		top: 0px;
		height: 100%;
		background: #489EF5;
	}

	.sd_hg_df {
		border: 1px solid #EEEEEE;
		background: #fff;
		width: 70upx;
		height: 70upx;
		text-align: center;
		line-height: 70upx;
		font-size: 28upx;
		color: #999;
		position: absolute;
		left: 50upx;
		top: -25upx;
	}

	.sd_hg_df.ab {
		left: 30%;
	}

	.sd_hg_df.ac {
		left: 55%;
	}

	.sd_hg_df.ad {
		left: 85%;
	}

	.dsf_dffsdfre.aa .sd_hg_df.aa,
	.dsf_dffsdfre.ab .sd_hg_df.ab,
	.dsf_dffsdfre.ab .sd_hg_df.aa,

	.dsf_dffsdfre.ac .sd_hg_df.aa,
	.dsf_dffsdfre.ac .sd_hg_df.ab,
	.dsf_dffsdfre.ac .sd_hg_df.ac,
	.dsf_dffsdfre.ad .sd_hg_df {
		background: #489EF5 !important;
		color: #fff !important;
		border: 1px solid #489EF5;
	}

	.dsf_dffsdfre.aa .jidu_eertt {
		width: 50upx;
	}

	.dsf_dffsdfre.ab .jidu_eertt {
		width: 30%;
	}

	.dsf_dffsdfre.ac .jidu_eertt {
		width: 55%;
	}

	.dsf_dffsdfre.ad .jidu_eertt {
		width: 100%;
	}

	.user_icon_der {
		width: 130upx;
		height: 130upx;

	}

	.df_k_paher {
		padding-top: 50upx;
		padding-bottom: 50upx;
	}
</style>
