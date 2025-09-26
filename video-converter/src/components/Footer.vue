<template>
  <div class="bg-[#f2f2f2] px-4 py-14 comd:px-20 md:px-28">
    <div class="grid md:grid-cols-5 lg:grid-cols-10">
      <div class="md:col-span-3 md:flex md:flex-wrap lg:col-span-4 maxmd:grid maxmd:grid-cols-2">
        <div v-for="(list, index) in lists" :key="index" class="mx-4 mb-5 maxmd:text-center">
          <p class="font-semibold text-black md:pb-2">{{ list.listName }}</p>
          <ul class="text-[#b53836] [&>*]:py-1">
            <!-- <li>{{ list.listContent[0].name1 }}</li>
          <li>{{ list.listContent[0].name2 }}</li> -->
            <li v-html="list.listContent[0].name1"></li>
            <li v-html="list.listContent[0].name2"></li>
          </ul>
        </div>
      </div>
      <div class="text-center md:col-span-2 md:text-end lg:col-span-6 maxmd:pt-5 maxmd:text-15px">
        <p class="text-black">Lorem, ipsum dolor amet.</p>
        <p class="text-gray-400">Lorem ipsum dolor consectetur.</p>
      </div>
    </div>
    <p class="mb-7 mt-10 text-center text-xl font-semibold text-gray-400 md:mb-10 md:mt-14 md:text-2xl">We've already converted <span class="font-bold text-gray-500">1,672,395,206 files</span> with a total size of <span class="font-bold text-gray-500">12,972 TB.</span></p>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const lists = ref([
  {
    listName: 'Company',
    listContent: [
      {
        name1: 'About&nbsp;Us',
        name2: 'Security',
      },
    ],
  },
  {
    listName: 'Resources',
    listContent: [
      {
        name1: 'Blog',
        name2: 'Status',
      },
    ],
  },
  {
    listName: 'Legal',
    listContent: [
      {
        name1: 'Privacy',
        name2: 'Terms',
      },
    ],
  },
  {
    listName: 'Contact',
    listContent: [
      {
        name1: 'Contact&nbsp;Us',
        name2: 'Imprint',
      },
    ],
  },
]);
</script>
