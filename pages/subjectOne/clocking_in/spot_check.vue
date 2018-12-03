<template>
	<view class="pd bgff">
		<view class="pt20 pm20 fz30 z3">
			> 海口分公司 > 软件事业部
		</view>

		<view class="br yj4 f_jh_derrtcr pr">
			<input type="text" placeholder="请输入姓名" class="fz30" />
			<icon class="dx icon-sousuo z9 df_h_deerttxret"></icon>
		</view>

		<view class="dx_row fz30 z3 mt20">
			<view class="dx_col_8">
				处理状态 <icon class="dx icon-down"></icon>
			</view>
			<view class="dx_col_8">
				打卡状态 <icon class="dx icon-down"></icon>
			</view>
		</view>


		<view class="dx_row dsf_roww_er">
			<view class="dx_col_12 g_jhj_deerddf " v-for="sd in 10">
				
				<view class="d_casexer br  pt20  yj4 ov pr ">
					<view class="pd">
						
					
					<image src="../../../static/img/user_icon.png" class="user_drertxc fl" ></image>

					<view class="ov pl20 ln">
						<view class=" fz32 mt10">
							许润龙
						</view>
						<view class="fz26 z9">
							JAVA开发
						</view>
					</view>
					<view class="qc"></view>

					<view class="mt20">
						<text class="fz26 cf dfs_jh_deertddfe ac">迟到</text>
						<text class="fz26 cf dfs_jh_deertddfe ab">请假</text>

					</view>

					<view class="mt40 fz28">
						抽查通过率 <text class="ls fz24 ml20">打卡正常</text>
					</view>
					<view class="fz50 ls">
						100%
					</view>
					</view>
					<view class="mt20 df_btn_der fz30">
						待处理
					</view>
					

				</view>
				
			</view>
		</view>




	</view>
</template>
<script>
	export default {
		data() {
			return {}
		},
		components: {},
		methods: {},
		mounted() {},
	}
</script>
<style scoped>
	.f_jh_derrtcr {
		height: 80upx;
		line-height: 80upx;
		background: #fff;
		padding-top: 20upx;
		padding-left: 20upx;
	}

	.df_h_deerttxret {
		position: absolute;
		right: 20upx;
		top: 0px;
	}

	/* 卡片 */
	.d_casexer {

	}

	.user_drertxc {
		width: 93upx;
		height: 93upx;
	}

	.dfs_jh_deertddfe {
		width: 87upx;
		height: 38upx;
		display: inline-block;
		line-height: 38upx;
		text-align: center;
		color: #fff;
		margin-right: 10upx;
		background: #BEEDBE;
	}

	.dfs_jh_deertddfe.ab {
		background: #FFABBF;
	}

	.dfs_jh_deertddfe.ac {
		background: #A6E8E2;
	}
	.df_btn_der{
		height: 60upx;
		line-height: 60upx;
		text-align: center;
		color: #fff;
		background:#FF4600 ;
		
	}
	.dsf_roww_er{
		margin-left: -10upx;
		margin-right: -10upx;
	}
	.g_jhj_deerddf{
		padding-left: 10upx;
		padding-right: 10upx;
		margin-top: 20upx;
	}
</style>
