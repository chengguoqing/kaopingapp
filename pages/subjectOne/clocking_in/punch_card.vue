<template>
	<view class="bgff pm100">
		<view class="pt20 pm20 fz30 pd">
			2018年10月19日
		</view>
		<view class="map_dituer">
			<map style="width: 100%; height: 100%;" :latitude="latitude" :longitude="longitude" :markers="covers">
			</map>
		</view>
		<view class="pd pt20 fz32 z3 ln">
			当前位置：海口市迎宾路棕榈公寓
			<view class="fz28 ls">
				<text class="dian_ddf f_b cz yj"></text>
				上班时间：8:00
			</view>
			<navigator url="" class="sh_dakai_e cen cf ln yj">
				<view class="fz48 ">
					上班打卡
				</view>
				<view class="fz28 ">
					07:50:00<br>
					正常状态
				</view>

			</navigator>


		</view>

		<!-- 右上角的菜单 -->
		<view class="yopushangjiao fz30" v-if="is_kh_d">
			<view class="fkiy_list cf">
				<icon class="dx icon-shezhi fz40 cz"></icon>
				<text class="cz">公休日设置</text>
			</view>
			<view class="fkiy_list cf ab">
				<icon class="dx icon-jilu fz36 cz"></icon>
				<text class="cz">打卡记录</text>
			</view>
		</view>


	</view>
</template>
<script>
	export default {
		data() {
			return {
				title: 'map',
				is_kh_d: false,
				latitude: 39.909,
				longitude: 116.39742,
				covers: [{
					latitude: 39.909,
					longitude: 116.39742,
					iconPath: '/static/img/map_ww.png'
				}, {
					latitude: 39.90,
					longitude: 116.39,
					iconPath: '/static/img/map_ww.png'
				}]
			}
		},
		components: {},
		methods: {},
		mounted() {},
		onNavigationBarButtonTap() {
			// this.is_kh_d = true

			uni.showActionSheet({
				itemList: ['公休日设置', '打卡记录'],
				success: function(res) {
					
				},
				fail: function(res) {
					
				}
			});


		}
	}
</script>
<style scoped>
	.map_dituer {
		height: 400upx;
	}

	.dian_ddf {
		width: 18upx;
		height: 18upx;
		background: #489FF6;
	}

	.sh_dakai_e {
		width: 260upx;
		height: 260upx;
		background: #489FF6;
		margin: auto;
		margin-top: 35upx;
		padding-top: 80upx;
	}

	.yopushangjiao {
		position: fixed;
		right: 0;
		top: 0px;
		width: 245upx;
		z-index: 10000;
		background: #67B7F9;
	}

	.fkiy_list {
		line-height: 80upx;
		padding-left: 20upx;
	}

	.fkiy_list.ab {
		border-top: 1px solid #55A9F7;
	}
</style>
