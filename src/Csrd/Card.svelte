<script>

export let image = "https://avatars.githubusercontent.com/u/159441246?v=4&size=64";
export let Orders = "Order";
export let OrdersNO = "48";
</script>



<div class="w-1/3 mx-auto align-middle border shadow-md mt-10 p-8 rounded-lg flex flex-row">
    <div><img src={image} alt="" class="size-16 rounded-lg"></div>
    <div class="flex flex-col  pl-4 gap-1">
        <span class="font-medium text-xl"> {Orders}</span>
        <span class="font-medium text-3xl leading-8">  {OrdersNO}</span>
    </div>

</div>