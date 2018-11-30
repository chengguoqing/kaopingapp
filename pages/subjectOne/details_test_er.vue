<template>
	<view>
		<view class="fz24 pt10 pd pm20 bbm ye bgff">
			<icon class="dx icon-naozhong1"></icon>
			倒计时5分30秒
		</view>
		<view class="pd pt40 bgff pm40">

			<view class="sd_df_dft fz30" v-for="(sd,idx ) in timu">
				<text class="fz26 dsf_df_dsr">单选题</text>
				<text class="fz32 ml10 z3 ln">{{sd.title}}</text>
				({{xz_sd}})
				<view class="pt10">


					<view class="df_jh_ddf z6 mt30" v-for="sf in sd.xx_d" @click="sd_sdf(sd.xx_d,sf)">
						<text class="sd_sdrxcr yj cz" :class="sf.cls">{{sf.num}}</text>
						<text class="ml10">{{sf.name}}</text>
					</view>
				</view>

			</view>


		</view>


		<view class="dsf_jh_drtxrtx btm box pd ">
			<view class="box_a fz28" @click="show=true">
				<icon class="dx icon-gengduo z9"></icon>
				<text class="ml10 ls">2 </text>/10
			</view>
			<view class="box_a tr fz32 ls">
				交卷
			</view>

		</view>


		<van-popup :show="show" position="bottom" :close="onClose" :close-on-click-overlay="is_gnsd">
			<view class="pt20 dx_row">
				<view class="dx_col_4 cen mb20" v-for="sd in sd_mud" @click="dsdf_sddf(sd)">
					<text class="ddf_dfggc" :class="sd.cls">{{sd.num}}</text>
				</view>
			</view>
			
		</van-popup>


	</view>
</template>
<script>
	export default {
		data() {
			return {
				sd_mud:[
					{
						num:1,
						cls:""
					},{
						num:2,
						cls:"act"
					},{
						num:3,
						cls:""
					},{
						num:4,
						cls:""
					},{
						num:5,
						cls:""
					},{
						num:6,
						cls:""
					},{
						num:7,
						cls:""
					},{
						num:8,
						cls:""
					},{
						num:9,
						cls:""
					},{
						num:10,
						cls:""
					}
				],
				xz_sd: "B",
				show:false,
				is_gnsd:false,
				timu: [{
					title: "李某在参加机试时大声喧哗，被领导批评进行10元违约金处罚，李某的行为违反了",
					xx_d: [{
						num: "A",
						cls: "",
						name: "标准化与组织纪律规章制度"
					}, {
						num: "B",
						cls: "act",
						name: "分之合经营管理暨阿米巴"
					}, {
						num: "C",
						cls: "",
						name: "3S现场管理"
					}, {
						num: "D",
						cls: "",
						name: "管理环"
					}]
				}]
			}
		},
		components: {},
		methods: {
			onClose(){
				this.show=false
			},
			sd_sdf(sd, sf) {
				sd.map(a => {
					a.cls = ""
				})
				this.xz_sd = sf.num
				sf.cls = "act"
			},
			dsdf_sddf(sd){
				this.sd_mud.map(a=>{
					a.cls=""
				})
				sd.cls="act"
				this.show=false
			}
		},
		mounted() {},
	}
</script>
<style scoped>
	.dsf_df_dsr {
		display: inline-block;
		width: 103upx;
		height: 37upx;
		line-height: 37upx;
		text-align: center;
		color: #489CF3;
		border: 1px solid #489CF3;
	}

	.sd_sdrxcr {
		width: 51upx;
		height: 51upx;
		display: inline-block;
		text-align: center;
		line-height: 51upx;
		border: 1px solid #F4F3F2;
	}

	.sd_sdrxcr.act {
		color: #fff;
		border: 1px solid #489CF3;

		background: #489CF3;
	}

	.dsf_jh_drtxrtx {
		position: fixed;
		left: 0;
		bottom: 0;
		width: 100%;
		background: #fff;
		height: 95upx;
		line-height: 95upx;
	}
	.ddf_dfggc{
		width: 90upx;
		height: 90upx;
		border: 1px solid #E5F1F9;
		text-align: center;
		font-size: 32upx;
		line-height: 90upx;
		border-radius: 50%;
		display: inline-block;
	}
	.ddf_dfggc.act{
		background: #459cf3;
		color: #fff;
	}
</style>
