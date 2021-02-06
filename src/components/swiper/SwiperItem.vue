<template>
	<div>
		<img :src="img.src" alt="img.title" class="swiper-item" />
	</div>
</template>
<script>
export default {
	name: "SwiperItem",
	props: {
		img: Object,
	},
};
</script>
<style>
.swiper-item {
	width: 80%;
    display: inline-block;
}
</style>