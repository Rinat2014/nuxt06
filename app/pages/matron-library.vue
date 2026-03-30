<template>
  
    <h1 class="p-4 text-3xl font-bold text-center">
      Библиотека знаний
    </h1>
    
    
    <!-- info block -->
    <div 
      class="my-4 border rounded"
      v-for="(item_main, index_main) in my_content" :key="index_main"
      >
      <h2 class="px-2 text-xl text-center font-semibold bg-gray-500/10 ">{{ item_main.blok_title }}</h2>
      
      <div
        v-for="(item, index) in item_main.blok_content" :key="index"
        >
        <div class="px-2 text-center font-semibold bg-gray-500/10 mt-1">{{ item.blok_content_title }}</div>
        <ul class="list-none ">
          <li 
            class="pl-2 mb-4 my-1 border-b border-dotted hover:border-green-500 hover:bg-green-200/30 hover:marker:text-green-500 "
            v-for="(link, index_link) in item.links" :key="index_link"
            >
            <NuxtLink class="" :to="link.link_url"  target="_blank">
              {{ link.link_text }}
              <div class="pr-2 text-sm text-end text-gray-500/80 ">{{ link.link_subtext }}</div>
            </NuxtLink>
          </li>
        </ul>
      </div>



    </div>
    


    

</template>




<script setup>

const my_content = ref([
  {
    blok_title: "Подборка аллергия",
    blok_content: [
      {
        blok_content_title: "",
        links: [
          {
            link_text: "Психосоматика : астма, аллергия , насморк, раздражительность",
            link_url: "https://m.youtube.com/watch?v=RbxtYhDcxIE",
            link_subtext: "время в видео --:--"
          },
          {
            link_text: "С самого детства аллергия , что делать",
            link_url: "https://m.youtube.com/watch?v=qydPY5vktcQ&t=1483s",
            link_subtext: "время в видео 00:24"
          },
          {
            link_text: "Как избавится от аллергии/болезни?",
            link_url: "https://m.youtube.com/watch?time_continue=193&v=VShgP1XZM0s&feature=emb",
            link_subtext: "время в видео --:--"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-2",
        links: [
          {
            link_text: "link_text1   Lorem ipsum dolor sit !",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-3",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-4",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      
    ],
  },
  {
    blok_title: "My_blok_title",
    blok_content: [
      {
        blok_content_title: "block_content_title-1",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora unde quisquam commodi sed beatae tempore fugit, consectetur eveniet id architecto.",
            link_url: "link_url1",
            link_subtext: "время в видео 10:33"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 15:15"
          },
          {
            link_text: "link_text3 Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, asperiores eius! Enim deserunt architecto quibusdam dolores autem adipisci placeat saepe necessitatibus ea deleniti vitae error, facilis perspiciatis, soluta excepturi modi.",
            link_url: "link_url3",
            link_subtext: "время в видео 11:22"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-2",
        links: [
          {
            link_text: "link_text1   Lorem ipsum dolor sit !",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-3",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-4",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      
    ],
  },
  {
    blok_title: "My_blok_title",
    blok_content: [
      {
        blok_content_title: "block_content_title-1",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora unde quisquam commodi sed beatae tempore fugit, consectetur eveniet id architecto.",
            link_url: "link_url1",
            link_subtext: "время в видео 10:33"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 15:15"
          },
          {
            link_text: "link_text3 Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, asperiores eius! Enim deserunt architecto quibusdam dolores autem adipisci placeat saepe necessitatibus ea deleniti vitae error, facilis perspiciatis, soluta excepturi modi.",
            link_url: "link_url3",
            link_subtext: "время в видео 11:22"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-2",
        links: [
          {
            link_text: "link_text1   Lorem ipsum dolor sit !",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-3",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      {
        blok_content_title: "block_content_title-4",
        links: [
          {
            link_text: "link_text1  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url1",
            link_subtext: "время в видео 11:11"
          },
          {
            link_text: "link_text2  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url2",
            link_subtext: "время в видео 22:22"
          },
          {
            link_text: "link_text3  Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime, fugit! consectetur adipisicing elit. Maxime, fugit!",
            link_url: "link_url3",
            link_subtext: "время в видео 33:33"
          },
        ],
      },

      
    ],
  },

])

</script>

