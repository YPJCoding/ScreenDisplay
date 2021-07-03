<template>
  <div class="home">
	  <FullScreenContainer></FullScreenContainer>
  </div>
</template>

<script>
import FullScreenContainer from "@/components/FullScreenContainer";
export default {
  name: 'Home',
	data(){
  	return{}
	},
  components: {
	  FullScreenContainer
  },
	mounted() {
		document.title = "Android手机综合数据"
	},
	methods:{

	}
}
</script>
<style lang="less" scoped>
.home{
	width: 100%;
	height: 100%;
	background-color: #030409;
	color: #fff;
}
</style>
