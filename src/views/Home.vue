<template>
	<div class="home">
		<div class="top-bar">
			<span class="search-box iconfont icon-search">搜索</span>
		</div>
		<Swiper :imgs="imgs" />
	</div>
</template>

<script>
import Swiper from "../components/swiper/Swiper.vue";
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
	name: "Home",
	components: { Swiper },
	data() {
		return {
			imgs,
		};
	},
};
import pic1 from "@/assets/img/1.jpg";
let imgs = [
	{
		title: "test",
		src: pic1,
	},
	{
		title: "test",
		src: pic1,
	},
	{
		title: "test",
		src: pic1,
	},
];
</script>

<style lang="scss" scoped>
.top-bar {
	display: inline-block;
	width: 100%;
	height: 50px;
	line-height: 50px;
	text-align: center;
	background-color: #409eff;
}

.search-box {
	display: inline-block;
	width: 80%;
	height: 35px;
	line-height: 35px;
	text-align: center;
	background-color: white;
	color: gray;
	border-radius: 20px;
}
</style>