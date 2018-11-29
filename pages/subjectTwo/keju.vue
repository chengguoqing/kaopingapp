<template>
	<view class="sd_sdf_dseret">
		<view class="bgs_ddff bgff">


		</view>
		<view class="pr">

			<view class="pd pt40">


				<view class="yj4 dsf_hg_der dx_row ov">
					<view class="dx_col_12 df_sd_dert" @click="sd_sdf(sd)" :class="sd.cls" v-for="sd in sd_dsdf">
						{{sd.name}}
					</view>
				</view>
			</view>
			<view class="mt60">
				<image src="../../static/img/kaoping.jpg" mode="widthFix"  class="w100"></image>
			</view>
			
		</view>

	</view>
</template>
<script>
	export default {
		data() {
			return {
				sd_dsdf: [{
						cls: "act",
						name: "领导班子"
					},
					{
						cls: "",
						name: "员工"
					}
				]
			}
		},
		components: {},
		methods: {
			sd_sdf(sd) {
				this.sd_dsdf.map(a => {
					a.cls = ""
				})
				sd.cls = "act"
			}
		},
		mounted() {},
	}
</script>
<style>

</style>
<style scoped>
	.bgs_ddff {
		position: fixed;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;

	}



	
</style>
