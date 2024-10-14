<script>
 
    let cards = [
      {
        image: "https://avatars.githubusercontent.com/u/159441246?v=4&size=64",
        Orders: "Order",
        OrdersNO: "48"
      },
      {
        image: "https://avatars.githubusercontent.com/u/159441246?v=4&size=64",
        Orders: "Pending Order",
        OrdersNO: "24"
      },
      {
        image: "https://avatars.githubusercontent.com/u/159441246?v=4&size=64",
        Orders: "Completed Order",
        OrdersNO: "72"
      }
    ];
    document.addEventListener('alpine:init', () => {
        Alpine.data('skillDisplay', () => ({
            skills: [{
                    '': 'HTML',
                    'percent': '95',
                },
                {
                    'title': 'CSS',
                    'percent': '70',
                },
                {
                    'title': 'Tailwind CSS',
                    'percent': '90',
                },
                {
                    'title': 'JavaScript',
                    'percent': '70',
                },
                {
                    'title': 'Alpine JS',
                    'percent': '80',
                }, {
                    'title': 'PHP',
                    'percent': '65',
                }, {
                    'title': 'Laravel',
                    'percent': '75',
                }
            ],
            currentSkill: {
                'title': 'HTML',
                'percent': '95',
            }
        }));
    });
  </script>
 
  
  <div class=" mt-10 p-8">
    <ul class="flex flex-row">
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">Navbar</a>
      </li>
      <span class="mx-2">/</span>
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">Notification</a>
      </li>
      <span class="mx-2">/</span>
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">Buttons</a>
      </li>
      <span class="mx-2">/</span>
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">PricingCard</a>
      </li>
    </ul>
  </div>
  

  <div class="w-full   grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 p-8">
    {#each cards as card}
      <div class="border shadow-md p-8 rounded-lg flex flex-row items-center">
        <img src={card.image} alt="User avatar" class="w-16 h-16 rounded-lg" />
        <div class="flex flex-col pl-4 gap-1">
          <span class="font-medium text-xl">{card.Orders}</span>
          <span class="font-medium text-3xl leading-8">{card.OrdersNO}</span>
        </div>
        <div class=" ml-52"> <svg class="transform -rotate-90 w-24 h-24">
            <circle cx="50" cy="50" r="25" stroke="currentColor" stroke-width="5" fill="transparent"
                class="text-gray-700" />
    
                <circle cx="50" cy="50" r="25" stroke="currentColor" stroke-width="5" fill="transparent"
                :stroke-dasharray="circumference"
                :stroke-dashoffset="circumference - currentSkill.percent / 100 * circumference"
                class="text-blue-500 " />
        </svg>
    </div>
      </div>
     
    {/each}
  </div>
  