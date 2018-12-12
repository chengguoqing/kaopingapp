<template>
	<view class="pd pt20">
		<view class="" v-for="(sd,idx) in ['海口分公司','南京分公司','上海分公司']">

			<view class="pt20 pm20 fz32 touy_dert pr pl20">
				<text class="bian_kside"></text>
				{{sd}}
			</view>

			<scroll-view class="scroll-view_H pm20" scroll-x style="width: 100%">
				<view class="scroll-view-item_H yj4 br mr10 bgff pd pt10 pm10 pr zhuse" v-for="sd in 10">
					<view class="sd_jhb_dsdr ">
						<image src="../../../static/img/bingtu.png"></image>
						<view class="cf sdf_df_sdr">
							<text class="fz26">常态</text><br>
							<text class="fz18">(2/10)</text>
						</view>

						<view class="cf sdf_df_sdr ab">
							<text class="fz26">问题</text><br>
							<text class="fz18">(2/10)</text>
						</view>


						<view class="cf sdf_df_sdr ac">
							<text class="fz26">临时</text><br>
							<text class="fz18">(2/10)</text>
						</view>

					</view>

					<view class="fz28 ">
						软件事业部
					</view>

					<view class="mt60 fz28">
						完成率
					</view>
					<view class="fz60">
						30%
					</view>

					<view class="box mt20 pt10 df_dfftgcxr zhuse fz24 cen">
						<view class="box_a df_right">
							自评(10)
						</view>
						<view class="box_a ">
							直检(10)
						</view>
					</view>


				</view>
				<view class="qc">

				</view>

			</scroll-view>
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
	.touy_dert {
		line-height: 1;
	}

	.bian_kside {
		position: absolute;
		left: 0;
		top: 20upx;
		height: 30upx;
		width: 4upx;
		background: #489FF6;
	}

	.scroll-view_H {
		white-space: nowrap;
	}

	.scroll-view-item_H {
		display: inline-block;
		width: 327upx;
	}

	.zhuse {
		color: #A48B78;
	}

	.sd_jhb_dsdr {
		width: 152upx;
		height: 152upx;
		position: absolute;
		right: 10upx;
		top: 40upx;
	}

	.sd_jhb_dsdr image {
		width: 100%;
		height: 100%;
	}

	.sdf_df_sdr {
		position: absolute;
		right: 20upx;
		top: 20upx;
		line-height: 0.6;
	}

	.sdf_df_sdr.ab {
		right: none;
		left: 12upx;
		top: 60upx;
	}

	.sdf_df_sdr.ac {
		right: 22upx;
		top: 90upx;
	}

	.df_dfftgcxr {
		border-top: 1px solid #A48B78;
	}

	.df_dfftgcxr .df_right {
		border-right: 1px solid #A48B78;
	}
</style>
