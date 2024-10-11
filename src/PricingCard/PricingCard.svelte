<script>
   
    let pricingPlans = [
        {
            plan: "Free",
            description: "freelancer",
            price: "$0",
            features: ["1 user", "10 projects", "Roster files"],
            bgColor: "gradient-to-r from-red-500 to-yellow-500",
            bgimage: "https://img.freepik.com/free-photo/futuristic-metaverse-empty-room-product-display-presentation-abstract-technology-scifi-with-neon-light-3d-background_56104-2314.jpg",

        },
        {
            plan: "Pro",
            description: "Small Team",
            price: "$49",
            bgColor: "gradient-to-r from-blue-500 to-green-500",
            features: ["5 users", "Unlimited projects", "All file types"],
            bgimage: "https://images.unsplash.com/photo-1568602471122-7832951cc4c5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80",
        },
        {
            plan: "Enterprise",
            description: "Large Teams",
            price: "$99",
            features: ["20 users", "Unlimited projects", "Priority support"],
            bgimage: "https://images.unsplash.com/photo-1568602471122-7832951cc4c5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80",
            bgColor: "gradient-to-r from-blue-500 to-green-500",

   
        }
    ];

</script>

<style>
    .pricing-card {
        max-width: 600px;
    }
</style>

<main class="h-screen justify-center flex items-center bg-gray-100">
    <div class="grid md:grid-cols-3 sm:grid-cols-1   space-x-6">
       
        {#each pricingPlans as plan}
        <div class={`pricing-card flex flex-col border-2 hover:-translate-y-4 hover:shadow-7xl hover:shadow-stone-800 text-start px-16 items-center rounded-3xl border-gray-500 shadow-xl shadow-gray-700 ${ plan.bgColor}`}>
                <span class="font-semibold pt-8">{plan.plan}</span>
                <span class="text-gray-500">{plan.description}</span>
                <p class="text-5xl font-bold py-5">{plan.price}</p>
                <ul class="flex flex-col my-14">
                    {#each plan.features as feature}
                        <li class="font-semibold text-gray-500">{feature}</li>
                    {/each}
                </ul>
                <button class="border-2 py-2 px-10 my-10 rounded-full bg-gradient-to-r hover:to-cyan-500 shadow-md shadow-slate-600 to-gray-400 from-white">
                    Get Started
                </button>
            </div>
        {/each}
    </div>
</main>
