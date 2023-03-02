
 <script>
    export default{
        data(){
            return{
                term:"",
            };
        },
        
        emits:["searching"],

        methods: {
         clear() {
             this.term ="";
        },

         search(){
             this.$emit("searching",this.term);
        },
     },
    };

   
</script>

<template>
    <form @submit.prevent="">
    <div class="input-group mb-3">
             <input type="text" v-model="term" class="form-control" placeholder="Search items" aria-label="Recipient's username" aria-describedby="basic-addon2">
             <button type="button" @click="search">SEARCH</button>
             <button type="button" @click="clear">RESET</button>
    </div>
    </form>
</template>

<style scoped></style>
