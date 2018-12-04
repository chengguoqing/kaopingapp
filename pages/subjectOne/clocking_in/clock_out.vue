<!-- 下班打卡 -->
<template>
	<view class="pm100 bgff pd">

		<view class="fz26 z9 pt20 ">
			2018年10月19日
		</view>
		<view class="fz26 z9 pt20 pm20">
			打卡记录时间和位置
		</view>

		<!-- 进度条 -->

		<view class="sd_jind_er pr pl30">
			<view class="zhsinh_sder">

			</view>
			<view class="sd_jh_row ln">
				<text class="yj siyhtdd_dert"></text>
				<view class="fz28">
					上班打卡时间07：50 <text class="ls_er fz26">验证通过</text>
					<icon class="dx icon-xiangji1 z9 ml10" @click="is_dakaicg_san=true"></icon>
					<text class="sd_kjh_dfgx cf ml10" @click="is_dakaicg_er=true">开始校验</text>
				</view>
				<view class="fz26 z9">
					海南省海口市迎宾路棕榈公寓
				</view>
			</view>

			<view class="sd_jh_row ln ab">
				<text class="yj siyhtdd_dert ab"></text>

				<view class="fz28">
					下班打卡
				</view>
			</view>

		</view>



		<navigator url="" class="sh_dakai_e cen cf ln yj" @click="is_dakaicg=true">
			<view class="fz48 ">
				下班打卡
			</view>
			<view class="fz28 ">
				07:50:00
			</view>

		</navigator>

		<!--打卡成功 弹窗 -->
		
		<view class="dakaicheng_d ln cen" v-if="is_dakaicg">
			<view class="sd_jhh_df ls">
				17:50
			</view>
			<view class="ls fz26">
				下班打卡成功
			</view>
			<view class="z9 fz28 djg_jh_det ">
				下班了，期待新一天的工作
			</view>
			
			<view class="mt20 pt20 pm20 ls fz30 btm " @click="is_dakaicg=false" >
				提交上级直检
			</view>
			
		</view>
		
		
		
		<!--人脸验证失败 弹窗 -->
		<view class="dakaicheng_d ln cen" v-if="is_dakaicg_er">
			<view class="sd_jhh_df ls">
				17:50
			</view>
			<view class="red fz26">
				人脸识别失败
			</view>
			<view class="z9 fz28 djg_jh_det ab">
				
			</view>
			
			<view class="mt20 pt20 pm20 ls fz30 btm box" >
				<view class="box_a" @click="is_dakaicg_er=false">
					我知道了
				</view>
				<view class="box_a" @click="is_dakaicg_er=false">
					异常申诉
				</view>
			</view>
			
		</view>
		
		
		
		
		<!--人脸验证成功 弹窗 -->
		<view class="dakaicheng_d ln cen" v-if="is_dakaicg_san">
			<view class="sd_jhh_df ls">
				17:50
			</view>
			<view class="ls fz26">
				人脸识别成功
			</view>
			<view class="z9 fz28 djg_jh_det ab">
				
			</view>
			
			<view class="mt20 pt20 pm20 ls fz30 btm " @click="is_dakaicg_san=false">
				
					我知道了
				
				
			</view>
			
		</view>
		
		
		
		

	</view>
</template>
<script>
	export default {
		data() {
			return {
				is_dakaicg:false, //打卡成功弹窗
				is_dakaicg_er:false,
				is_dakaicg_san:false
			}
		},
		components: {},
		methods: {},
		mounted() {},
	}
</script>
<style scoped>
	.sd_kjh_dfgx {
		width: 150upx;
		height: 43upx;
		line-height: 43upx;
		text-align: center;
		display: inline-block;
		background: #489FF6;
		border-radius: 20px;
	}

	.zhsinh_sder {
		position: absolute;
		left: 0px;
		top: 15upx;
		width: 1px;
		height: 100%;
		background: #C8C9CA;
	}

	.sd_jh_row {
		position: relative;
	}

	.sd_jh_row.ab {
		margin-top: 130upx;
	}

	.siyhtdd_dert {
		width: 16upx;
		height: 16upx;
		border-radius: 50%;
		background: #C8C9CA;
		position: absolute;
		left: -37upx;
		top: 10upx;
	}

	.siyhtdd_dert.ab {
		background: #489FF6;
	}

	.sh_dakai_e {
		width: 260upx;
		height: 260upx;
		background: #489FF6;
		margin: auto;
		margin-top: 80upx;
		padding-top: 80upx;
	}

	.dakaicheng_d {
		position: fixed;
		left: 0;
		right: 0;
		top: 0;
		bottom: 0;
		margin: auto;
		width: 450upx;
		height: 560upx;
		background: #fff;
		box-shadow: 0 0px 16upx rgba(0, 0, 0, .1);
		padding-top: 100upx;
	}

	.sd_jhh_df {
		font-size: 100upx;
	}
	.djg_jh_det{
		margin-top: 115upx;
	
		padding-bottom: 20upx;
		
	}
	.djg_jh_det.ab{
		height: 60upx;
	}
</style>
