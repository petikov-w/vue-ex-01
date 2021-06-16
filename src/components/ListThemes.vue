<template>
  <div class="root">
    <ul class="list">
      <li class="list-item" v-for="(title, index) in themes" :key="index">
        <div class="card-theme">
          {{ title.title }}
          <hr>
          <span class="sas">Создано: {{title.date_create}}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ListThemes",
  data() {
    return {
      themes: [{title: 'Природа',
                date_create: '11.08.2013'},
               {title: 'IT',
                date_create: '17.01.2014'},
               {title: 'Книги',
                date_create: '02.01.2014'},
               {title: 'Журналы',
                date_create: '21.02.2014'}]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
.list {
  display: flex;
  //color: $main-color-list-item;
  list-style: none;
  padding-left: 0;
  &li {
    margin-right: 30px;
  }
  &-item {
    &:not(:last-child) {
       margin-right: 30px;
     }

}
  .card-theme {
    border: 3px solid #f55faa;
    border-radius: 15px;
    padding: 5px 10px;
    font-family: sans-serif;
    font-size: 16px;
    font-weight: 600;
    color: #f55faa;
    &:hover {
       color: #ffffff;
       background-color: #f55faa;
     }
  }
  .sas {
    font-size: 12px;
    color: #8b8b89;
    &:hover {
      color: #ffffff;
    }
  }
}
</style>