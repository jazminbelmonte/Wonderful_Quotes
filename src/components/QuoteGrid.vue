<template>
    <div class="row">
        <ul>
            <app-quote @click.native="deleteQuote(this.index)" v-for="(quote, index) in quotes">
                {{quote}}
            </app-quote>
        </ul>
    </div>
</template>

<script>
  import Quote from './Quote.vue'
  export default {
    props: ["quotes"],
    components: {
      'app-quote': Quote
    },
    methods: {
      deleteQuote(index) {
        this.$emit('quoteDeleted', index)
      }
    }
  }
</script>
