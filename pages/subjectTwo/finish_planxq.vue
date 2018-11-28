<template>
	<view>
		<view class="pd bgff pt20 pm20">
			<text class="pd  fz26 z9">海口分公司>软件事业部</text>
		</view>
		<view class="pd bgff mb20" v-for="(sd,idx) in sd_ddf">
			<view class="fz32 bbm pt20  pm20">
				<text class="pt20 pm20 df_jgh_dett pd">{{sd.title}}</text>
			</view>
	
			<navigator url="" class="dx_row pt20 pm20 bbm df_df_drrt" v-for="sd in sd.data">
				<view class="dx_col_14 fz30 z3 pd">
					{{sd.name}}
				</view>
				<view class="dx_col_10 fz26 z3">
					<view class="dx_col_18 dfs_jh_deert">
						<view class="jindu_ert gd" :style="{width:sd.jindu+'%'}"></view>
					</view>
					<view class="dx_col_6 tr z6 fz26">
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
					title: "我要业绩",
					data: [{
						name: "经营系统100天上线",
						jindu: "90"
					}, {
						name: "经营系统利润达标或超额",
						jindu: "80"
					}]
				}, {
					title: "我要团建",
					data: [{
						name: "高职低于标准",
						jindu: "90"
					}, {
						name: "面试入职率高于标准",
						jindu: "80"
					}, {
						name: "团队岗位职责完成率",
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
