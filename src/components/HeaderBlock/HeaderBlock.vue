<template>
	<div class="header">
		<div class="header__container">
			<router-link to="/" class="header__logo">
				<img src="@/assets/logo.svg" alt="gitpod" />
			</router-link>
			<div class="header__nav" :class="{ 'is-active': isActive }" @click="isActive = false">
				<div class="header__li">
					<router-link to="/">Features</router-link>
				</div>
				<div class="header__li">
					<router-link to="/">Pricing</router-link>
				</div>
				<div class="header__li">
					<router-link to="/">Blog</router-link>
				</div>
				<div class="header__li">
					<router-link to="/">Docs</router-link>
				</div>
				<div class="header__li">
					<router-link to="/">Changelog</router-link>
				</div>
				<div class="header__li element-mark">
					<router-link to="/">We're hiring</router-link>
				</div>
				<div class="header__close" @click="isActive = false">
					<CloseIcon />
				</div>
			</div>
			<div class="header__burger" v-if="!isActive" @click="isActive = !isActive">
				<MenuIcon />
			</div>
			<div class="header__btn">
				<router-link to="/">Login</router-link>
			</div>
		</div>
	</div>
</template>

<script>
import MenuIcon from "vue-material-design-icons/Menu.vue";
import CloseIcon from "vue-material-design-icons/Close.vue";
export default {
	name: "HeaderBlock",
	data() {
		return {
			isActive: false,
		};
	},
	components: {
		MenuIcon,
		CloseIcon,
	},
};
</script>

<style lang="scss" scoped>
@import '@/components/HeaderBlock/HeaderBlock.scss';
</style>
