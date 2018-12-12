<template>
<view class="pm50">
		<view class="pr dfg_drrt pm20" :class="iy_sdf">
		<rili :is_ddf="is_ddf"  is_down="act" is_hd="act"></rili>


		</view>
		
		<view class="pd ">
			<view class="df_jh_derxet bgff pr br yj4 ov">
				<input type="text" value="" placeholder="请输入姓名" class="fz30"/>
				<icon class="dx icon-sousuo ssd_derxer z9"></icon>
			</view>
		</view>
		
		<view class="dsf_dffcrt bgff pd fz28 z6 mt20">
			<picker class="picker-item" mode="selector" :range="textList">
			处理状态 <icon class="dx icon-down "></icon>
			</picker>

		</view>
		
		<view class="sd_jh_derxert pd dx_row">
			<view class="dx_col_12 mt20" v-for="sd in 10">
					<view class="yj4 bgff dfd_dd_eetxc pt10 pm10 pr">
					<!-- 	<view class="sd_hh_drrtcrt">
							
						</view> -->
						<image src="../../../static/img/jindu_drtr.png" class="jindu_drtr"></image>
						<image src="../../../static/img/user_icon.png" class="user_icon_erff yj fl"></image>
						<view class="ov pl10 ln">
							<view class="fz26 z3">
								关于华
							</view>
							<view class="fz20 z6">
								高级开发工程师
							</view>
						</view>
						<view class="qc">
							
						</view>
						<view class="dx_row fz24 cen mt50">
							<view class="dx_col_12">
								全部(10)
							</view>
							<view class="dx_col_12 ls">
								已处理
							</view>
						</view>
						
						
					</view>
			</view>
		</view>
		
		
	</view>
</template>
<script>
	import rili from "@/components/rili.vue"
	export default {
		data() {
			return {
				is_ddf: true,
				textList: [
					'text1',
					'text2',
					'text3'
				],
			}
		},
		components: {
			rili
		},
		methods: {},
		mounted() {},
	}
</script>
<style scoped>
	.sd_jh_derxert{
		margin-left: -10upx;
		margin-right: -10upx;
	}
	.sd_jh_derxert  .dx_col_12{

		padding-left: 10upx;
		padding-right: 10upx;
	}
	.df_jh_derxet{
		height: 70upx;
		line-height: 70upx;
		padding-top: 15upx;
		padding-left: 30upx;
	}
	
	.ssd_derxer{
		position: absolute;
		right: 20upx;
		top: 0upx;
	}
	.dsf_dffcrt{
		line-height: 80upx;
	}
	.user_icon_erff{
		width: 78upx;
		height: 78upx;
	}
	.sd_hh_drrtcrt{
		width: 90upx;
		height: 90upx;
		background: red;
		position: absolute;
		right: 10upx;
		top: 10upx;
	}
	.dfd_dd_eetxc{
		padding-left: 10upx;
		padding-right: 10upx;
	}
	.jindu_drtr{
		position: absolute;
		right: 10upx;
		top: 10upx;
		width: 78upx;
		height: 78upx;
	}
</style>
