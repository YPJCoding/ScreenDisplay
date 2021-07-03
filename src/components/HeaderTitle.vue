<template>
	<div class="container" @click="screenFullClick">
		<dv-decoration-8 class="header-left"/>
		<dv-decoration-5 class="header-center"/>
		<dv-decoration-8 class="header-right" :reverse="true"/>
		<div class="center-title">Android手机综合数据</div>
	</div>
</template>

<script>
import screenFull from "screenfull";

export default {
	name: "Header",
	data() {
		return {}
	},
	methods: {
		screenFullClick() {
			screenFull.toggle()
		}
	}
}
</script>

<style lang="less" scoped>
.container {
	display: flex;
	justify-content: space-between;
	position: relative;
	width: 100%;
	height: 100px;
	flex-shrink: 0;
}

.header-center {
	width: 40%;
	height: 60px;
	margin-top: 30px;
}

.header-left, .header-right {
	width: 25%;
	height: 60px;
}

.center-title {
	position: absolute;
	font-size: 30px;
	font-weight: bold;
	left: 50%;
	top: 15px;
	transform: translateX(-50%);
}
</style>
