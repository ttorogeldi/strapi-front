<template>
  <div class="home">
    <div style="background: #F6F6F6" class="py-11">
      <carousel-3d
          v-if="news!==null"
          style="width: 1200px"
          class="mx-auto"
          :disable3d="true"
          :display="7"
          :space="310"
          :width="290"
          :border="0"
          :height="188"
          :clickable="false"
          :autoplay="true">
        <slide v-for="(item,index) in (news)" v-bind:key="item.id" v-bind:title="item.title" :index="index">
          <NewsBlock :data="item.attributes"/>
        </slide>


      </carousel-3d>
    </div>
    <v-container>
      <v-row>

      </v-row>
    </v-container>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
import NewsBlock from "@/components/NewsBlock";
import {Carousel3d, Slide} from 'vue-carousel-3d';
import axios from "axios";

export default {
  name: 'HomeView',
  components: {
    NewsBlock,
    HelloWorld,
    Carousel3d,
    Slide
  },
  data() {
    return {
      news: null
    }
  },
  mounted() {
    axios.get('http://localhost:1337/api/news?populate=*').then(res => {
      this.news = res.data.data
      console.log(res.data.data)
    }).catch(er => {
      console.error(er)
    })
  }
}
</script>
