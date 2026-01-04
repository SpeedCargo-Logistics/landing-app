<template>
    <div class="site-wrapper flex flex-row gap-5">
        <Nav />
        <div class="pt-20 pl-30">
            <section id="getQuotas" class="flex flex-col gap-10 h-200 py-10">
                <h1 class="text-cyan-800 text-5xl font-bold w-200">Delivery your cargo without any problems and delays</h1>
                <p class="text-cyan-600 text-2xl font-semibold uppercase">Get affordable quotes</p>
                <form class="flex flex-row gap-5 w-250 items-center mt-10">
                    <div class="flex flex-col gap-2">
                        <!-- <label for="startLocation" class="uppercase bg-gray-200 text-cyan-800 p-2">
                            Start location
                        </label> -->
                        <input
                            name="startLocation"
                            id="startLocation"
                            class="py-4 px-3 bg-gray-200 rounded-xl w-60 text-xl text-cyan-800"
                            placeholder="Pick up location"
                        />
                    </div>
                    <div class="flex flex-col gap-2">
                        <!-- <label for="endLocation" class="uppercase bg-gray-200 text-cyan-800 p-2">
                            End location
                        </label> -->
                        <input
                            name="endLocation"
                            id="endLocation"
                            class="py-4 px-3 bg-gray-200 rounded-xl w-60 text-xl text-cyan-800"
                            placeholder="Drop off location"
                        />
                    </div>
                    <div class="flex flex-col gap-2">
                         <!-- <label for="parcelItemsCount" class="uppercase bg-gray-200 text-cyan-800 p-2">
                            Parcel items
                        </label> -->
                        <input
                            name="parcelItemsCount"
                            id="parcelItemsCount"
                            class="py-4 px-3 bg-gray-200 rounded-xl w-60 text-xl text-cyan-800"
                            placeholder="Parcel items count"
                        />
                    </div>
                    <button
                        class="primary-background hover:bg-blue-700 text-white py-2 px-4 rounded-xl h-10 uppercase text-xs cursor-pointer font-bold"
                        v-on:click="handleQuotesSearch"
                        type="button"
                        v-bind:disabled="quotasLoading"
                    >Get quote</button>
                    <div role="status" v-if="quotasLoading">
                            <svg aria-hidden="true" class="w-5 h-5 text-neutral-tertiary animate-spin fill-red" viewBox="0 0 100 101" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M100 50.5908C100 78.2051 77.6142 100.591 50 100.591C22.3858 100.591 0 78.2051 0 50.5908C0 22.9766 22.3858 0.59082 50 0.59082C77.6142 0.59082 100 22.9766 100 50.5908ZM9.08144 50.5908C9.08144 73.1895 27.4013 91.5094 50 91.5094C72.5987 91.5094 90.9186 73.1895 90.9186 50.5908C90.9186 27.9921 72.5987 9.67226 50 9.67226C27.4013 9.67226 9.08144 27.9921 9.08144 50.5908Z" fill="currentColor"/>
                                <path d="M93.9676 39.0409C96.393 38.4038 97.8624 35.9116 97.0079 33.5539C95.2932 28.8227 92.871 24.3692 89.8167 20.348C85.8452 15.1192 80.8826 10.7238 75.2124 7.41289C69.5422 4.10194 63.2754 1.94025 56.7698 1.05124C51.7666 0.367541 46.6976 0.446843 41.7345 1.27873C39.2613 1.69328 37.813 4.19778 38.4501 6.62326C39.0873 9.04874 41.5694 10.4717 44.0505 10.1071C47.8511 9.54855 51.7191 9.52689 55.5402 10.0491C60.8642 10.7766 65.9928 12.5457 70.6331 15.2552C75.2735 17.9648 79.3347 21.5619 82.5849 25.841C84.9175 28.9121 86.7997 32.2913 88.1811 35.8758C89.083 38.2158 91.5421 39.6781 93.9676 39.0409Z" fill="currentFill"/>
                            </svg>
                            <span class="sr-only">Loading...</span>
                    </div>
                </form>
                <div class="flex flex-row gap-4">
                    <button
                        class="primary-background hover:bg-blue-700 text-white py-2 px-4 rounded-xl uppercase text-xs h-10 cursor-pointer font-bold"
                    >Price API</button>
                    <button
                        class="primary-background hover:bg-blue-700 text-white py-2 px-4 rounded-xl uppercase text-xs h-10 cursor-pointer font-bold"
                    >Get an app</button>
                </div>
            </section>
            <section id="howDoWeWork" class="flex flex-col gap-5">
                <div class="flex flex-col gap-5">
                    <h1 class="text-cyan-800 text-5xl font-bold w-200">How do we work</h1>
                    <p class="font-semibold text-xl text-gray-200 w-200">
                        SpeedCargo makes tricky deliveries simple.
                        Finding a driver for your parcel or items as easy as been ever.
                        All you have to do is list your items and choose one of thousands of verified transport companies.
                        And your item would be ready to go.
                    </p>
                </div>
                <div class="flex flex-row gap-5">
                    <div class="flex flex-col gap-5 bg-gray-200 p-10">
                        <h3 class="text-xl text-cyan-800">List your item for 0 fee</h3>
                        <p class="pr-2 text-gray-500">Describe your shipment and list it for free. It will only take you a couple of minutes.</p>
                        <img src="" />
                    </div>
                    <div class="flex flex-col gap-5 bg-gray-200 p-10 w-100">
                        <h3 class="text-xl text-cyan-800">Waiting for shipment proposals to come and choose one</h3>
                        <p class="pr-2 text-gray-500">Waiting for a shipment proposals to come, verify it's quotas, and choose the onces captured your attention.</p>
                        <img src="" />
                    </div>
                    <div class="flex flex-col gap-5 bg-gray-200 p-10 w-80">
                        <h3 class="text-xl text-cyan-800">Accept right quote</h3>
                        <p class="pr-2 text-gray-500">Accept the right and most affordable quota - and it's done, your shipment will be on the way!</p>
                        <img src="" />
                    </div>
                </div>
            </section>
            <section id="uniqueFeatures" class="mt-20">
                <div class="flex flex-col gap-5">
                    <h2 class="text-cyan-800 text-5xl font-bold w-200">Unique features</h2> 
                     <div class="flex flex-row gap-5">
                        <div class="flex flex-col gap-5 bg-gray-200 p-10 w-100">
                            <h3 class="text-xl text-cyan-800">Price prediction API per subscription</h3>
                            <p class="text-gray-500">Get price predictions for items and routes. Would be useful in order to know average prices.</p> 
                        </div>
                        <div class="flex flex-col gap-5 bg-gray-200 p-10 w-100">
                            <h3 class="text-xl text-cyan-800">Driver verification API per subscription</h3>
                            <p class="text-gray-500">Verify drivers by search for it's company name.</p>
                        </div>
                    </div>
                </div>
                <div class="flex flex-col gap-6 mt-10">
                    <h2 class="text-cyan-800 text-5xl font-bold w-200">Refund policy</h2>
                    <p class="text-cyan-700 text-2xl">We provide strong refund policy and incident resolutions.</p>
                </div>
            </section>
            <section id="savings" class="mt-20">
                <div class="flex flex-col gap-5">
                    <h2 class="text-cyan-800 text-5xl font-bold w-200">How much can you save using SpeedCargo?</h2>
                    <p class="text-cyan-700 text-2xl">
                        The average cost of transportation of a Toyota Prius from Warsaw to Kyiv is about €0.50/km, which gives a total of around €408.
                        With SpeedCargo the car was transported by a company that was doing the same route anyway but had extra room for one car.
                        The price was €360, so almost 20% less.
                    </p>
                    <img src="" alt="SpeedCargo - cost savings" />
                </div>
            </section>
        </div>
    </div>
</template>
<script setup>
    import { ref } from 'vue'
import Nav from './Nav.vue'

    const handleQuotesSearch = () => {
        console.log('Search...')

        quotasLoading.value = true
    }

    const quotasLoading = ref(false)
</script>