<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					bio:
						'Name: Honey Cuizon',
				},
				{
					id: 2,
					bio:
						'Im Honey Cuizon 23 yrs of age, studied at CPC 3rd yr college.  I live in Gabi cordova for the meantime. My birthday is on September 16, 200. I have 3 siblings, 2 boys and 1 girl, my 2 brother already have a family, while my sister and I are still studying ',
				},
			],
		};
	},
};
</script>

<template>
    <body class="bg-blue-400">
	<div class="block sm:flex sm:gap-10 mt-10 sm:mt-20 bg-blue-400">
		<!-- About profile image -->
		<div class="w-full sm:w-1/4 mb-7 sm:mb-0">
			<img
				src="@/assets/images/hani.jpg"
				class="rounded-xl w-96"
				alt="hani"
			/>
		</div>

		<!-- About details -->
		<div class="w-full sm:w-3/4 text-left">
			<p
				v-for="bio in bios"
				:key="bio.id"
				class="font-general-regular mb-4 text-ternary-light dark:text-ternary-light text-lg"
			>
				{{ bio.bio }}
			</p>
		</div>
	</div>
</body>
</template>
