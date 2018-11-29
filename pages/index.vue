<template>
	<view>
		<view class=" pd bgff gfh_jh_dertt dx_row pr bbm" v-for="sd in sd_ddf" @click="tiaozsf(sd.path)">

			<view class="f_b fz30 z3 cz pr">
				<text class="z6">{{sd.style.navigationBarTitleText}}</text>
			</view>
			<view class="right_ert">

				<icon class="dx icon-right"></icon>
			</view>
		</view>



	</view>
</template>
<script>
	export default {
		data() {
			return {
				sd_ddf: [ //pages数组中第一项表示应用启动页，参考：https://uniapp.dcloud.io/collocation/pages
		 {
			"path": "pages/subjectOne/my_pay_slip",
			"style": {
				"navigationBarTitleText": "我的工资条"
			}
		},{
			"path": "pages/subjectThree/sales_receipts",
			"style": {
				"navigationBarTitleText": "销售凭证"
			}
		}, {
			"path": "pages/subjectThree/goods_inventory_er",
			"style": {
				"navigationBarTitleText": "物品盘点"
			}
		}, {
			"path": "pages/subjectThree/goods_inventory",
			"style": {
				"navigationBarTitleText": "物品盘点"

			}
		}, {
			"path": "pages/subjectThree/equipment_inventory",
			"style": {
				"navigationBarTitleText": "设备盘点"

			}
		}, {
			"path": "pages/subjectThree/Internal_marketing",
			"style": {
				"navigationBarTitleText": "内部购销列表"

			}
		}, {
			"path": "pages/subjectThree/yield",
			"style": {
				"navigationBarTitleText": "产量-本周"

			}
		}, {
			"path": "pages/subjectThree/yield_er",
			"style": {
				"navigationBarTitleText": "产量-本月"

			}
		}, {
			"path": "pages/subjectTwo/examination_hall",
			"style": {
				"navigationBarTitleText": "科举大厅 "
			}
		}, {
			"path": "pages/subjectThree/purchasing_requisition",
			"style": {
				"navigationBarTitleText": "采购申请",
				"usingComponents": {
					"van-field": "/wxcomponents/field/index",
					"van-cell": "/wxcomponents/cell/index",
					"van-cell-group": "/wxcomponents/cell-group/index"
				}
			}
		}, {
			"path": "pages/subjectThree/msg_gl",
			"style": {
				"navigationBarTitleText": "消息",
				"usingComponents": {
					"van-tab": "/wxcomponents/tab/index",
					"van-tabs": "/wxcomponents/tabs/index"
				}
			}
		}, {
			"path": "pages/subjectThree/index",
			"style": {
				"navigationBarTitleText": "首页",
				"usingComponents": {
					"van-notice-bar": "/wxcomponents/notice-bar/index",
					"van-toast": "/wxcomponents/toast/index",
					"van-row": "/wxcomponents/row/index",
					"van-col": "/wxcomponents/col/index",
					"van-button": "/wxcomponents/button/index"
				}
			}
		}, {
			"path": "pages/subjectTwo/plan_details",
			"style": {
				"navigationBarTitleText": "计划详情"
			}
		}, {
			"path": "pages/subjectTwo/keju",
			"style": {
				"navigationBarTitleText": "科举",
				"usingComponents": {
					"van-tab": "/wxcomponents/tab/index",
					"van-tabs": "/wxcomponents/tabs/index"
				}
			}
		}, {
			"path": "pages/subjectTwo/finish_planxq",
			"style": {
				"navigationBarTitleText": "计划进度完成情况 "
			}
		}, {
			"path": "pages/subjectTwo/finish_plan",
			"style": {
				"navigationBarTitleText": "计划进度完成情况 "
			}
		}, {
			"path": "pages/subjectTwo/index",
			"style": {
				"navigationBarTitleText": "考评主页 ",
				"usingComponents": {
					"van-row": "/wxcomponents/row/index",
					"van-col": "/wxcomponents/col/index"
				}
			}
		}, {
			"path": "pages/subjectTwo/my_evaluation",
			"style": {
				"navigationBarTitleText": "我的考评情况"

			}
		}, {
			"path": "pages/subjectThree/sxy",
			"style": {
				"navigationBarTitleText": "产量-本周"

			}
		}, {
			"path": "pages/subjectThree/gztai",
			"style": {
				"navigationBarTitleText": "产量-本周"

			}
		}, {
			"path": "pages/subjectThree/user_center",
			"style": {
				"navigationBarTitleText": "产量-本周"

			}
		}
	],
			}
		},
		components: {},
		methods: {
			tiaozsf(sd) {
				if (sd == 'pages/subjectThree/msg_gl' || sd == "pages/subjectThree/msg_gl") {
					uni.switchTab({
						url:"/"+ sd
					});
					return
				}
				uni.navigateTo({
					url: "/"+sd
				});
			}
		},
		mounted() {},
	}
</script>
<style scoped></style>
