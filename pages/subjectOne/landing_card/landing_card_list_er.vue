<template>
<view class="pm50">
		<view class="pr dfg_drrt pm20" :class="iy_sdf">
			<rili :is_ddf="is_ddf" ></rili>

		</view>
		
		<view class="pd mt20">
			<view class="df_jh_derxet bgff pr br yj4 ov">
				<input type="text" value="" placeholder="请输入姓名" class="fz30"/>
				<icon class="dx icon-sousuo ssd_derxer z9"></icon>
			</view>
		</view>
		
		<view class="dsf_dffcrt bgff pd fz30 mt20">
			处理状态 <icon class="dx icon-down "></icon>
		</view>
		
		<view class="sd_jh_derxert pd dx_row">
			<view class="dx_col_12 mt20" v-for="sd in 10">
					<view class="yj4 bgff pd pt10 pm10 pr">
					<!-- 	<view class="sd_hh_drrtcrt">
							
						</view> -->
						<image src="../../../static/img/user_icon.png" class="user_icon_erff yj fl"></image>
						<view class="ov pl10">
							<view class="fz32 z3">
								关于华
							</view>
							<view class="fz24 z6">
								高级开发工程师
							</view>
						</view>
						<view class="qc">
							
						</view>
						<view class="dx_row fz30 cen mt50">
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
		width: 82upx;
		height: 82upx;
	}
	.sd_hh_drrtcrt{
		width: 90upx;
		height: 90upx;
		background: red;
		position: absolute;
		right: 10upx;
		top: 10upx;
	}
</style>
