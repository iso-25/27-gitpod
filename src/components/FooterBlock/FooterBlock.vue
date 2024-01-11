<template>
	<div class="footer">
		<div class="footer__container">
			<div class="footer__links">

				<div class="footer__nav" v-for="(site, siteIndex) in  sites" :key="siteIndex">
					<router-link v-for="(item, index) in site" :key="index" :to="item.url" class="footer__li"
						:class="[{ 'first-element-class': index === 0 }, { 'element-mark': item.isMark }]">
						{{ item.name }}
					</router-link>
				</div>

			</div>
			<div class="footer__socials">
				<div class="footer__logo">
					<img class="footer__logo-img" src="@/assets/frame-logo.svg" alt="Logo">
					<div class="footer__logo-txt">
						Copyright &copy;<span class="footer__logo-year">{{ getCurrentYear() }}</span>Gitpod
					</div>
				</div>
				<div class="footer__link">
					<img src="@/assets/frame-twitter.svg" alt="Twitter">
					<img src="@/assets/frame-git.svg" alt="Git">
					<img src="@/assets/frame-other.svg" alt="Other">
				</div>

			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "FooterBlock",
	data() {
		return {
			sites: [
				[
					{ name: "Gitpod", url: "/", isMark: false },
					{ name: "Home", url: "/", isMark: false },
					{ name: "Features", url: "/", isMark: false },
					{ name: "Pricing", url: "/", isMark: false },
					{ name: "Changelog", url: "/", isMark: false },
					{ name: "Self-Hosted", url: "/", isMark: false },
					{ name: "Gitpod vs GitHub Codespaces", url: "/", isMark: false },
					{ name: "Status", url: "/" },
				],
				[
					{ name: "Developer", url: "/", isMark: false },
					{ name: "Getting started", url: "/", isMark: false },
					{ name: "Screencasts", url: "/", isMark: false },
					{ name: "Blog", url: "/", isMark: false },
					{ name: "Documentation", url: "/", isMark: false },
					{ name: "Report a bug", url: "/", isMark: false },
					{ name: "Community", url: "/", isMark: false },
				],
				[
					{ name: "Company", url: "/", isMark: false },
					{ name: "About", url: "/", isMark: false },
					{ name: "Careers", url: "/", isMark: true },
					{ name: "Contact", url: "/", isMark: false },
					{ name: "Media Kit", url: "/", isMark: false },
				],
				[
					{ name: "Legal", url: "/", isMark: false },
					{ name: "Imprint", url: "/", isMark: false },
					{ name: "Terms of Service", url: "/", isMark: false },
					{ name: "Privacy Policy", url: "/", isMark: false },
				],
			]

		};
	},
	methods: {
		getCurrentYear() {
			return new Date().getFullYear();
		},
	},
};
</script>

<style lang="scss" scoped>
@import '@/components/FooterBlock/FooterBlock.scss';
</style>

