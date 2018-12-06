<template>
	<view>
		<view class=" pd bgff gfh_jh_dertt dx_row pr bbm" v-for="(sd,idx) in sd_ddf" @click="tiaozsf(sd.path)">

			<view class="f_b fz30 z3 cz pr">
				<text class="z6">{{idx+1}} {{sd.style.navigationBarTitleText}}</text>
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
								"path": "pages/subjectOne/employee_statistical_analysis_jiang",
								"style": {
									"navigationBarTitleText": "统计分析",
									"bz": "APP端-科目1-奖罚部分_员工-统计分析-奖"
								}
							}, {
								"path": "pages/subjectOne/employee_statistical_analysis_fa",
								"style": {
									"navigationBarTitleText": "统计分析",
									"bz": "APP端-科目1-奖罚部分_员工-统计分析-罚"
								}
							}, {
								"path": "pages/subjectOne/statistical_analysis_jiang",
								"style": {
									"navigationBarTitleText": "统计分析",
									"bz": "APP端-科目1-奖罚部分_上级-统计分析-奖"
								}
							}, {
								"path": "pages/subjectOne/statistical_analysis_fa",
								"style": {
									"navigationBarTitleText": "统计分析",
									"bz": "APP端-科目1-奖罚部分_上级-统计分析-罚"
								}
							}, {
								"path": "pages/subjectOne/for_single_list",
								"style": {
									"navigationBarTitleText": "奖罚",
									"bz": "员工-奖罚列表"
								}
							}, {
								"path": "pages/subjectOne/for_single",
								"style": {
									"navigationBarTitleText": "奖单",
									"bz": "员工-奖单"
								}
							}, {
								"path": "pages/subjectOne/employee_ticket_appeal",
								"style": {
									"navigationBarTitleText": "罚单",
									"bz": "奖罚部分_员工-罚单申诉"
								}
							}, {
								"path": "pages/subjectOne/view_complaints",
								"style": {
									"navigationBarTitleText": "罚单"
								}
							}, {
								"path": "pages/subjectOne/send_bill_me",
								"style": {
									"navigationBarTitleText": "罚单-开给我的"
								}
							}, {
								"path": "pages/subjectOne/statistic_analysis",
								"style": {
									"navigationBarTitleText": "统计分析"
								}
							}, {
								"path": "pages/subjectOne/pool_section/detail_earnings",
								"style": {
									"navigationBarTitleText": "薪酬池",
									"app-plus": {
										"bounce": "none", //关闭窗口回弹效果
										"titleNView": {
											"buttons": [ //原生标题栏按钮配置,
												{
													"text": "\ue6ba",
													"fontSize": "22",
													"fontSrc": "static/fonts/iconfont.ttf"
												}
											]
										}
									}
								}
							}, {
								"path": "pages/subjectOne/landing_card/landing_card_list_er",
								"style": {
									"navigationBarTitleText": "落地卡列表二"
								}
							}, {
								"path": "pages/subjectOne/landing_card/landingcard_er",
								"style": {
									"navigationBarTitleText": "落地卡二",
					
									"app-plus": {
										"bounce": "none", //关闭窗口回弹效果
										"titleNView": {
											"buttons": [ //原生标题栏按钮配置,
												{
													"text": "\ue6ba",
													"fontSize": "22",
													"fontSrc": "static/fonts/iconfont.ttf"
												}
											]
										}
									}
								}
							}, {
								"path": "pages/subjectOne/landing_card/landingcard",
								"style": {
									"navigationBarTitleText": "落地卡",
									"app-plus": {
										"bounce": "none", //关闭窗口回弹效果
										"titleNView": {
											"buttons": [ //原生标题栏按钮配置,
												{
													"text": "\ue6ba",
													"fontSize": "22",
													"fontSrc": "static/fonts/iconfont.ttf"
												}
											]
										}
									}
								}
							}, {
								"path": "pages/subjectOne/landing_card/landing_card_list",
								"style": {
									"navigationBarTitleText": "落地卡列表"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/spot_check_list",
								"style": {
									"navigationBarTitleText": "抽检-图表列表"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/clock_out",
								"style": {
									"navigationBarTitleText": "下班打卡"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/punch_card",
								"style": {
									"navigationBarTitleText": "打卡",
									"app-plus": {
										"bounce": "none", //关闭窗口回弹效果
										"titleNView": {
											"buttons": [ //原生标题栏按钮配置,
												{
													"text": "\ue6ba",
													"fontSize": "22",
													"fontSrc": "static/fonts/iconfont.ttf"
												}
											]
										}
									}
								}
							}, {
								"path": "pages/subjectOne/clocking_in/direct_inspection_list",
								"style": {
									"navigationBarTitleText": "直检（10月23日）",
									"app-plus": {
										"bounce": "none", //关闭窗口回弹效果
										"titleNView": {
											"buttons": [ //原生标题栏按钮配置,
												{
													"text": "全选",
													"fontSize": "16"
												}
											]
										}
									}
								}
							}, {
								"path": "pages/subjectOne/clocking_in/spot_check",
								"style": {
									"navigationBarTitleText": "抽检（10月23日）"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/movement",
								"style": {
									"navigationBarTitleText": "行动轨迹分布图"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/department_holidays",
								"style": {
									"navigationBarTitleText": "设置部门公休日"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/abnormal_complaints_er",
								"style": {
									"navigationBarTitleText": "异常申诉二"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/abnormal_complaints",
								"style": {
									"navigationBarTitleText": "异常申诉"
								}
							}, {
								"path": "pages/subjectOne/clocking_in/direct_inspection",
								"style": {
									"navigationBarTitleText": "直检"
								}
							}, {
								"path": "pages/subjectOne/leave_superior",
								"style": {
									"navigationBarTitleText": "我开出的-上级"
								}
							}, {
								"path": "pages/subjectOne/leave_the_chuli",
								"style": {
									"navigationBarTitleText": "我开出的-处理"
								}
							}, {
								"path": "pages/subjectOne/leave_the",
								"style": {
									"navigationBarTitleText": "我开出的"
								}
							}, {
								"path": "pages/subjectOne/details_test_er",
								"style": {
									"navigationBarTitleText": "考试详情",
									"usingComponents": {
										"van-popup": "/wxcomponents/popup/index"
									}
								}
							}, {
								"path": "pages/subjectOne/record_details",
								"style": {
									"navigationBarTitleText": "成绩详情"
								}
							}, {
								"path": "pages/subjectOne/details_test",
								"style": {
									"navigationBarTitleText": "考试详情"
								}
							}, {
								"path": "pages/subjectOne/attendance_details",
								"style": {
									"navigationBarTitleText": "考勤详情"
								}
							}, {
								"path": "pages/subjectOne/behavioral_details",
								"style": {
									"navigationBarTitleText": "行为详情"
								}
							}, {
								"path": "pages/subjectOne/labor_summary_er",
								"style": {
									"navigationBarTitleText": "人工费用汇总"
								}
							}, {
								"path": "pages/subjectOne/labor_summary",
								"style": {
									"navigationBarTitleText": "人工费用汇总"
								}
							}, {
								"path": "pages/subjectOne/my_pay_slip",
								"style": {
									"navigationBarTitleText": "我的工资条"
								}
							}, {
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
							}
				],
			}
		},
		components: {},
		methods: {
			tiaozsf(sd) {
				if (sd == 'pages/subjectThree/msg_gl' || sd == "pages/subjectThree/msg_gl") {
					uni.switchTab({
						url: "/" + sd
					});
					return
				}
				uni.navigateTo({
					url: "/" + sd
				});
			}
		},
		mounted() {},
	}
</script>
<style scoped></style>
