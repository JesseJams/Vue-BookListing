<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <BookItem v-for="book in books" :book="book"></BookItem>
    </ul>
  </div>
</template>
<script>
import BookItem from './BookItem';
export default {
  name: "BookList",
  data: function data() {
      return {
        title: "All Books",
        books: [{
            title: 'Self-Reliance',
            author: 'Ralph Waldo Emerson'
          },
          {
            title: 'American Gods',
            author: 'Neil Gaiman'
          },
          {
            title: 'Amusing Ourselves to Death',
            author: 'Neil Postman'
          },
        ]
      };
  },
  components: {
    class: BookItem
  }
};
</script>
<style lang="css">
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}  
</style>