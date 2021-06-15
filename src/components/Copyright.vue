<template>
    <div class="root">
      <a :href="link"><span>{{getTitle}}</span></a>
    </div>
</template>

<script>
export default {
  name: 'Copyright',
  data() {
    return {
       titles: 'Petikov Studio',
       years:  '2020-2021',
       link: 'https://kroxdev.ru'}
  },
  computed: {
    getTitle() {
      return `Copyright \u00A9 ${this.titles} ${this.years}`;
    }
  }
}
</script>
<style lang="scss" scoped>
@import "../assets/scss/variables";
    span {
      font-family: sans-serif;
      font-size: 14px;
      font-weight: 600;
      color: $copyright-color;
    }
</style>