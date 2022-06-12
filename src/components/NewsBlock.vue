<template>
  <v-card height="100%" style="border-radius: 0!important;">
    <v-img
        v-if="data.img.data!==null"
        height="100"
        :src="'http://localhost:1337'+ (data.img.data.attributes.url)"
    />
    <v-card-title>
      {{ data.title }}
    </v-card-title>
  </v-card>
</template>

<script>
export default {
  name: "NewsBlock",
  props: {
    data: {
      type: Object,
    }
  }
}
</script>

<style scoped>

</style>
