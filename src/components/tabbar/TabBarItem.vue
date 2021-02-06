<template>
	<div
		class="tab-bar-item"
		@click="onItemClick()"
		:style="isActive == true ? 'color: #1e9fff;' : ''"
	>
		<div
			:class="'iconfont ' + icon + (isMiddle == true ? ' middle' : '')"
		></div>
		<div class="tab-text">{{ msg }}</div>
	</div>
</template>

<script>
export default {
	name: "TabBarItem",
	props: {
		msg: String,
		icon: String,
		isMiddle: Boolean, //居中突出项
		path: String,
	},
	computed: {
		isActive() {
			return this.$route.path === this.path;
		},
	},
	methods: {
		onItemClick() {
			this.$router.replace(this.path).catch(() => {
				//catch捕捉重复点击按钮路由导向当前位置抛出的错误
				//不做处理
			});
		},
	},
};
</script>
<style scoped>
.tab-bar-item {
	flex: 1;
	text-align: center;
	height: 49px;
	vertical-align: middle;
	margin-bottom: 2px;
	color: #393d49;
}

.iconfont {
	font-size: 28px;
}

.middle {
	margin-top: -20px;
	font-size: 40px;
}

.tab-text {
	bottom: 0;
}
</style>