<template>
    <div class="site-wrapper flex flex-row gap-5">
        <nav>
            <img src="../../public/logo-new.png" class="w-60 p-5" />
            <ul class="py-10 pl-3">
                <li>
                    <a href="#getQuotas" class="text-cyan-600">Get quotes</a>
                </li>
                <li>
                    <a href="#howDoWeWork" class="text-cyan-600">How do we work</a>
                </li>
                <li>
                    <a href="#uniqueFeatures" class="text-cyan-600">Unique features</a>
                </li>
                <li>
                    <a href="#savings" class="text-cyan-600">Savings and FAQ</a>
                </li>
            </ul>
        </nav>
        <div class="pt-20 pl-30">
            <section id="getQuotas" class="flex flex-col gap-10 h-200 py-10">
                <h1 class="text-cyan-600 text-5xl font-bold w-200">Delivery your cargo without any problems and delays</h1>
                <p class="text-cyan-400 text-2xl font-bold">Get affordable quotes</p>
                <form class="flex flex-row gap-5 w-250 items-end">
                    <div class="flex flex-col gap-2">
                        <label for="startLocation" class="text-cyan-400">Start location</label>
                        <input
                            name="startLocation"
                            id="startLocation"
                            class="p-3 bg-cyan-100 rounded-xl w-60"
                        />
                    </div>
                    <div class="flex flex-col gap-2">
                        <label for="endLocation" class="text-cyan-400">End location</label>
                        <input
                            name="endLocation"
                            id="endLocation"
                            class="p-3 bg-cyan-100 rounded-xl w-60"
                        />
                    </div>
                    <div class="flex flex-col gap-2">
                        <label class="text-cyan-400">Parcel items</label>
                        <input
                            name="parcelItemsCount"
                            id="parcelItemsCount"
                            class="p-3 bg-cyan-100 rounded-xl w-60"
                        />
                        <!-- <input
                            name="parcelItemsSize"
                            id="parcelItemsSize"
                            class="inset-ring-1 inset-ring-blue-500 p-3 bg-cyan-100 rounded-md w-40"
                        /> -->
                    </div>
                    <button
                        class="primary-background hover:bg-blue-700 text-white py-2 px-4 rounded-lg h-10 uppercase text-xs cursor-pointer"
                    >Get quote</button>
                </form>
                <div class="flex flex-row gap-4">
                    <button
                        class="primary-background hover:bg-blue-700 text-white py-2 px-4 rounded-lg uppercase text-xs h-10 cursor-pointer"
                    >Price API</button>
                    <button
                        class="primary-background hover:bg-blue-700 text-white py-2 px-4 rounded-lg uppercase text-xs h-10 cursor-pointer"
                    >Get an app</button>
                </div>
            </section>
            <section id="howDoWeWork" class="flex flex-col gap-5">
                <div class="flex flex-col gap-5">
                    <h1 class="text-cyan-600 text-5xl font-bold w-200">How do we work</h1>
                    <p class="font-semibold text-xl text-cyan-400 w-300">
                        SpeedCargo makes tricky deliveries simple.
                        Finding a driver for your parcel or items as easy as been ever.
                        All you have to do is list your items and choose one of thousands of verified transport companies.
                        And your item would be ready to go.
                    </p>
                </div>
                <div class="flex flex-row gap-5">
                    <div class="flex flex-col gap-5">
                        <h3 class="text-xl">List your item for 0 fee</h3>
                        <p class="pr-10 text-cyan-400">Describe your shipment and list it for free. It will only take you a couple of minutes.</p>
                        <img src="" />
                    </div>
                    <div class="flex flex-col gap-5">
                        <h3 class="text-xl">Waiting for shipment proposals to come and choose one</h3>
                        <p class="pr-10 text-cyan-400">Waiting for a shipment proposals to come, verify it's quotas, and choose the onces captured your attention.</p>
                        <img src="" />
                    </div>
                    <div class="flex flex-col gap-5">
                        <h3 class="text-xl">Accept right quote</h3>
                        <p class="pr-10 text-cyan-400">Accept the right and most affordable quota - and it's done, your shipment will be on the way!</p>
                        <img src="" />
                    </div>
                </div>
            </section>
            <!-- <section id="uniqueFeatures">
                <div>
                    <h2>Unique features</h2> 
                    <div>
                        <div>
                            <h3>Price prediction API per subscription</h3>
                            <p>Get price predictions for items and routes. Would be useful in order to know average prices.</p> 
                        </div>
                        <div>
                            <h3>Driver verification API per subscription</h3>
                            <p>Verify drivers by search for it's company name.</p>
                        </div>
                    </div>
                </div>
                <div>
                    <h2>Refund policy</h2>
                    <div>
                        <p>We provide strong refund policy and incident resolutions.</p>
                    </div>
                </div>
            </section>
            <section id="savings">
                <div>
                    <h2>How much can you save using SpeedCargo?</h2>
                    <p>
                        The average cost of transportation of a Toyota Prius from Warsaw to Kyiv is about €0.50/km, which gives a total of around €408.
                        With SpeedCargo the car was transported by a company that was doing the same route anyway but had extra room for one car.
                        The price was €360, so almost 20% less.
                    </p>
                    <img src="" />
                </div>
            </section> -->
        </div>
    </div>
</template>
