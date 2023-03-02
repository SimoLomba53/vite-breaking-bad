<script>
export default {
    props: {
        type: String,
        name: String,
        pic:Array,
        form:String,
    }
}


</script>

<template>
    <li class="singlecard">
    <h2>{{ name }}</h2>
    <p>{{ type }}</p>
    <p>{{ form }}</p>
    <img v-for="image in pic" id="cardimage" :src="image.image_url" alt="">
    </li>
</template>

<style scoped>

#cardimage{
    width:100px;
}

.singlecard{
    list-style: none;
    
}

</style>
