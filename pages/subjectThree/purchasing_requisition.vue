<template>
	<view>
		<van-cell-group>
			<van-field input-align="right" clearable label="采购事由" placeholder="请输入" />
		</van-cell-group>

		<view class="mt20">
			<van-cell-group>
				<van-field input-align="right" clearable label="经手人" placeholder="请输入" />
			</van-cell-group>
		</view>

		<view class="mt20">
			<van-cell-group>
				<van-cell title="经手人所属和" value="请输入" is-link />
			</van-cell-group>
		</view>
		<view class="pd pt20 pm20 box">
			<view class="box_a fz30 z9">
				采购清单
			</view>
			<view class="box_a fz30 ls tr">
				删除
			</view>
		</view>

		<view class="bgff pd fz32 z6 gfh_jh_dertt">
			物流信息
		</view>

		<van-cell-group>
			<van-field input-align="right" clearable label="物品名称" placeholder="请输入" />
			<van-field input-align="right" clearable label="品牌" placeholder="请输入" />
			<van-field input-align="right" clearable label="规格" placeholder="请输入" />
			<van-field input-align="right" clearable label="单价" placeholder="请输入" />
			<van-field input-align="right" clearable label="数量" placeholder="请输入" />
			<van-field input-align="right" clearable label="分类" placeholder="请输入" />
		</van-cell-group>


		<view class="bgff pd fz32 z6 gfh_jh_dertt mt20">
			供应商信息
		</view>

		<van-cell-group>
			<van-field input-align="right" clearable label="联系人" placeholder="请输入" />
			<van-field input-align="right" clearable label="联系人电话" placeholder="请输入" />
			<van-field input-align="right" clearable label="地址" placeholder="请输入" />
			<van-cell title="采购日期" value="请选择" is-link />

		</van-cell-group>



		<view class="bgff pd fz32 z6 gfh_jh_dertt mt20">
			货比三家 <text class="fz26">(至少填写3家供应商信息)</text>
		</view>

		<view class="bgff pd fz32 z6 gfh_jh_dertt ">
			供应商1
		</view>
		<van-cell-group>
			<van-field input-align="right" clearable label="联系人" placeholder="请输入" />
			<van-field input-align="right" clearable label="联系人电话" placeholder="请输入" />
			<van-field input-align="right" clearable label="品牌" placeholder="请输入" />
			<van-field input-align="right" clearable label="单价" placeholder="请输入" />
		</van-cell-group>

		<view class="" v-for="(sd,idx) in sd_ddff">


			<view class="bgff pd fz32 z6 gfh_jh_dertt mt20">
				供应商{{idx+2}}
			</view>
			<van-cell-group>
				<van-field input-align="right" clearable label="联系人" placeholder="请输入" />
				<van-field input-align="right" clearable label="联系人电话" placeholder="请输入" />
				<van-field input-align="right" clearable label="品牌" placeholder="请输入" />
				<van-field input-align="right" clearable label="单价" placeholder="请输入" />
			</van-cell-group>


		</view>


		<view class="bgff pd fz32 ls gfh_jh_dertt mt20 cen" @click="add_liao">
			<icon class="dx icon-add ls fz40"></icon> 添加采购物品
		</view>
		
		<view class="pd pt20 pm20 box">
			<view class="box_a fz30 z9">
				汇总
			</view>
			
		</view>
		
		<van-cell-group>
			<van-field input-align="right" clearable label="物品种类" placeholder="请输入" />
			<van-field input-align="right" clearable label="设备总数" placeholder="请输入" />
			<van-field input-align="right" clearable label="采购总费用" placeholder="请输入" />
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
