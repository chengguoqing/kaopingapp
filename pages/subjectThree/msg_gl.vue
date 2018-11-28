<template>
	<view>
		<van-tabs>
			<van-tab title="全部" sticky swipeable>
				<view class="pd pt20 pm20 bgff bbm" v-for="sd in 10">
					<view class="box">
						<view class="box_b fz32">
							申述
						</view>
						<view class="box_a fz30 z9 fz26 tr">
							10/25 8:00
						</view>
					</view>
					<view class="fz26 z6">
						你收到一条申诉
					</view>
				</view>

			</van-tab>
			<van-tab title="未读">
				<view class="pd pt20 pm20 bgff bbm" v-for="sd in 2">
					<view class="box">
						<view class="box_b fz32">
							申述
						</view>
						<view class="box_a fz30 z9 fz26 tr">
							10/25 8:00
						</view>
					</view>
					<view class="fz26 z6">
						你收到一条申诉
					</view>
				</view>
			</van-tab>
			<van-tab title="已读">
				<view class="pd pt20 pm20 bgff bbm" v-for="sd in 5">
					<view class="box">
						<view class="box_b fz32">
							申述
						</view>
						<view class="box_a fz30 z9 fz26 tr">
							10/25 8:00
						</view>
					</view>
					<view class="fz26 z6">
						你收到一条申诉
					</view>
				</view>
			</van-tab>
		</van-tabs>



	</view>
</template>
<script>
	export default {
		data() {
			return {}
		},
		components: {},
		methods: {},
		mounted() {},
	}
</script>
<style scoped></style>
