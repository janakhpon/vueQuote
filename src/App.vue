<template>

  <div class="container">
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
     <button class="btn btn-primary" type="submit" @click="showAdd">CUSTOM QUOTE</button>
  </nav>

      <NewQuote @quoteAdded="newQuote" v-if="!show"></NewQuote>
      <p v-else></p>
    
    <Header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></Header>
   

    <QuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote"></QuoteGrid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import NewQuote from "./components/NewQuote.vue";
import QuoteGrid from "./components/QuoteGrid.vue";

export default {
  data: function() {
    return {
      quotes: ["Just a Quote to see something"],
      maxQuotes: 5,
      show:true
    };
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length >= this.maxQuotes) {
        return alert("Please delete Quotes first!");
      }
      this.quotes.push(quote);
      this.show = true;
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    },
    showAdd: function () {
            this.show = false;
    }
  },
  components: {
    Header,
    NewQuote,
    QuoteGrid
  }
};
</script>

<style>
body {
  background: #02182b;
  color: #fff;
}
</style>
