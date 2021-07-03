<template>
	<div class="container">
		<div class="digital-brand-item" v-for="item in digitalBrandData" :key="item.title">
			<div class="digital-brand-title">{{ item.title }}</div>
			<div class="digital-brand">
				<dv-digital-flop class="dv-digital-flop" :config="item.number"/>
				<div class="unit">{{ item.unit }}</div>
			</div>
		</div>
		<dv-decoration-10/>
	</div>
</template>

<script>
import {randomExtend} from "@/utils/random";

export default {
	name: 'Brand',
	data() {
		return {
			digitalBrandData: []
		}
	},
	methods: {
		createData() {
			this.digitalBrandData = [{
				title: 'HUAWEI',
				number: {
					number: [randomExtend(20, 30)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#CE2C24',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'Xiaomi',
				number: {
					number: [randomExtend(20, 30)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#ED732E',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'OPPO',
				number: {
					number: [randomExtend(20, 30)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#2E693D',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'VIVO',
				number: {
					number: [randomExtend(10, 20)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#475DF7',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'Samsung',
				number: {
					number: [randomExtend(5, 10)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#204C9D',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'SONY',
				number: {
					number: [randomExtend(5, 10)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#FFFFFF',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'OnePlus',
				number: {
					number: [randomExtend(5, 10)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#E13229',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'Redmi',
				number: {
					number: [randomExtend(5, 10)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#ED732E',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}, {
				title: 'MEIZU',
				number: {
					number: [randomExtend(5, 10)],
					content: '{nt}',
					textAlign: 'right',
					style: {
						fill: '#3D8BF7',
						fontWeight: 'bold'
					}
				},
				unit: '部'
			}]
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
.container {
	position: relative;
	height: 15%;
	flex-shrink: 0;
	display: flex;
	justify-content: space-between;
	align-items: center;
	background-color: rgba(6, 30, 93, 0.5);

	.dv-decoration-10 {
		position: absolute;
		width: 95%;
		left: 2.5%;
		height: 5px;
		bottom: 0;
	}

	.digital-brand-item {
		width: 11%;
		height: 80%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		border-left: 3px solid rgb(6, 30, 93);
		border-right: 3px solid rgb(6, 30, 93);
	}

	.digital-brand-title {
		font-size: 20px;
		margin-bottom: 20px;
	}

	.digital-brand {
		display: flex;
	}

	.unit {
		margin-left: 10px;
		display: flex;
		align-items: flex-end;
		box-sizing: border-box;
		padding-bottom: 13px;
	}
}

.dv-digital-flop {
	width: 100px;
	height: 50px;
}
</style>
