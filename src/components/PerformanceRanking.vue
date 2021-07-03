<template>
	<div class="container">
		<div class="ranking-title">性能排行</div>
		<dv-scroll-ranking-board class="scroll-ranking" :config="config"/>
	</div>
</template>

<script>
export default {
	name: 'PerformanceRanking',
	data() {
		return {
			config: {
				data: [{
					name: '一加手机9 Pro',
					value: 824459
				}, {
					name: 'OPPO Find X3 Pro',
					value: 818689
				}, {
					name: 'vivo X60 Pro+',
					value: 811808
				}, {
					name: '一加手机9',
					value: 810916
				}, {
					name: '小米11 Ultra',
					value: 757379
				}, {
					name: '魅族18',
					value: 692292
				}, {
					name: 'Redmi K40 Pro+',
					value: 684648
				}, {
					name: '三星Galaxy S21 Ultra 5G',
					value: 663375
				}, {
					name: '小米10 至尊纪念版',
					value: 526211
				}],
				rowNum: 9
			}
		}
	}
}
</script>

<style lang="less" scoped>
.container {
	width: 20%;
	box-shadow: 0 0 3px blue;
	display: flex;
	flex-direction: column;
	background-color: rgba(6, 30, 93, 0.5);
	border-top: 2px solid rgba(1, 153, 209, .5);
	box-sizing: border-box;
	padding: 0 30px;

	.ranking-title {
		font-weight: bold;
		height: 50px;
		display: flex;
		align-items: center;
		font-size: 20px;
	}

	.scroll-ranking {
		flex: 1;
		width: 100%;
		height: 100%;
		color: #fff;
	}
}
</style>
