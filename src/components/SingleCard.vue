<script>
export default {
    props: {
        type: String,
        name: String,
        pic:Array,
    }
}


</script>

<template>
    <h2>{{ name }}</h2>
    <p>{{ type }}</p>
    <img v-for="image in pic" id="cardimage" :src="image.image_url" alt="">
</template>

<style scoped>

#cardimage{
    width:100px;
}

</style>
