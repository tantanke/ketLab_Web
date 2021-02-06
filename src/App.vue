<template>
	<div id="app">
		<tab-bar>
			<tab-bar-item msg="首页" icon="icon-home" path="/"></tab-bar-item>
			<tab-bar-item
				msg="扫一扫"
				icon="icon-camera"
				:isMiddle="true"
				path="/scan"
			></tab-bar-item>
			<tab-bar-item
				msg="我的"
				icon="icon-profile"
				path="/profile"
			></tab-bar-item>
		</tab-bar>
		<keep-alive>
			<router-view />
		</keep-alive>
	</div>
</template>

<script>
import "@/assets/iconfont/iconfont.css";
import TabBar from "./components/tabbar/TabBar";
import TabBarItem from "./components/tabbar/TabBarItem";

export default {
	name: "App",
	components: {
		TabBar,
		TabBarItem,
	},
};
</script>

<style lang="scss">
@import "@/css/index.scss";
</style>
