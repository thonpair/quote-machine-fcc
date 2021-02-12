<template>
  <div id="quote-box">
      <div id="quote">
      <div id="text">
          {{ quote }}
      </div>
      <div id="author">
          {{ author }}
      </div>
      </div>
      <div id="buttons">
        <button id="new-quote" v-on:click="getQuote">New Quote</button>
        <a href="https://twitter.com/intent/tweet" target="_blank" id="tweet-quote">Tweet it !</a>
      </div>
  </div>
</template>

<script>
import quotes from './../../static/quotes.json'
export default {
    data(){
        return{
            quote: String,
            author: String
        }
    },
    methods:{
        getQuote(){
            const random = Math.floor(Math.random() * Math.floor(quotes.length))
            const randomQuote = quotes[random];
            this.quote = randomQuote.quote;
            this.author = randomQuote.author;
        }
    },
    created(){
        this.getQuote();
    }
}
</script>

<style>
#quote-box{
    width: 400px;
    margin: auto;
    border: 1px solid grey;
    border-radius: 20px;
    padding: 20px;
}
#quote{
    height: 150px;
}
#author{
    text-align: right;
    font-style: italic;
}

#buttons{
    display: flex;
    justify-content: center
}

#new-quote, #tweet-quote{
    margin: 0px 30px;
}

#tweet-quote{
    padding-top: 5px;
}
</style>