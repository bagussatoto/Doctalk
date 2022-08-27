<template>
    <main class="shadow-lg bg-primary w-full px-5 pt-4 pb-3">
    	<!-- Topbar -->
        <section class="show flex justify-between">
            <div class="text-gray-50 flex items-center gap-3">
                <i class="text-sm fas fa-th-large"></i>
                <p class="text-xs">
                    September 29, 2021
                </p>
            </div>
            <img class="rounded shadow" src="/bagus.png" width="35">
        </section>

        <!-- Greetings -->
        <section class="show mt-5 text-sm text-gray-50">
            <h2 class="font-medium">Hello, Bagus Satoto</h2>
            <small>What do you need?</small>
        </section>

        <!-- Search -->
        <section class="show bg-gray-50 px-3 py-2 gap-2 mt-2 flex rounded items-center">
            <i class="text-gray-400 text-xs fa fa-search"></i>
            <input type="search" class="focus:outline-none text-xs w-full bg-gray-50" placeholder="Find a doctor or specialist">
        </section>

        <!-- Calendar -->
        <section class="show mt-3 flex justify-between gap-2 text-gray-50 overflow-scroll hide-scrollbar">
            <template v-for="card in schedules" :key="card">
                <div class="text-center">
                    <small class="text-xxs">
					   	{{ card.day }}
                    </small>
                    <div :class="concat(card.day, card.date) === active ? 'bg-gray-50 text-gray-500' : 'bg-blue-400'"
                     @click="active = concat(card.day, card.date)"
                     class="duration-300 text-xs rounded py-1 px-2 grid place-items-center">
                        {{ card.date }}
                    </div>
                    <div v-if="card.dot" class="bg-red-500 inline">
						<i class="fa fa-circle block mt-2"></i>
                    </div>
                </div>
            </template>
        </section>
    </main>
</template>

<style scoped>

	.fa-circle {
		font-size: .4rem;
	}

</style>

<script setup>

	import { ref } from 'vue'

	const active = ref('Sun-26')

	const concat = (day, date) => `${day}-${date}`

    const schedules = [
    	{
    		day: 'Sun',
    		date: '26',
    		dot: false
    	},
    	{
    		day: 'Mon',
    		date: '27',
    		dot: true
    	},
    	{
    		day: 'Tue',
    		date: '28',
    		dot: false
    	},
    	{
    		day: 'Wed',
    		date: '29',
    		dot: true
    	},
    	{
    		day: 'Thu',
    		date: '30',
    		dot: true
    	},
    	{
    		day: 'Fri',
    		date: '01',
    		dot: false
    	},
    	{
    	   day: 'Sat',
    	   date: '02',
    	   dot: false
    	},
    	{
    	   day: 'Sun',
    	   date: '03',
    	   dot: true
    	},
    	{
    	   day: 'Mon',
    	   date: '04',
    	   dot: false
    	},
    	{
    	   day: 'Tue',
    	   date: '05',
    	   dot: false
    	}
    ]
 
</script>
