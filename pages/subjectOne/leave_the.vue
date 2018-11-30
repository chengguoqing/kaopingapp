<!-- 我开出的 -->
<template>
	<view class="pd">

		<view class=" pt20 pm20 fz26 z6">
			全部 <icon class="dx icon-down"></icon>
		</view>

		<navigator url="/pages/subjectOne/leave_the_chuli" class="yj4 bgff box pd pt20 pm20 mb20">
			<view class="box_b ln">
				<view class="dx_row fz28 z6">
					<view class="dx_col_6">
						类型：
					</view>
					<view class="ov">
						罚 金额10元
					</view>
				</view>


				<view class="dx_row fz28 z6 mt10">
					<view class="dx_col_6">
						时间：


					</view>
					<view class="ov">
						2018-10-28 10:00:01

					</view>
				</view>



				<view class="dx_row fz28 z6 mt10">
					<view class="dx_col_6">
						事由：
					</view>
					<view class="ov">
						上班瞌睡
					</view>
				</view>

			</view>
			<view class="box_a pt20 cen">
				<icon class="dx icon-mail fz60 ls"></icon>
				<view class="fz30 ls">
					处理
				</view>

			</view>
		</navigator>




		<navigator class="yj4 bgff box pd pt20 pm20 mb20" url="/pages/subjectOne/leave_superior">
			<view class="box_b ln">
				<view class="dx_row fz28 z6">
					<view class="dx_col_6">
						类型：
					</view>
					<view class="ov">
						罚 金额10元
					</view>
				</view>


				<view class="dx_row fz28 z6 mt10">
					<view class="dx_col_6">
						时间：


					</view>
					<view class="ov">
						2018-10-28 10:00:01

					</view>
				</view>



				<view class="dx_row fz28 z6 mt10">
					<view class="dx_col_6">
						事由：
					</view>
					<view class="ov">
						上班瞌睡
					</view>
				</view>

			</view>
			<view class="box_a pt20 cen">
				<icon class="dx icon-mail fz60 z9"></icon>
				<view class="fz30 z9">
					已处理
				</view>

			</view>
		</navigator>







		<navigator class="yj4 bgff box pd pt20 pm20 mb20">
			<view class="box_b ln">
				<view class="dx_row fz28 z6">
					<view class="dx_col_6">
						类型：
					</view>
					<view class="ov">
						罚 金额10元
					</view>
				</view>


				<view class="dx_row fz28 z6 mt10">
					<view class="dx_col_6">
						时间：


					</view>
					<view class="ov">
						2018-10-28 10:00:01

					</view>
				</view>



				<view class="dx_row fz28 z6 mt10">
					<view class="dx_col_6">
						事由：
					</view>
					<view class="ov">
						上班瞌睡
					</view>
				</view>

			</view>
			<view class="box_a pt20 cen">


			</view>
		</navigator>


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
						cls: "",
						href: "/pages/subjectOne/send_bill_me",
						name: "开给我的"
					}, {
						cls: "act",
						href: "",
						name: "我开出的"
					},
					{
						cls: "",
						href: "",
						name: "统计分析"
					}
				],

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
				uni.redirectTo({
					url: sd.href
				});
			}
		},
		mounted() {},
	}
</script>
<style scoped></style>
