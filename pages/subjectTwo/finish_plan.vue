<template>
	<view>
		<view class="pd bgff mb20" v-for="(sd,idx) in sd_ddf">
			<view class="fz32 bbm pt30  pm20">
				<text class="z3 pt20 pm20 df_jgh_dett pd">{{sd.title}}</text>
			</view>
	
			<navigator url="/pages/subjectTwo/finish_planxq" class="dx_row pt20 pm20 bbm df_df_drrt" v-for="sd in sd.data">
				<view class="dx_col_14 fz30 z3 pd pt10">
					{{sd.name}}
				</view>
				<view class="dx_col_10 fz26 z3 pt10">
					<view class="dx_col_18 dfs_jh_deert">
						<view class="jindu_ert gd" :style="{width:sd.jindu+'%'}"></view>
					</view>
					<view class="dx_col_6 tr z6 fz22">
						{{sd.jindu}}%
					</view>
				</view>
			</navigator>

		</view>


		<view class="box sd_deert">
			<view class="box_a df_kse fz32" :class="sd.cls" v-for="sd in  sd_sdf" @click="xzdfd(sd)">
				{{sd.name}}
			</view>

		</view>


	</view>
</template>
<script>
	export default {
		data() {
			return {
				sd_sdf: [{
						cls: "act",
						href: "",
						name: "团队"
					}, {
						cls: "",
						href: "",

						name: "个人"
					},
					{
						cls: "",
						href: "",

						name: "对接"
					}
				],
				sd_ddf: [{
					title: "海口分公司",
					data: [{
						name: "软件事业部",
						jindu: "90"
					}, {
						name: "咨询事业部",
						jindu: "80"
					}, {
						name: "网络营销部",
						jindu: "90"
					}, {
						name: "人财部",
						jindu: "90"
					}]
				}, {
					title: "广州分公司",
					data: [{
						name: "软件事业部",
						jindu: "90"
					}, {
						name: "咨询事业部",
						jindu: "80"
					}, {
						name: "网络营销部",
						jindu: "90"
					}, {
						name: "人财部",
						jindu: "90"
					}]
				}]
			}
		},
		components: {},
		methods: {
			xzdfd(sd) {
				this.sd_sdf.map(a => {
					a.cls = ""
				})
				sd.cls = "act"
				if (!sd.href) {
					return
				}
				uni.navigateTo({
					url: sd.href
				});
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.df_jgh_dett {
		border-bottom: 2px solid #47A0F7;
	}

	.dfs_jh_deert {
		border: 1px solid #E5E2E0;
		border-radius: 20px;
		height: 25upx;
		overflow: hidden;

	}

	.jindu_ert {
		height: 100%;
		background: #ACD6FC;
	}

</style>
