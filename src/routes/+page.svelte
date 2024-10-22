<script>
  import Buttons from "../Buttons/Buttons.svelte";
  import Card from "../Csrd/Card.svelte";
  import Navabr from "../Navbar/Navabr.svelte";
  import Nvabr from "../Navbar/Navabr.svelte";
import Notificationes from "../Notificationes/Notificationes.svelte";
  import HoveredCards from "../PricingCard/hovedCard/hoveredCards.svelte";
  import PricingCard from "../PricingCard/PricingCard.svelte";

  
  </script>

  <main>
    <!-- <div>
      <h1 class=" mt-8 text-3xl font-bold flex justify-center text-gray-500 items-center">BreadCrumd</h1>
      <Card/>
    </div> -->
    <hr class="border-1 border-gray-400 ">
    <div class="p-5 mt-8">
      <h1 class="text-3xl font-bold flex justify-center text-gray-500 items-center">Navbar</h1>
      <Navabr/>
    </div>
    <hr class="border-1 border-gray-400 ">
    <div class="p-5">
      <h1 class="text-3xl font-bold flex justify-center text-gray-500 items-center">Notifications Card</h1>
      <Notificationes/>
    </div>  
      <hr class="border-1 border-gray-400 ">
    <div class="py-5 mt-28">
      <h1 class="text-6xl font-bold flex justify-center text-black-500 items-center ">Button</h1>
      <Buttons/>
    </div>
    <hr class="border-1 border-gray-400 ">
    <div class="py-5">

      <h1 class=" text-3xl mt-40 font-bold flex justify-center text-gray-500 items-center ">Pricing Card</h1>
<PricingCard/>
    </div>
    <div class="py-5">

      <h1 class=" text-3xl mt-40 font-bold flex justify-center text-gray-500 items-center ">Hover Cards</h1>
<HoveredCards/>
    </div>


   
  </main>
  
 
  