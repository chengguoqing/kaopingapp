<template>
	<view>
		<view class="pd pt20 pm20 bgff"> 
			<view class="box">
				<view class="box_a ls fz30">
					 <picker class="picker-item" mode="date"  @change="dateChange" end="2020-01-01" start="2010-01-01">
					        
								 {{time}} <icon class="dx icon-down"></icon>
					
					        </picker>
				</view>
				<view class="box_a tr">
					<view class="ssd_dffgxc pr f_b tl">
						<input type="text" placeholder="搜索人名" />
						<icon class="dx icon-sousuo z9"></icon>
					</view>

				</view>
			</view>

			<view class="huang_dsdet">
				<huanxing canvasId="piexe" :date_d='date_d' tet_m='date_d'></huanxing>
			</view>
		</view>

		<view class="pd">
			<view class="pd pt20 pm20 fz32">
				海口分公司-软件事业部
			</view>
			<view class="pd pt20 pm20 bgff yj4 mb20" v-for="sd in 10">
				<image src="../../static/img/user_icon.png" class="yj user_iu_der fl"></image>
				<view class="ov pl20">
					<view class="fz32">
						独行工匠 <text class="fz30 fr">10000</text>
						<view class="qc fz28 z9 pt10">
							开发架构师
						</view>
					</view>
				</view>
				<view class="qc">

				</view>

			</view>


		</view>


	</view>
</template>
<script>
	import huanxing from "../../components/huanxing.vue"
	export default {
		data() {
			return {
				time:"2018年10月",
				date_d:[1,2,3,4,5,6]
			}
		},
		components: {
			huanxing
		},
		methods: {
			dateChange(evt){
				let date_e=evt.detail.value.split("-")
				this.time = date_e[0]+"年"+date_e[1]+"月";
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.ssd_dffgxc {
		width: 310upx;
		height: 65upx;
		line-height: 65upx;
		border: 1px solid #F4F4F4;
		border-radius: 40upx;
	}

	.ssd_dffgxc input {
		padding-left: 20upx !important;
		margin-top: 6upx;
		font-size: 30upx;
	}

	.ssd_dffgxc icon {
		position: absolute;
		right: 20upx;
		top: 0upx;
	}


	.huang_dsdet {
		width: 560upx;
		height: 560upx;
		margin: auto;
		margin-top: 20upx;
	}

	.sd_r_dert {
		background: #FB9B69;
		color: #fff;
	}

	.user_iu_der {
		width: 100upx;
		height: 100upx;
	}
</style>
