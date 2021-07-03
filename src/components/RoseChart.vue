<template>
	<div id="rose-chart">
		<div class="rose-chart-title">品牌销量分布</div>
		<dv-charts :option="option"/>
	</div>
</template>

<script>
import {randomExtend} from "@/utils/random";

export default {
	name: 'RoseChart',
	data() {
		return {
			option: {}
		}
	},
	methods: {
		createData() {
			this.option = {
				series: [
					{
						type: 'pie',
						radius: '50%',
						roseSort: false,
						data: [
							{name: 'HUAWEI', value: randomExtend(40, 70)},
							{name: 'Xiaomi', value: randomExtend(20, 30)},
							{name: 'OPPO', value: randomExtend(10, 50)},
							{name: 'VIVO', value: randomExtend(5, 20)},
							{name: 'Samsung', value: randomExtend(40, 50)},
							{name: 'SONY', value: randomExtend(20, 30)},
							{name: 'OnePlus', value: randomExtend(5, 10)},
							{name: 'Redmi', value: randomExtend(20, 35)},
							{name: 'MEIZU', value: randomExtend(5, 10)}
						],
						insideLabel: {
							show: false
						},
						outsideLabel: {
							formatter: '{name} {percent}%',
							labelLineEndLength: 20,
							style: {
								fill: '#fff'
							},
							labelLineStyle: {
								stroke: '#fff'
							}
						},
						roseType: true
					}
				],
				color: ['#CE2C24', '#ED732E', '#2E693D', '#475DF7', '#204C9D', '#FFFFFF', '#E13229', '#ED732E', '#3D8BF7']
			}
		},
	},
	mounted() {
		const {createData} = this
		createData()
		setInterval(createData, 30000)
	}
}
</script>

<style lang="less" scoped>
#rose-chart {
	width: 30%;
	height: 100%;
	background-color: rgba(6, 30, 93, 0.5);
	border-top: 2px solid rgba(1, 153, 209, .5);
	box-sizing: border-box;

	.rose-chart-title {
		height: 50px;
		font-weight: bold;
		text-indent: 20px;
		font-size: 20px;
		display: flex;
		align-items: center;
	}

	.dv-charts-container {
		height: calc(~"100% - 50px");
	}
}
</style>
