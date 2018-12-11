<template>
	<view class="pt20">
		<van-cell-group >

			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					采购事由
				</view>
			</van-field>

		</van-cell-group>

		<view class="mt20">
			<van-cell-group>
				<van-field input-align="right" clearable placeholder="请输入">
					<view slot="label" class="fz30 jz">
						经手人
					</view>
				</van-field>
			</van-cell-group>
		</view>

		<view class="mt20">
			<van-cell-group>
				<van-cell is-link>
					<view slot="title" class="fz30 jz">
						经手人所属和
					</view>

					<text class="z9">请选择</text>
				</van-cell>
			</van-cell-group>
		</view>
		<view class="pd pt20 pm20 box">
			<view class="box_a fz26 z9">
				采购清单(1)
			</view>
			<view class="box_a fz26 ls tr">
				删除
			</view>
		</view>

		<view class="bgff pd fz30 z6 gfh_jh_dertt">
			物流信息
		</view>

		<van-cell-group>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30">
					物品名称
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					品牌
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					规格
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					单价
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					数量
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					分类
				</view>
			</van-field>
		</van-cell-group>


		<view class="bgff pd fz30 z6 gfh_jh_dertt mt20">
			供应商信息
		</view>

		<van-cell-group>
			<van-field input-align="right" clearable  placeholder="请输入">
				<view slot="label" class="fz30 jz">
					联系人
				</view>
			</van-field>
			<van-field input-align="right" clearable  placeholder="请输入">
				<view slot="label" class="fz30 jz">
					联系人电话
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					地址
				</view>
			</van-field>
			<van-cell title="采购日期" value="请选择" is-link>
				<view slot="label" class="fz30 jz">
					采购日期
				</view>
			</van-cell>

		</van-cell-group>



		<view class="bgff pd fz32 z6 gfh_jh_dertt mt20">
			货比三家 <text class="fz26">(至少填写3家供应商信息)</text>
		</view>

		<view class="bgff pd fz30 z6 gfh_jh_dertt ">
			供应商1
		</view>
		<van-cell-group>
			<van-field input-align="right" clearable  placeholder="请输入">
				<view slot="label" class="fz30 jz">
					联系人
				</view>
			</van-field>
			<van-field input-align="right" clearable  placeholder="请输入">
				<view slot="label" class="fz30 jz">
					联系人电话
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					品牌
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
单价
				</view>
			</van-field>
		</van-cell-group>

		<view class="" v-for="(sd,idx) in sd_ddff">


			<view class="bgff pd fz32 z6 gfh_jh_dertt mt20">
				供应商{{idx+2}}
			</view>
			<van-cell-group>
				<van-field input-align="right" clearable  placeholder="请输入">
					<view slot="label" class="fz30 jz">
						联系人
					</view>
				</van-field>
				<van-field input-align="right" clearable placeholder="请输入">
					<view slot="label" class="fz30 jz">
						联系人电话
					</view>
				</van-field>
				<van-field input-align="right" clearable  placeholder="请输入">
					<view slot="label" class="fz30 jz">
						品牌
					</view>
				</van-field>
				<van-field input-align="right" clearable placeholder="请输入">
					<view slot="label" class="fz30 jz">
						单价
					</view>
				</van-field>
			</van-cell-group>


		</view>


		<view class="bgff pd fz30 ls gfh_jh_dertt mt20 cen" @click="add_liao">
			<icon class="dx icon-add ls fz40"></icon> 添加采购物品
		</view>

		<view class="pd pt20 pm20 box">
			<view class="box_a fz30 z9">
				汇总
			</view>

		</view>

		<van-cell-group>
			<van-field input-align="right" clearable  placeholder="请输入">
				<view slot="label" class="fz30 jz">
					物品种类
				</view>
			</van-field>
			<van-field input-align="right" clearable  placeholder="请输入">
				<view slot="label" class="fz30 jz">
					设备总数
				</view>
			</van-field>
			<van-field input-align="right" clearable placeholder="请输入">
				<view slot="label" class="fz30 jz">
					采购总费用
				</view>
			</van-field>
		</van-cell-group>


		<view class="pd mt100 pm50">
			<view class="dx_btn">
				提交申请
			</view>

		</view>




	</view>
</template>
<script>
	export default {
		data() {
			return {
				sd_ddff: ['', '']
			}
		},
		components: {},
		methods: {
			add_liao() {
				this.sd_ddff.push('')
			}
		},
		mounted() {},
	}
</script>
<style scoped></style>
