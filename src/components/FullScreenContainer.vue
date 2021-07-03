<template>
	<div class="container">
		<dv-full-screen-container>
			<dv-loading v-if="loading">Loading...</dv-loading>
			<template v-else>
				<!--头部-->
				<HeaderTitle></HeaderTitle>
				<!--品牌-->
				<div class="main-content">
					<Brand></Brand>
					<div class="block-left-right-content">
						<PerformanceRanking></PerformanceRanking>
						<div class="block-top-bottom-content">
							<div class="block-top-content">
								<RoseChart/>
								<WaterLevelChart/>
								<ScrollBoard/>
							</div>
							<Cards/>
						</div>
					</div>
				</div>

			</template>
		</dv-full-screen-container>
	</div>
</template>

<script>
import HeaderTitle from "@/components/HeaderTitle";
import Brand from "@/components/Brand";
import PerformanceRanking from "@/components/PerformanceRanking";
import RoseChart from "@/components/RoseChart";
import WaterLevelChart from "@/components/WaterLevelChart";
import ScrollBoard from "@/components/ScrollBoard";
import Cards from "@/components/Cards";

export default {
	name: "FullScreenContainer",
	data() {
		return {
			loading: true
		}
	},
	components: {
		HeaderTitle, Brand, PerformanceRanking, RoseChart, WaterLevelChart, ScrollBoard, Cards
	},
	mounted() {
		setTimeout(() => {
			this.loading = false
		}, 1500)
	},
}
</script>

<style lang="less" scoped>
.container {
	#dv-full-screen-container {
		background-image: url('../assets/bg.png');
		background-size: 100% 100%;
		box-shadow: 0 0 3px blue;
		display: flex;
		flex-direction: column;
	}

	.main-content {
		flex: 1;
		display: flex;
		flex-direction: column;
	}

	.block-left-right-content {
		flex: 1;
		display: flex;
		margin-top: 20px;
	}

	.block-top-bottom-content {
		flex: 1;
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
		padding-left: 20px;
	}

	.block-top-content {
		height: 55%;
		display: flex;
		flex-grow: 0;
		box-sizing: border-box;
		padding-bottom: 20px;
	}
}
</style>
