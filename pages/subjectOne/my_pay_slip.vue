<template>
	<view class="pm50">
		<view class="bgls pt40 pm40 pd dx_row">
			<image src="../../static/img/user_icon.png" class="yj user_icdfr fl"></image>
			<view class="ov pl20 pt10 ln">
				<view class="fz32 cf">
					独行工匠
				</view>
				<view class="fz26 mt10">
					独行工匠工作室/软件开发
				</view>
			</view>

		</view>

		<view class="mt20 pd bgff">
			<picker class="pt20 fz30 ls" mode="date" @change="dateChange" end="2020-01-01" start="2010-01-01">

				{{time}}
				<icon class="dx icon-down"></icon>

			</picker>

			<view class="cen">
				<icon class="dx icon-ico_home_obligation dsf_deettx ls"></icon>
				<view class="fz40 ls pm20">
					4700.00
				</view>
			</view>
		</view>

		<view class="mt20 bgff">


			<view class="pd pt20 pm10 fz32 box" @click="is_sdf_a?is_sdf_a=false:is_sdf_a=true">
				<view class="box_b">
					基本工资 <text class="ml20">+3800</text>
				</view>
				<view class="box_a tr">
					<icon class="dx icon-up1 " :class="is_sdf_a?'dfsd_jh_ddgfg':''"></icon>
				</view>
			</view>

			<view class="" v-if="!is_sdf_a">


				<view class="pd pt20 pm20 fz28 z6 box btm">
					<view class="box_b">
						最低社保工资
					</view>
					<view class="box_a ls_er tr">
						+1000
					</view>
				</view>


				<view class="pd pt20 pm20 fz28 z6 box btm">
					<view class="box_b">
						岗位工资
					</view>
					<view class="box_a ls_er tr">
						+1000
					</view>
				</view>


				<view class="pd pt20 pm20 fz28 z6 box btm">
					<view class="box_b">
						学历工资
					</view>
					<view class="box_a ls_er tr">
						+1000
					</view>
				</view>


				<view class="pd pt20 pm20 fz28 z6 box btm">
					<view class="box_b">
						全勤工资
					</view>
					<view class="box_a ls_er tr">
						+1000
					</view>
				</view>
			</view>
		</view>




		<view class="mt20 bgff">
			<view class="pd pt20 pm20 fz32  btm">
				考勤工资 <text class="ml20">+700</text>
			</view>
			<view class="pd pt20 pm20 fz32  btm">
				考试工资 <text class="ml20">+700</text>
			</view>
			<view class="pd pt20 pm20 fz32  btm">
				行为工资 <text class="ml20">+700</text>
			</view>
		</view>

		<view class="mt20 bgff">
			<view class="pd pt20 pm20 fz32  btm">
				绩效工资 <text class="ml20">+700</text>
			</view>
		</view>

		<view class="mt20 bgff">
			<view class="pd pt20 pm20 fz32  btm">
				我的分红 <text class="ml20">+700</text>
			</view>
		</view>



		<view class="mt20 bgff">


			<view class="pd pt20 pm10 fz32 box" @click="is_sdf_b?is_sdf_b=false:is_sdf_b=true">
				<view class="box_b">
					其他 <text class="ml20">-3800</text>
				</view>
				<view class="box_a tr">
					<icon class="dx icon-up1 " :class="is_sdf_b?'dfsd_jh_ddgfg':''"></icon>
				</view>
			</view>
			<view v-if="!is_sdf_b">


				<view class="pd pt20 pm20 fz28 z6 box btm">
					<view class="box_b">
						五险扣除
					</view>
					<view class="box_a red tr">
						-1000
					</view>
				</view>
				<view class="pd pt20 pm20 fz28 z6 box btm">
					<view class="box_b">
						税点扣除
					</view>
					<view class="box_a red tr">
						-1000
					</view>
				</view>
			</view>


		</view>



	</view>
</template>
<script>
	export default {
		data() {
			return {
				time: "2018年10月",
				is_sdf_a: false,
				is_sdf_b: false
			}
		},
		components: {},
		methods: {
			dateChange(evt) {
				let date_e = evt.detail.value.split("-")
				this.time = date_e[0] + "年" + date_e[1] + "月";
			},
		},
		mounted() {},
	}
</script>
<style scoped>
	.red {
		color: #ff4300 !important;
	}

	.dfsd_jh_ddgfg {
		transform: rotate(180deg);
	}

	.user_icdfr {
		width: 105upx;
		height: 105upx;
	}

	.dsf_deettx {
		font-size: 100upx;
	}
</style>
