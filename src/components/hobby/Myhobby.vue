<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					bio:
						'Hobby:',
				},
				{
					id: 2,
					bio:
						'My Hobbies when I do not have a class is: Sleeping, Eating and Playing Online Games. ',

				},
                {
                    id: 3,
                    bio: 
                        'I also like to grocery. I also like to watch kdrama and listen music.',
                }
			],
		};
	},
};
</script>

<template>
    <body class="bg-green-400">
	

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
        
	
</body>
</template>
