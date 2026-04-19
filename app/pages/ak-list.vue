<template>
  
    <h1 class="p-4 text-3xl font-bold text-center">
      Akhanda kiirtan list
    </h1>


    
    <div class=" mx-1">

      <div class="p-4 border border-gray-500/30 rounded  flex justify-around">
        
        <div>
          <div class="flex ">
            <div class="px-2">Time:</div>
            <input class="w-24" type="text" value="10:00">
          </div>
        </div>

        <!-- <div>|</div> -->

        <div>
          <div class="flex ">
            <div class="px-2">Date:</div>
            <input class="w-24" type="text" value="19.04.2026">
          </div>
        </div>

        

      </div>
      <!-- <div 
        class="text-center border-r border-l border-t last:border-b hover:bg-blue-500/20"
        v-for="(item, index) in slots" :key="index"> -->
      <div 
        class="my-2 text-center border rounded hover:bg-blue-500/20"
        v-for="(item, index) in slots" :key="index">
        <div class="flex justify-between items-center gap-4">
  
          <div class="py-2 px-8 text-xl bg-gray-500/20 ">{{ item.time }}
            <!-- <div class=""></div> -->
            <!-- <div class="text-[10px]">{{ item.date }}</div> -->
          </div>
  
          <div class="">{{ item.username }}
            <!-- <input type="text" :value="$(item.username)"> -->
          </div>
          <div class="py-2 px-8 text-xl bg-gray-500/20">{{ item.id }}
            <!-- <div class=""></div> -->
          </div>
  
        </div>
        <!-- <div class="text-sm text-gray-500/70">{{ toLocalTime(item.time) }}</div> -->
      </div>
    </div>
    
    
    <div class="my-4 mx-1 flex justify-end gap-4 ">
      
      <div class="p-4  bg-gray-500/20 hover:bg-blue-500/20 flex justify-center items-center hover:cursor-pointer" @click="handleEdit">
        <svg class="size-10" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="m16.862 4.487 1.687-1.688a1.875 1.875 0 1 1 2.652 2.652L6.832 19.82a4.5 4.5 0 0 1-1.897 1.13l-2.685.8.8-2.685a4.5 4.5 0 0 1 1.13-1.897L16.863 4.487Zm0 0L19.5 7.125" /></svg>
      </div>
      <div class="p-4  bg-gray-500/20 hover:bg-blue-500/20 flex justify-center items-center hover:cursor-pointer" @click="handleShare">
        <svg class="size-10" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="M13.19 8.688a4.5 4.5 0 0 1 1.242 7.244l-4.5 4.5a4.5 4.5 0 0 1-6.364-6.364l1.757-1.757m13.35-.622 1.757-1.757a4.5 4.5 0 0 0-6.364-6.364l-4.5 4.5a4.5 4.5 0 0 0 1.242 7.244" /></svg>
      </div>
      <div class="p-4  bg-gray-500/20 hover:bg-blue-500/20 flex justify-center items-center hover:cursor-pointer" @click="handleAdd">
        <svg class="size-10" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" /></svg>
      </div>
      
      
      
      <div class="p-4  bg-gray-500/20 hover:bg-blue-500/20 flex justify-center items-center hover:cursor-pointer" @click="handleSettings">
        <svg class="size-10 " xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="M9.594 3.94c.09-.542.56-.94 1.11-.94h2.593c.55 0 1.02.398 1.11.94l.213 1.281c.063.374.313.686.645.87.074.04.147.083.22.127.325.196.72.257 1.075.124l1.217-.456a1.125 1.125 0 0 1 1.37.49l1.296 2.247a1.125 1.125 0 0 1-.26 1.431l-1.003.827c-.293.241-.438.613-.43.992a7.723 7.723 0 0 1 0 .255c-.008.378.137.75.43.991l1.004.827c.424.35.534.955.26 1.43l-1.298 2.247a1.125 1.125 0 0 1-1.369.491l-1.217-.456c-.355-.133-.75-.072-1.076.124a6.47 6.47 0 0 1-.22.128c-.331.183-.581.495-.644.869l-.213 1.281c-.09.543-.56.94-1.11.94h-2.594c-.55 0-1.019-.398-1.11-.94l-.213-1.281c-.062-.374-.312-.686-.644-.87a6.52 6.52 0 0 1-.22-.127c-.325-.196-.72-.257-1.076-.124l-1.217.456a1.125 1.125 0 0 1-1.369-.49l-1.297-2.247a1.125 1.125 0 0 1 .26-1.431l1.004-.827c.292-.24.437-.613.43-.991a6.932 6.932 0 0 1 0-.255c.007-.38-.138-.751-.43-.992l-1.004-.827a1.125 1.125 0 0 1-.26-1.43l1.297-2.247a1.125 1.125 0 0 1 1.37-.491l1.216.456c.356.133.751.072 1.076-.124.072-.044.146-.086.22-.128.332-.183.582-.495.644-.869l.214-1.28Z" /><path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" /></svg>
      </div>
    </div>



</template>






<script setup>

const toLocalTime = (time) => { return new Date(time).toLocaleString() }


const handleShare = () => { console.log('handleShare')}
const handleSettings = () => { console.log('handleSettings')}

const slots = ref([
    {
        "id": 1,
        "username": "Ramesh",
        "time": "10:00",
        "date": "2026-04-19"
    },
    {
        "id": 2,
        "username": "Mantresh",
        "time": "10:30",
        "date": "2026-04-19"
    },
    {
        "id": 3,
        "username": "Nikolay",
        "time": "11:00",
        "date": "2026-04-19"
    },
    {
        "id": 4,
        "username": "Eminem",
        "time": "11:30",
        "date": "2026-04-19"
    },
    {
        "id": 5,
        "username": "Don Chichi",
        "time": "12:00",
        "date": "2026-04-19"
    },
    {
        "id": 6,
        "username": "Mangala",
        "time": "12:30",
        "date": "2026-04-19"
    },
    
])

</script>
