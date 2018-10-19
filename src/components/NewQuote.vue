<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Quote</label>
                <textarea v-model="quote" class="form-control" rows="3" placeholder="This is a quote"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <button @click.prevent="createNew" class="btn btn-primary">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
  export default {
    data: function() {
      return {
        quote: " "
      };
    },
    methods: {
      createNew() {
        this.$emit('quoteAdded', this.quote)
        this.quote = ""
      }
    }
  }
</script>
