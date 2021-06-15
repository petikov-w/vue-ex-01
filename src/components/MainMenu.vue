<template>
    <div class="root">
        <ul class="list">
          <li class="list-item" v-for="(title, index) in titles" :key="index" @click="getItem(title)"> {{getTitle(title)}} </li>
        </ul>
    </div>

</template>

<script>
export default {
  name: 'MainMenu',
  data() {
    return {
       titles: [{title: 'Главная'},
                {title: 'Каталог'},
                {title: 'О нас'},
                {title: 'Контакты'}]
    }
  },
  methods: {
      getTitle(title) {
        return `${title.title}`;
      },
      getItem(title) {
         console.log(title.title);
      }
  }
}
</script>
<style lang="scss" scoped>
  @import "../assets/scss/variables";
  .list {
    display: flex;
    font-family: sans-serif;
    font-size: 18px;
    font-weight: 600;
    color: $main-color-list-item;
    list-style: none;
    outline: none;
    &-item {
      &:not(:last-child) {
        margin-right: 30px;
      }
      &:hover {
        color: $hover-color-list-item;
      }
    }
  }
</style>