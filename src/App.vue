<template>
  <v-app id="app">
    <v-container>
      <v-row>
        <v-col cols="1"/>
        <v-col cols="4">
          <div style="display: flex">
            <div class="mx-0"><v-img width="60" src="logo.svg"/></div>
            <div class="">Посольство Республики Беларусь<br>в Китайской Народной Республике</div>
          </div>
        </v-col>
        <v-col/>
      </v-row>
    </v-container>
    <HeadarBlock>
    </HeadarBlock>
    <router-view/>
  </v-app>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
<script>
import HeadarBlock from "@/components/HeadarBlock";

export default {
  components: {HeadarBlock}
}
</script>
