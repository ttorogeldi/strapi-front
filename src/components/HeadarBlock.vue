<template>
  <v-card style="border-radius: 0!important;" color="#192A81" height="65">
    <div class="text-center">
      <MenuBlock
          :items="items"
          name="Посольство"
      />
      <MenuBlock
          :items="items2"
          name="Двусторонее отношение"
      />
      <MenuBlock
          :items="items3"
          name="Консульские вопросы"
      />
      <MenuBlock
          :items="items3"
          name="Экспортерам"
      />
      <MenuBlock
          :items="items3"
          name="Инвесторам"
      />
      <MenuBlock
          :items="items3"
          name="Туризм в Беларуси"
      />
    </div>
  </v-card>
</template>

<script>
import MenuBlock from "@/components/MenuBlock";

export default {
  name: "HeadarBlock",
  components: {MenuBlock},
  data: () => ({
    items: [
      {
        title: 'Посольство',
        link: '/ewe'
      },
      {title: 'Click Me'},
      {title: 'Click Me'},
      {title: 'Click Me 2'},
    ],
    items2: [
      {
        title: 'Click Me',
        link: '/ewe'
      },
      {title: 'Click Me'},
      {title: 'Click Me 2'},
    ],
    items3: [
      {
        title: 'Click Me',
        link: '/ewe'
      },
      {title: 'Click Me 2'},
    ]
  }),
}
</script>

<style scoped>

</style>
