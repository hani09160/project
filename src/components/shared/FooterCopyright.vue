<script>
export default {
	data: () => {
		return {
			copyrightDate: new Date().getFullYear(),
			projectName: 'Vue.js & Tailwind CSS Portfolio',
			
		};
	},
};
</script>

<template>
	<div class="flex justify-center items-center text-center bg-gray-400 ">
		<div
			class="font-general-regular text-lg text-ternary-dark dark:text-ternary-light"
		>
			&copy; {{ copyrightDate }}.
            PORTFOLIO

			</div></div>
</template>

<style lang="scss" scoped></style>
