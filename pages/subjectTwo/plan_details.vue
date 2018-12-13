<template>
	<view>

		<view class=" pd bgff pt20 pm20 dx_row" @click="dsf_s_a?dsf_s_a=false:dsf_s_a=true">
			<view class="sd_jh_deert f_b cz">
				<view class="dsf_gouxuan cz">
					<icon class="dx icon-check cz df_c_ertx" :class="dsf_s_a?'act':''"></icon>
				</view>
			</view>
			<view class="f_b fz32 z3 cz">
				定内部交易价值链与SST合同(web端)
			</view>
		</view>

		<view class="mt20">

			<view class=" pd bgff gfh_jh_dertt dx_row pr">
				<view class="df_df_ertxc f_b cz">
					<icon class="dx icon-user fz40  z6"></icon>
				</view>
				<view class="f_b fz30 z3 cz pr">
					<text class="z6">负责人</text>
				</view>
				<view class="right_ert">
					<text class="sd_drrtxc">刘</text>
					<text class="sd_drrtxc">陈</text>
					<icon class="dx icon-right"></icon>
				</view>
			</view>
			<view class=" pd bgff  dx_row pr gfh_jh_dertt btm">
				<view class="df_df_ertxc f_b cz">
					<icon class="dx icon-naozhong fz40  z6"></icon>
				</view>
				<view class="f_b fz30 z3 cz pr">
					<text class="z6">截止时间</text>
				</view>
				<view class="right_ert fz26 z6">
					<!-- <text class="fz26 z6">201年10月1日</text>
					<icon class="dx icon-right"></icon> -->
					<picker class="picker-item" mode="date" @change="dateChange" end="2020-01-01" start="2010-01-01">

						{{time}}
						<icon class="dx icon-down"></icon>

					</picker>

				</view>
			</view>

			<view class=" pd bgff  dx_row pr gfh_jh_dertt btm">

				<view class="df_df_ertxc f_b cz">
					<icon class="dx icon-icon-- fz40  z6"></icon>
				</view>
				<view class="f_b fz30 z3 cz pr">
					<text class="z6">状态</text>
				</view>
				<view class="right_ert">
					<picker class="picker-item " mode="selector" :range="textList" @change="textChange">

						<text class="fz26 z6">{{textList[textValue]}}</text>
						<icon class="dx icon-right"></icon>
					</picker>

				</view>






			</view>




			<view class=" pd bgff  dx_row pr pt20 btm">
				<view class="df_df_ertxc fl cz">
					<icon class="dx icon-gengduo-2 fz40  z6"></icon>
				</view>
				<view class="ov fz30 z3 cz pr dian ln pl10">
					<view class="sd_oiu_row mb10" v-for="(sd,idx) in jiancs" @click="gx_sdf(sd)">
						<view class="dsf_gouxuan cz f_b">
							<icon class="dx icon-check cz df_c_ertx" :class="sd.cls"></icon>
						</view>
						<view class="f_b fz30 z3 cz ml10" :class="sd.cls=='act'?'del_x':''">
							{{idx+1}}.{{sd.name}}
						</view>
					</view>


					<view class="sd_oiu_row mb10" @click="add_xz_e" v-if="!is_tji">


						<icon class="dx icon-add fz40 ls cz"></icon>
						<view class="f_b fz30 ls cz ml10">
							点击添加检查项
						</view>
					</view>

					<view class="sd_oiu_row mb10" v-else>


						<icon class="dx icon-add fz40 ls cz fl"></icon>
						<view class="ov fz30 z3 cz ml10">
							<textarea placeholder="请输入" class="fz26 sdf_kjh_dfrt" rows="3"  v-model="nmn_sdff"/>
							</view>
						<view class="qc tr ">
							<view class="sdfsd_df_Drtt" @click="is_tji=false">
								取消
							</view>
							<view class="sdfsd_df_Drtt ab" @click="querener">
								确认
							</view>
						</view>
						
					</view>




				</view>

			</view>





		</view>


		<view class="mt20 pd pt20 bgff">
			<view class="fz32 z3">
				评论
			</view>

			<view class="mt20">
				<text class="sd_drrtxc fl">刘</text>
				<view class="ov pl20">
					<view class="box">
						<view class="box_a fz32 z3">
							刘峰
						</view>
						<view class="box_a tr fz26 z9">
							2018-10-25 14:25
						</view>
					</view>

					<view class="mt10 fz30 z6 ln pm20">
						内容啊内容啊内容啊内容啊内容啊内容啊内容啊内容啊内容啊内容啊内容啊
					</view>

				</view>
				<view class="qc">

				</view>
			</view>
		</view>



		<view class="pd sdf_dfrtd mt40">
			<view class="dx_row  yj4 ov bgff">

				<view class="bjhg_sddf fr">
					评论
				</view>
				<view class="ov df_dertxfcrdr pd">
					<input type="text" placeholder="我来说几句" />
				</view>
			</view>
		</view>


	</view>
</template>
<script>
	export default {
		data() {
			return {
				textList: [
					'进行中',
					'进行中1',
					'进行中2'
				],
				textValue: 0,
				nmn_sdff:"",
				dsf_s_a: false,
				jiancs: [{
					name:"项目分条完成情况，完成打钩",
					cls: "act"
				}, {
					name:"项目分条完成情况，完成打钩",
					cls: ""
				}, {
					name:"项目分条完成情况，完成打钩",
					cls: ""
				}],
				is_tji:false,
				time: "2018年10月1日",
			}
		},
		components: {},
		methods: {
			textChange(evt) {
				this.textValue = evt.detail.value;
			},
			dateChange(evt) {
				let date_e = evt.detail.value.split("-")
				this.time = date_e[0] + "年" + date_e[1] + "月" + date_e[2] + "日";
			},
			add_xz_e() {
				this.is_tji=true
			
			},
			querener(){
				if(!this.nmn_sdff){
					uni.showToast({
						title:"请输入内容",	
						icon:"none"
					})
					return
				}
				this.jiancs.push({
					name:this.nmn_sdff,
					cls:""
				})
				this.is_tji=false
			},
			gx_sdf(sd) {
				if (sd.cls) {
					sd.cls = ""
				} else {
					sd.cls = "act"
				}
			}
		},
		mounted() {

		},
	}
</script>
<style scoped>
	.df_derr_frrtt {
		position: absolute;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
		z-index: 1000;
		background: red;
	}
	.sdf_kjh_dfrt{
		width: 100%;
		border: 0px;
		padding: 10upx;
	}
	.sdfsd_df_Drtt{
		display: inline-block;
		width: 150upx;
		height: 60upx;
		line-height: 60upx;
		text-align: center;
		border: 1px solid #666;
		color: #666;
		font-size: 28upx;
		margin-left: 20upx;
		border-radius: 8upx;
		}
.sdfsd_df_Drtt.ab{
	background: #449EF6;
	color: #fff;
	border: 1px solid #449EF6;
}
</style>
