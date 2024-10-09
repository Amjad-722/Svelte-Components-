<script>
  export let Notifi = "Notificationes";
  export let show = "Show All";
  export let date = "Today";
  export let image =
    "https://avatars.githubusercontent.com/u/159441246?v=4&size=64";
  export let status = false;
  let notifications = [
    {
      title: "Greta luck",
      description: "Lorem ipsum dolor sit dfghsdgfhsgdfhshdgfhsgamet",
      sender: "Imran Ali",
      time: "5 days ago",
    },
    {
      title: "Jane Doe",
      description: "Lorem ipsum dolor sit amet consectetur adipisicing.",
      sender: "John Smith",
      time: "3 days ago",
    },
    {
      title: "New Update",
      description: "An update is available for your software.",
      sender: "System Admin",
      time: "2 days ago",
    },
    {
      title: "Welcome Back",
      description: "It's been a while since you last logged in.",
      sender: "Support Team",
      time: "1 day ago",
      
    },
  ];
</script>

<main>
  <div class="w-1/3 mx-auto align-middle border shadow-md mt-10 rounded-lg">
    <div class="flex flex-row justify-between pt-10 px-4">
      <h2 class="font-medium text-2xl">{Notifi}</h2>
      <p class="text-xl text-blue-500 cursor-pointer">{show}</p>
    </div>
    <div>
      <h1 class="font-medium text-xl pt-10 text-gray-500 px-4">{date}</h1>
    </div>

    {#each notifications as notification}
      <div class="flex flex-row pt-8 pl-3">
        <div class="relative flex flex-row px-4 pt-4">
          <div class="relative">
            <img src={image} alt="" class="size-16 rounded-lg" />
            <div class="absolute bottom-0 right-0">
              {#if notification.status}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="size-6 fill-green-600 text-white"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M9 12.75 11.25 15 15 9.75M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
                  />
                </svg>
              {/if}
              {#if !notification.status}
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="size-6 fill-red-600 text-white"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="m9.75 9.75 4.5 4.5m0-4.5-4.5 4.5M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
                  />
                </svg>
              {/if}
            </div>
          </div>
        </div>

        <div class="flex flex-col pt-2 pl-2 gap-1">
          <h1 class="font-semibold text-black text-[18px]">
            {notification.title}
            <span class="font-normal text-gray-500 text-[18px]"
              >confirms from</span
            >
            {notification.sender}
          </h1>
          <p class="truncate max-w-xs">{notification.description}</p>
          <p class="text-gray-500">{notification.time}</p>
        </div>
      </div>
    {/each}
  </div>
</main>
