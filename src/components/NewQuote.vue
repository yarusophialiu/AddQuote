<template>
    <div id="row">
        <form action="">
            <div class="col-sm-8">  
                <label class="light-font-weight">Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 margin">  
                <button class="btn btn-primary light-font-weight" @click.prevent="createNew">
                    Add Quote
                </button>
            </div>
        </form>
    </div>
    
</template>

<script>
    export default {
        data: function() {
            return {
                quote: ''
            }
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded', this.quote)
                // reset this.quote
                this.quote =  ''
            }
        }
    }
</script>

<style>
    .margin {
        margin-top: 5px;
    }
    .light-font-weight {
        font-weight: 200;
    }

</style>