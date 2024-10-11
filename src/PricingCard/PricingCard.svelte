<script>
    let pricingPlans = [
        {
            plan: "Free",
            description: "freelancer",
            price: "$0",
            features: ["1 user", "10 projects", "Roster files"],
            bgColor: "bg-gradient-to-r from-red-500 to-yellow-500", 
            bgText: "text-gray-900",  
            bgimage: "https://thumbs.dreamstime.com/b/multiple-mixed-colors-background-illustration-abstract-blurred-color-background-picture-multiple-mixed-colors-background-240631260.jpg",
        },
        {
            plan: "Pro",
            description: "Small Team",
            price: "$49",
            bgColor: "bg-gradient-to-r from-blue-500 to-green-500",  
            features: ["5 users", "Unlimited projects", "All file types"],
            bgText: "text-black", 
            bgimage: "https://images.unsplash.com/photo-1568602471122-7832951cc4c5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=387&q=80",
        },
        {
            plan: "Enterprise",
            description: "Large Teams",
            price: "$99",
            features: ["20 users", "Unlimited projects", "Priority support"],
            bgimage: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxAQDw8PEBAVEg8PDw8PFRUVEA8PEBAPFREWFhUVFRUYHSggGBolHRUVITEhJSkrLi4uFx8zODMtNygtLisBCgoKDg0OFRAQGi0dHyUtLS0tLS0tLS0tLS0tLS0tLS0rLS0tLS0tLS0tNy0tLS0rLS0tLS0tLS0tLS0tLS0tLf/AABEIAMIBAwMBIgACEQEDEQH/xAAaAAEBAQEBAQEAAAAAAAAAAAAAAQIDBAUG/8QALxAAAgIABAQFAgcBAQAAAAAAAAECESExQVEDEmFxgZGhsfDR4QQTIjJCwfFSYv/EABoBAQEBAQEBAQAAAAAAAAAAAAABAgMEBgX/xAAhEQEBAAIBAwUBAAAAAAAAAAAAAQIREgMhMQQTQVFhFP/aAAwDAQACEQMRAD8A+VCcMr8adHoUFpj7HzIcZ8ulZXqdOFxZpVF4dsV9DpcHxGXSvxX0ZqMc/LUxxHgrfWl/Z4+DJSdX+r3OnFqOLeO2pOLHt6uvl2hxIVbdeDs5viKTp4LT79Tl+Zayx3OMptZmuLpj03sa5cE8fQxOMY4ydt6Zt/Q4Litft9rrscXLOV37l4tTp16OPNLGVX/GOaS3fzE4QirtvmbxpYt99jjKd41h0JzX89x7fZ6MMLHaTSwSTltjyx+p0UbWL5az/wBPNzJK3lvepzk5PFvD0NY4Rbhv8et8eOkkuuvgvngeXjca/wBMVUdd5fRdDEEcuN+I/jDz+n1NzGOuHSkvbu1xJRjhnLbbvsc/zFm89jjCt15pFlNLLF+h0kej254Wb/k8PmSOc+JeLx2SwSEscZOvmhxlNaX3K644balNZvwSwMriLN+VGZMxJaah1mEa4jvpFfPFnKTTyy9Q4mWRuSJJrTP0RzwNNGWR0kZZlmmZZGoyRmiMjTJJMplkGWRlZDLaUQtgK/aRWOWHq/mx3clhjfTY4uMo5tW9G0OdfyTTXQ5zPG+K/Cz9PlO9j0Oa7sRaWLxXqebn5svuWn1ZOcZ/ly09C/EK/wDlefmc5/iFlFYbvN/Q5ynFYPPb5kRYK5YLRavsalhPT/guLT29UbXG5slXiedcS7bw82YnJ1f7YrfV/NDUyjtfT7vju63eX+mJy5csZd8F337HKXHbVRVe/wBjCaWD0N621OnflVxXe/sa/P8A+vQ4zexlPc3I6Xpy93onxXJbR9++5wnxLwWC9WV8qVt/22c3xU+i8ymOEnhU0Z/NrLD1Mud9vUy8dCunH7Vu8c31GWZiXqZc3qw1xdHP/lY/MjlKWi8X9CuTrZbnLmWwrWOLTk66GObyEpX0Rlsm25i1a2+hiT3zHM9zJNrIhLL4mWzLQ2QlkbCjZlsAy1pGRlZCKyAQiv2MZK8F+nrh/h34TeXLzLbRdnn4Hz3+Jcnsl4HaDU1/a/s82XT0xxezh8K26a/TnisO5njfi1+1SUd5KMn5NXXl4ng4iisHi+lM5fmvLJep0x6Eve1Lj+PTxXGv049cr7GFNdb65I5XomZnJrNr+zvMO3dLjHoc+VczlvStPmfY4Odu3b7nOT/849xz979Czp6u2bHaXFaWGHXNmIyVY+eZzlJRVy1yWr+3U5ObeL8tEdJpy4fDtLiN5YIzJ74s58+2BOZrqXbXBuT3zCa1dHPm8WS2Di6OnlkRvS/ncwkYctFl7kOLbltlvqzNksnMg1pWZaDMCrGm9jLRW67+xgixbMMtmWyNaRhsphmVLJQZGRSzNlIRQjAIrIAA/Qqd6euAWGbq9rMJap+xcG8X46HWt8XRNaLDd4CUtl4nKctFl7kfEdVgu2YiWfa2k+vTQSktMX4mEloW6NRirFvTAO9yyVrRLyOTnpbounPz4HV529yvoZeBOZePkCujdLEylfY5t75kYZ01J7fYikZKRdLJvXIiM+xG/IJppvEnPROZmcCbXQ3uLIMgo92ZbsSZlshIrM2WyURpGQNkIFmWUhFGRiyEUFkBFQAAfcar9338ha0OTwLKV6+leZ2da3zbLAvNHW7Oa6YMSa1dvpj/AIaYqksnM32I3sGVeBJS2VDlMc3UjOlXYjn0DZlhGq1slk8DNBNNtsywSTIAsWLAWRhtGcwg2QBkUMiyNkF5jLYIyWroZkrIRoICEAgAUAIQQAAfV65tl5nWi66nO/mwkzq6bb9iGVRYlRrmrWgpPoYbsjRWWkluR+45lt9DN31ZEaozmCeIRX3JbISyIthksZBBCyNi/MA2QEbIKRksNgUkg5GQAJZGZUbIwCKgIAoAQgpGCMKjBCg0+i3RLMWWzo1t0UiSnfbb6mPclhG76ksgbKithMjZLQRolk5hkELDdkIEWyFJZA5iBsWABLJZAsNghAsjYAUI2CMgMEKFQpAAIARQjBGFZYDKB7LLbMg2LZTNlRUVksjkFQRUCMWAAsgFsjZGLIiksgsIosliybFI2SwNqAEIKRsWQAQAKAACAAioARhQAAZYKAPSmWzKFm0aIRsDY0QgsIosgGxbJYJZBRZCBFbBCgQoAEbBGCCkBAq2QAACAgAAKEAChAAAKQCAADsCAqNAhAjVgzYsDVkIAKQWABbMgC2CACggAFsgAAEAFICAAAuggAUIAAAKAIABllIUDoikBWVsgAAAEAAhRQQEFBAAKQAUgAAAAAAFACAUgIFUgAApAAAAAAAZYKANgECKCFCgIUACWAiggsGlBLAFBAFUEKEASxYVQSyWBQyWAAAAAAAAAAAABgAZKQoAoAAAAAAAAAAAAAAAIUAAAAIUAAAAAAAAAAAAAAAAAAwAMAAD/9k=",
            bgColor: "bg-gradient-to-r from-purple-500 to-pink-500",
            bgText: "text-white", 
        }
    ];
</script>

<style>
    .pricing-card {
        max-width: 400px;
    }
</style>

<main class="h-screen justify-center flex items-center ">
    <div class="grid md:grid-cols-3 sm:grid-cols-1 space-x-6">
        {#each pricingPlans as plan}
            <div class={`pricing-card flex flex-col border-2 hover:-translate-y-4 hover:shadow-7xl hover:shadow-stone-800 text-start px-16 items-start rounded-3xl border-gray-500 shadow-xl shadow-gray-700 ${plan.bgColor}`} style="background-image: url({plan.bgimage}); background-size: cover; background-repeat: no-repeat;">
                <span class={`font-semibold pt-8 text-start py-1 w-full ${plan.bgText}`}>{plan.plan}</span>
                <span class={`text-start w-full ${plan.bgText}`}>{plan.description}</span>
                <p class={`text-5xl font-bold py-5 text-start w-full ${plan.bgText}`}>{plan.price}</p>
                <ul class="flex   flex-col my-14 text-start w-full">
                    {#each plan.features as feature}
                    <div class="flex py-2 gap-2 text-fill flex-row"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
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
