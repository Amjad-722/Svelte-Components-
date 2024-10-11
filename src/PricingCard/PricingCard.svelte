<script>
    let pricingPlans = [
        {
            plan: "Free",
            description: "Freelancer",
            price: "$0",
            features: ["1 user", "10 projects", "Roster files"],
            bgColor: "bg-gradient-to-r from-red-500 to-yellow-500",
            bgText: "text-gray-900",
            bgimage: "https://thumbs.dreamstime.com/b/multiple-mixed-colors-background-illustration-abstract-blurred-color-background-picture-multiple-mixed-colors-background-240631260.jpg",
            iconColor: "text-red-700" 
        },
        {
            plan: "Pro",
            description: "Small Team",
            price: "$49",
            features: ["5 users", "Unlimited projects", "All file types"],
            bgColor: "bg-gradient-to-r from-blue-500 to-green-500",
            bgText: "text-black",
            bgimage: "https://images.unsplash.com/photo-1568602471122-7832951cc4c5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80",
            iconColor: "text-blue-700" },
        {
            plan: "Enterprise",
            description: "Large Teams",
            price: "$99",
            features: ["20 users", "Unlimited projects", "Priority support"],
            bgimage: "https://img.freepik.com/free-vector/gradient-dynamic-blue-lines-background_23-2148995756.jpg?size=626&ext=jpg&ga=GA1.1.553209589.1728604800&semt=ais_hybrid-rr-similar",
            bgColor: "bg-gradient-to-r from-purple-500 to-pink-500",
            bgText: "text-white",
            iconColor: "text-White-700" 
        }
    ];
</script>


<style>
    .pricing-card {
        max-width: 400px;
    }
</style>
<main class="h-screen justify-center flex items-center">
    <div class="grid md:grid-cols-3 sm:grid-cols-1 space-x-6">
        {#each pricingPlans as plan}
            <div class={`pricing-card flex flex-col border-2 hover:-translate-y-4 hover:shadow-7xl hover:shadow-stone-800 text-start px-16 items-start rounded-3xl border-gray-500 shadow-xl shadow-gray-700 ${plan.bgColor}`} style="background-image: url({plan.bgimage}); background-size: cover; background-repeat: no-repeat;">
                <span class={`font-semibold pt-8 text-start py-1 w-full ${plan.bgText}`}>{plan.plan}</span>
                <span class={`text-start w-full ${plan.bgText}`}>{plan.description}</span>
                <p class={`text-5xl font-bold py-5 text-start w-full ${plan.bgText}`}>{plan.price}</p>
                <ul class="flex flex-col my-14 text-start w-full">
                    {#each plan.features as feature}
                    <div class="flex py-2 gap-2 text-fill flex-row">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class={`w-6 h-6 ${plan.iconColor}`}>
                            <path stroke-linecap="round" stroke-linejoin="round" d="M9 12.75 11.25 15 15 9.75M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z" />
                        </svg>
                        <li class={`font-semibold ${plan.bgText}`}>{feature}</li>
                    </div>
                    {/each}
                </ul>
                <button class="border-2 py-2 px-10 my-10 rounded-full bg-gradient-to-r hover:to-cyan-500 shadow-md shadow-slate-600 to-gray-400 from-white">
                    Get Started
                </button>
            </div>
        {/each}
    </div>
</main>

