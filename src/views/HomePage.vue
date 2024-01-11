<template>
	<HeaderBlock />
	<div class="container">
		<MainBlock />
	</div>
	<FooterBlock />
</template>

<script>

import HeaderBlock from "@/components/HeaderBlock/HeaderBlock.vue"
import MainBlock from "@/components/MainBlock/MainBlock.vue"
import FooterBlock from "@/components/FooterBlock/FooterBlock.vue";

export default {
	name: "HomePage",
	data() {
		return {
			isChecked: false,
		};
	},
	methods: {},
	components: { HeaderBlock, MainBlock, FooterBlock },
};
</script>

<style lang="scss">
@import '@/styles/style.scss';

.container {
	background: linear-gradient($background-primary, $background-secondary);
}

// .wrapper {
// 	background: $background-primary;
// }
</style>
