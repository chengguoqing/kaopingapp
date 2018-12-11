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
			
			
			<view class="yj4 bgff ov mt20" v-for="sd in sd_xddf">
				<view class="box pt20 pm10  pd" :class="sd.name" @click="sd.cls?sd.cls='':sd.cls='act'">
					<view class="box_b fz32">
						海口分公司  <text class="ml10">15000</text>
					</view>
					<view class="box_a tr">
						<icon class="dx icon-up1" :class="sd.cls?'dsfe_dfrtertggtty':''"></icon>
					</view>
				</view>
				<view class="" v-if="sd.cls">
					
			
				<view class="pd pt20 pm20 box fz30 btm">
					<view class="box_b  z6">
						软件事业部
					</view>
					<view class="box_a  ls tr">
						100000
					</view>
				</view>
				
				<view class="pd pt20 pm20 box fz30 btm">
					<view class="box_b  z6">
						咨询事业部
					</view>
					<view class="box_a  ls tr">
						100000
					</view>
				</view>
				
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
				date_d:[1,2,3,4,5,6],
				sd_xddf:[
					{
						cls:"act",
						name:"bglscf"
					},
					{
						cls:"act",
						name:"sd_r_dert"
					},
					{
						cls:"act",
						name:"bglscf"
					}
				]
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
	.dsfe_dfrtertggtty{
		transform: rotate(180deg);
	}
	.ssd_dffgxc{
		width: 310upx;
		height: 65upx;
		line-height: 65upx;
		border: 1px solid #F4F4F4;
		border-radius: 40upx;
	}
	.ssd_dffgxc input{
		padding-left: 20upx !important;
		margin-top: 6upx;
		font-size: 30upx;
	}
	.ssd_dffgxc icon{
		position: absolute;
		right: 20upx;
		top: 0upx;
	}
	
	
	.huang_dsdet{
		width: 560upx;
		height: 560upx;
		margin:auto;
		margin-top: 20upx;
	}
	.sd_r_dert{
		background: #FB9B69;
		color: #fff;
	}
</style>
