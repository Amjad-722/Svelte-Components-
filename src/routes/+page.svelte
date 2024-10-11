<script>
  import Buttons from "../Buttons/Buttons.svelte";
  import Navabr from "../Navbar/Navabr.svelte";
  import Nvabr from "../Navbar/Navabr.svelte";
import Notificationes from "../Notificationes/Notificationes.svelte";
  import PricingCard from "../PricingCard/PricingCard.svelte";

  
  </script>

  <main>
    <div class="p-5">
      <h1 class="text-3xl font-bold flex justify-center text-gray-500 items-center">Navbar</h1>
      <Navabr/>
    </div>
    <hr class="border-1 border-gray-400 ">
    <div class="p-5">
      <h1 class="text-3xl font-bold flex justify-center text-gray-500 items-center">Notifications Card</h1>
      <Notificationes/>
    </div>  
      <hr class="border-1 border-gray-400 ">
    <div class="py-5">
      <h1 class="text-3xl font-bold flex justify-center text-gray-500 items-center ">Buttons</h1>
      <Buttons/>
    </div>
    <hr class="border-1 border-gray-400 ">
    <div class="py-5">

      <h1 class=" text-3xl mt-40 font-bold flex justify-center text-gray-500 items-center ">Pricing Card</h1>
<PricingCard/>
    </div>

   
  </main>
  
 
  