<template>
 <div class="comment"> 
     <p>Made by Paul</p>
    <div class="second"> 
        <p>KING ❤️</p>
    </div>
</div>
</template>



<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
.comment {
    margin: auto;
    display: flex;
    color: #172886;
    font-size: 1.4rem;
    text-align: center;
    justify-content: center;

}

.second {
    display: flex;
    flex-direction: column;
    color: red;
    text-align: justify;
    justify-content: space-around;
    margin: 0 7px;
}
</style>