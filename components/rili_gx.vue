<!-- 公休 -->
<template>
	<view class="pm20">

		<view>
			<view class="month" v-if="sd_h_d==42">

				<view class="pd pt40 pm20">

					<view class="cen fz28">

						<image src="/static/img/left.png" class="sdf_deert mr40 cz" @click="pickPre(currentYear,currentMonth)"></image>

						<text class="cz">{{ currentYear }}年 {{ currentMonth }}月</text>

						<image src="/static/img/right.png" class="sdf_deert ml40 cz" @click="pickNext(currentYear,currentMonth)"></image>

					</view>
				</view>
			</view>
			<view class="weekdays fz28">
				<text>一</text>
				<text>二</text>
				<text>三</text>
				<text>四</text>
				<text>五</text>
				<text style="color:red">六</text>
				<text style="color:red">日</text>
			</view>

			<view class="days pm20">
				<view @click="pick(day)" v-for="(day,idx) in days" class="sd_dfderrt fz28" >

					<text class="yj sdf_jh_drtx " :class="day.isjintian">{{day.riqi}}</text>

					<text class="dian_drtxc ls fz22" v-if="day.is_dian%3==0">公休</text>

				</view>
			</view>
			
			
			
			
			





		</view>

		<view class="cen bgff" v-if="is_down">
			<view class="yj br dsf_jh_deerttx f_b" :class="sd_h_d==7?'':'act'" @click="zankai_er">
				<image src="/static/img/down.png"></image>
			</view>
		</view>







	</view>
</template>
<script>
	export default {
		props: {
			is_ddf: "",
			is_down:""
		},
		data() {
			return {
				currentDay: 1,
				currentMonth: 1,
				currentYear: 1970,
				currentWeek: 1,
				days: [],
				sd_h_d: 42
			}
		},
		components: {},
		methods: {
			df_dsdrtxc() {
				if (this.sd_h_d == 7) {
					this.sd_h_d = 42
					var d = new Date();
					this.initData(this.formatDate(d.getFullYear(), d.getMonth() + 1, 1), this.sd_h_d);
				} else {
					this.sd_h_d = 7
					var d = new Date();
					this.initData(null, this.sd_h_d);
				}
			},
			initData: function(cur, ide) {
				var date;
				if (cur) {
					date = new Date(cur);
				} else {
					date = new Date();
				}
				this.currentDay = date.getDate();
				this.currentYear = date.getFullYear();
				this.currentMonth = date.getMonth() + 1;
				this.currentWeek = date.getDay(); // 1...6,0
				if (this.currentWeek == 0) {
					this.currentWeek = 7;
				}
				var str = this.formatDate(this.currentYear, this.currentMonth, this.currentDay);
				console.log("today:" + str + "," + this.currentWeek);
				this.days.length = 0;
				// 今天是周日，放在第一行第7个位置，前面6个
				for (var i = this.currentWeek - 1; i >= 0; i--) {
					var d = new Date(str);
					d.setDate(d.getDate() - i);
					console.log("y:" + d.getDate());
					let sd_sdf = {}
					sd_sdf.riqi = d.getDate()
					sd_sdf.isjintian = ""
					sd_sdf.is_dian = Math.ceil(Math.random() * 20)
					if (d.getFullYear() == new Date().getFullYear() && d.getMonth() == new Date().getMonth() && d.getDate() == new Date()
						.getDate()) { //是否为今天
						sd_sdf.isjintian = "act"
					}

					this.days.push(sd_sdf);
				}
				for (var i = 1; i <= ide - this.currentWeek; i++) {
					var d = new Date(str);
					d.setDate(d.getDate() + i);
					let sd_sdf = {}
					sd_sdf.riqi = d.getDate()
					sd_sdf.isjintian = ""
					sd_sdf.is_dian = Math.ceil(Math.random() * 20)
					if (d.getFullYear() == new Date().getFullYear() && d.getMonth() == new Date().getMonth() && d.getDate() == new Date()
						.getDate()) { //是否为今天
						sd_sdf.isjintian = "act"
					}
					this.days.push(sd_sdf);
				}
			},
			pick: function(date) {
				if(date.isjintian){
					date.isjintian=""
				}else{
					date.isjintian="act"
				}
			},
			pickPre: function(year, month) {
				// setDate(0); 上月最后一天
				// setDate(-1); 上月倒数第二天
				// setDate(dx) 参数dx为 上月最后一天的前后dx天
				var d = new Date(this.formatDate(year, month, 1));
				d.setDate(0);
				this.initData(this.formatDate(d.getFullYear(), d.getMonth() + 1, 1), this.sd_h_d);
			},
			pickNext: function(year, month) {
				var d = new Date(this.formatDate(year, month, 1));
				d.setDate(35);
				this.initData(this.formatDate(d.getFullYear(), d.getMonth() + 1, 1), this.sd_h_d);
			},
			pickYear: function(year, month) {
				alert(year + "," + month);
			},

			// 返回 类似 2016-01-02 格式的字符串
			formatDate: function(year, month, day) {
				var y = year;
				var m = month;
				if (m < 10) m = "0" + m;
				var d = day;
				if (d < 10) d = "0" + d;
				return y + "-" + m + "-" + d
			},
			zankai_er() {
				var d = new Date();
			d.setDate(0);

				if(this.sd_h_d==7){
					this.sd_h_d = 42
					this.initData(this.formatDate(d.getFullYear(), d.getMonth() + 2, 1), this.sd_h_d);
				}else{
					this.sd_h_d = 7
					this.initData(null, this.sd_h_d);

				}
				try{
					this.$emit('sddffff')
				}catch(e){
					
				}
				
			
				
			}
		},
		onLoad: function() {
			var d = new Date();
			d.setDate(0);
			if (this.is_ddf) {
				this.sd_h_d=7
				this.initData(null, this.sd_h_d);
				return
			}
			this.initData(this.formatDate(d.getFullYear(), d.getMonth() + 2, 1), this.sd_h_d);
				
			     
			
		},
		mounted() {




		},
	}
</script>
<style scoped>
	.sdf_deert {
		width: 36upx;
		height: 36upx;
	}

	#calendar {
		margin: 0 auto;
	}

	.month {
		width: 100%;
		background: #fff;
	}

	.month ul {
		margin: 0;
		padding: 0;
		display: flex;
		justify-content: space-between;
	}

	.year-month {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-around;
	}

	.year-month span {
		color: #333 !important;
		font-size: 16px !important;
	}

	.year-month:hover {
		background: rgba(150, 2, 12, 0.1);
	}

	.choose-year {
		padding-left: 20px;
		padding-right: 20px;
	}

	.choose-month {
		text-align: center;
	}

	.arrow {
		width: 40upx;
		border: 1px solid red;
		text-align: center;
	}

	.arrow:hover {
		background: rgba(100, 2, 12, 0.1);
	}

	.month ul li {
		color: white;
		font-size: 16px;
		text-transform: uppercase;
		letter-spacing: 3px;
		color: #333;
		padding: 0px;
	}

	.weekdays {
		margin: 0;
		padding: 10px 0;
		background-color: #fff;
		display: flex;
		flex-wrap: wrap;
		color: #FFFFFF;
		justify-content: space-around;
	}

	.weekdays text {
		display: inline-block;
		width: 13.6%;
		color: #999 !important;
		text-align: center;
	}

	.days {
		padding: 0;
		background: #FFFFFF;
		margin: 0;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-around;
	}

	.days li {
		list-style-type: none;
		display: inline-block;
		width: 14.2%;
		text-align: center;
		padding-bottom: 15px;
		padding-top: 15px;
		font-size: 1rem;
		color: #000;
	}

	.days li .active {
		padding: 4px 4px;
		border-radius: 50%;
		background: #F09CAD;
		color: #fff;
	}

	.days li .other-month {
		padding: 5px;
		color: gainsboro;
	}

	.days li:hover {
		background: #e1e1e1;
	}

	.dsf_jh_drertx {
		width: 160px;
		margin: auto !important;
		padding-top: 10px !important;
		padding-bottom: 10px !important;
	}

	.sd_dfderrt {
		width: 13.6%;
		float: left;
		text-align: center;
		height: 90upx;
	}

	.sdf_jh_drtx {
		width: 60upx;
		height: 60upx;
		color: #666;
		text-align: center;
		line-height: 60upx;
		display: inline-block;
	}

	.sdf_jh_drtx.act {
		background: #489FF7;
		color: #fff;
	}

	.dian_drtxc {
		display: block;
		margin: auto;
	}

	.f_b {
		display: inline-block !important;
	}

	.dsf_jh_deerttx {
		width: 50upx;
		height: 50upx;
	}
	.dsf_jh_deerttx image{
		width: 100%;
		height: 100%;
	}
	.dsf_jh_deerttx.act{
		transform: rotate(180deg);
	}
	.xuanss{
		transform: rotate(180deg);
	}
</style>
