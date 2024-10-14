<script>
    // Array of card data for dynamic rendering
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
  </script>
  
  <!-- Breadcrumb Navigation -->
  <div class=" mt-10 p-8">
    <ul class="flex flex-row">
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">Navbar</a>
      </li>
      <span>/</span>
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">Notification</a>
      </li>
      <span>/</span>
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">Buttons</a>
      </li>
      <span>/</span>
      <li class="font-medium text-lg hover:text-blue-500 hover:underline">
        <a href="">PricingCard</a>
      </li>
    </ul>
  </div>
  

  <div class="w-full grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 p-8">
    {#each cards as card}
      <div class="border shadow-md p-8 rounded-lg flex flex-row items-center">
        <img src={card.image} alt="User avatar" class="w-16 h-16 rounded-lg" />
        <div class="flex flex-col pl-4 gap-1">
          <span class="font-medium text-xl">{card.Orders}</span>
          <span class="font-medium text-3xl leading-8">{card.OrdersNO}</span>
        </div>
      </div>
    {/each}
  </div>
  