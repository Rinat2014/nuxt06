<template>
  
    <h1 class="p-4 text-3xl font-bold text-center">
      Index page
    </h1>
    <!-- <div class="p-2 text-justify">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sed ullam, omnis illo quibusdam qui nesciunt sapiente. Id dignissimos explicabo, accusamus accusantium officiis tempora animi asperiores. Non itaque magni ducimus. Illum libero cumque vero placeat eligendi totam rem sunt asperiores illo, iste dolores error earum architecto reiciendis labore fugit molestias alias ratione! Dicta, amet earum. Ducimus perspiciatis sapiente debitis quaerat dolorum dolores molestiae repellat odio cum maxime, aliquam quibusdam illo quasi iste. Earum, doloribus suscipit odio at porro repellendus totam placeat praesentium possimus unde error ipsa amet ad officia et consequuntur cupiditate culpa dolores! Blanditiis necessitatibus delectus sit laborum vitae non.</div> -->
    <div 
      class="text-center border-r border-l border-t last:border-b hover:bg-green-500/20"
      v-for="(item_slot, index_lost) in slots" :key="index_lost">
      {{ item_slot.musician_obj.username }}
      <div class="text-sm text-gray-500/70">{{ toLocalTime(item_slot.time) }}</div>
      <div class="text-sm text-gray-500/70 bg-gray-500/10">{{ item_slot.time }}</div>
    </div>

</template>






<script setup>

const toLocalTime = (time) => { return new Date(time).toLocaleString() }

const slots = ref([
    {
        "id": 198,
        "musician_obj": {
            "id": 3,
            "username": "Ramesh",
            "email": "zoom2000@list.ru"
        },
        "time": "2026-04-25T10:00:00Z",
        "is_regular": false
    },
    {
        "id": 199,
        "musician_obj": {
            "id": 3,
            "username": "Ramesh",
            "email": "zoom2000@list.ru"
        },
        "time": "2026-04-25T10:30:00Z",
        "is_regular": false
    },
    {
        "id": 200,
        "musician_obj": {
            "id": 3,
            "username": "Ramesh",
            "email": "zoom2000@list.ru"
        },
        "time": "2026-04-25T11:00:00Z",
        "is_regular": true
    },
    {
        "id": 207,
        "musician_obj": {
            "id": 3,
            "username": "Ramesh",
            "email": "zoom2000@list.ru"
        },
        "time": "2026-03-25T12:00:00Z",
        "is_regular": false
    },
    {
        "id": 208,
        "musician_obj": {
            "id": 17,
            "username": "t13",
            "email": "test13@email.com"
        },
        "time": "2026-03-25T12:30:00Z",
        "is_regular": false
    },
    {
        "id": 191,
        "musician_obj": {
            "id": 3,
            "username": "Ramesh",
            "email": "zoom2000@list.ru"
        },
        "time": "2026-03-25T19:00:00Z",
        "is_regular": false
    },
    {
        "id": 192,
        "musician_obj": {
            "id": 3,
            "username": "Ramesh",
            "email": "zoom2000@list.ru"
        },
        "time": "2026-03-25T19:30:00Z",
        "is_regular": false
    },
    {
        "id": 193,
        "musician_obj": {
            "id": 3,
            "username": "Ramesh",
            "email": "zoom2000@list.ru"
        },
        "time": "2026-03-25T20:00:00Z",
        "is_regular": false
    }
])

</script>
