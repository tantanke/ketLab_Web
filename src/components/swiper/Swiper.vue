<template>
	<div class="swiper">
		<SwiperItem v-for="(item, index) in imgs" :img="item" :key="index" />
	</div>
</template>
<script>
import SwiperItem from "./SwiperItem";

export default {
	name: "Swiper",
	props: {
		imgs: Array,
	},
	methods: {
		onClick() {
			console.log(this.imgs);
		},
	},
	components: {
		SwiperItem,
	},
};
</script>
<style scoped>
.swiper{
    text-align: center;
}
</style>