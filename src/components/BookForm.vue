<template>
  <div>
    <form class="" action="#" method="post">
      <input type="text" name="title" value="" placeholder="Book Title" v-model="bookTitle">
      <input type="text" name="author" value="" placeholder="Book Author" v-model="bookAuthor">
      <button type="submit" name="button" onsubmit="bookSubmit(bookTitle, bookAuthor)">Add Book</button>
    </form>
  </div>
</template>
<script>
export default {
  name: 'BookForm',
  props: ['books'],
  bookTitle: '',
  bookAuthor: '',
  data: function() {
    // let bookTitle = '';
    // let bookAuthor = '';
    return bookTitle, bookAuthor
  },
  methods: {
    bookSubmit: function(bookTitle, bookAuthor){
      this.$emit('addBook', bookTitle, bookAuthor);
    }
  }
}
</script>
<style lang="css">
  
</style>