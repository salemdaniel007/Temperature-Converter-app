<template>
    <div class="container">
        <div>
            <form class="temperature">
                <label for="degrees">Degrees</label>
                <input type="text" v-model="temperature">
                    <label class="left" for="from">From</label>
                    <select name="Temperatures" id="Temperature" @change="changeTemp">
                            <option v-for='type in selected' :key='type'>{{ type }}</option>
                    </select>
                    <button @click.prevent="cToF" class="convert" value="submit" type="submit">Convert</button>
            </form> 
            <div class="result">
                            <p>Result</p>
                            <h2 class="inset"> {{ result }}</h2>
                 </div>       
        </div>
    </div>
</template>

<script>
// import { mapActions } from 'vuex';

export default {
    name: 'Main',
    // methods: {
        //  ...mapActions(['cToF']),
        // changeTemp: function(e){
        //     console.log("Show "+e.target.value+ " fields")
        //     if (e.target.value == 'Farenheit'){
        //       this.$store.commit('fTrue');
        //       this.$store.commit('cFalse');
        //     }else if (e.target.value == 'Celsius') {
        //       this.$store.commit('cTrue');
        //       this.$store.commit('fFalse');
        //     }
        // },
    //     storeTemp: function(e) {
    //         this.$store.getters.temp = e.target.value
    //     }
    // },
    // computed: {
    //     selected () {
    //         return this.$store.getters.selected
    //     },
    //     result () {
    //         return this.$store.getters.result
    //     },
    //     temp () {
    //         return this.$store.getters.temp
    //     },
    //     temperature: {
    //         get () {
    //         return this.$store.getters.temperature
    //         },
    //         set (value) {
    //         this.$store.commit('updateTemp', value);
    //         }
    //     }
    // }
    

}
</script>

<style scoped>
.container {
    padding: 2px 16px;
    margin: auto;
    width: 500px;    
    height: 400px;
    transition: 0.3s;
    /* box shadow made the box */
    box-shadow: 0 0 1rem 0 rgba(0, 0, 0, .2); 
    border-radius: 5px;
    z-index: 1;
    background: inherit;
    overflow: hidden;
	background-position: right;
    backdrop-filter: blur(5px);
    margin-top: -2rem;
}

.result {
    display: flex;
    margin: auto;
    margin-top: 6rem;
}

result p {
     margin-bottom: 1px;
}

.result h2 {
    margin: auto;
    margin-bottom: 1rem;
    margin-left: .4rem;
}

temperature {
    display: flex;
    justify-content: space-between;
    height: 3rem;
    margin-top: 2rem;
}

p {
    color: rgb(133, 124, 118);
    font-size: 1rem;
    color: rgb(34, 52, 112);
    margin-left: 5px;
}

label {
    font-size: 1rem;
    color: rgb(34, 52, 112);
    margin: 10px 10px 0 0px;
}

.left {
    margin-left: 15px;
}
.temperature select {
    padding: 11px 5px;
    background-color: #959fd4;
    color: rgb(239, 236, 243);
    border: 1px solid #959fd4;
    font-weight: 750;
    border-radius: 5px;
    margin: 0 10px  20px 0;
    margin-top: 2rem;
}

h1 {
    text-align: center;
    margin: auto;
    margin-top: 2rem;
    padding: 2rem;
    color: rgb(45, 50, 66);
}

h3 {
    margin-top: 17rem;
    text-align: center;
    color: rgb(54, 50, 54);
    
}

input[type="text"] {
  padding: 12px;
  border: 1px solid #eef0f5;
  outline: 0;
  border-radius: 5px;
  border-style: inset;
  background: rgb(247, 245, 242);
  color: rgb(228, 192, 228);
}

.convert {
    background: #8d97ca;
    color: #fff;
    padding: 11px 5px;
    background-color: #959fd4;
    color: rgb(239, 236, 243);
    border: 1px solid #959fd4;
    font-weight: 750;
    border-radius: 5px;
    border: 1px white solid;
    cursor: pointer;
    width: 67px;
    height: 2.7rem;
    margin: 15px;
}

#Temperature {
    width: 100px;
    border: black;
    border-style: solid;
}

h2.inset {
    border-radius: 5px;
    border-style: inset;
    width: 300px;
    height: 3rem;
    padding: 4px;
    background: rgb(247, 245, 242);
    color: #303a6d;
}

.card:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

</style>