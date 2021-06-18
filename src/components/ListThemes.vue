<template>
  <div class="root">
    <ul class="list">
<!--      <li class="list-item" v-for="(title, index) in themes" :key="index">-->
      <li class="list-item" v-for="(inf, index) in info" :key="index">
        <div class="card-theme">
<!--          {{ title.title }}-->
          {{ inf.name }}
          <hr>
<!--          <span>Создано: {{title.date_create}}</span>-->
          <span>Создано: {{inf.created_at}}</span>
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
                date_create: '21.02.2014'},
               {title: 'Путешествия',
                date_create: '15.07.2016'}],
      info: null
    }
  },
  mounted(){
    this.axios
        .get('http://api-240521/api/desks')
        .then(response => (this.info = response.data))
  }

}
</script>

<style lang="scss" scoped>
@import "../assets/scss/variables";
  .list {
    display: flex;
    flex-wrap: wrap;
    //color: $main-color-list-item;
    list-style: none;
    padding-left: 0;

    &-item {
      margin-top: 15px;
      &:not(:last-child) {
        margin-right: 30px;
      }
    }
  }

  .card-theme {
    width: 165px;
    height: 80px;
    border: 3px solid #f55faa;
    border-radius: 15px;
    padding: 5px 10px;
    font-family: sans-serif;
    font-size: 16px;
    font-weight: 600;
    //color: #f55faa;
    span {
      font-size: 12px;
    }
    &:hover {
      color: #ffffff;
      background-color: #f55faa;
    }
  }

</style>