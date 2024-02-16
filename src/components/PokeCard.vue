<template>

    

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Lato:wght@400;700&display=swap" rel="stylesheet">

    <div class="card">
        <div>
            <div class="image">
                <img :src="imageUrl" :alt="pokemon.name" />
            </div>
            <div class="name">
                <p><span class = "tag">#{{ pokemon.pokedex_number }}</span>{{pokemon.name}}</p>
            </div>
        </div>
        
        <div class="stats">
            <p>gen : {{ pokemon.generation }}</p>
            <p>sp atk : {{ pokemon.sp_attack }}</p>
            <p>sp def : {{ pokemon.sp_defense }}</p>
            <p>hp : {{ pokemon.hp }}</p>
            <p>atk : {{ pokemon.attack }}</p>
            <p>def : {{ pokemon.defense }}</p>
        </div>

    </div>






</template>
<script>
export default {
    emits: ['click'],
    props: {
        pokemon: {
            type: Object,
            required: true
        }
    },
    computed :{
        imageUrl(){
        return "/images/"+ this.pokemon.name.toLowerCase() + ".png";
    },
    }
    
    
}


      
    

</script>
<style scoped>
.card{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin: 1em;
    padding:1em;
    border-radius: 15px;
    background-color: rgb(1, 18, 110);
    margin-left: 5%;
    margin-right: 5%;
    height: 100px;
    color: white;
}
.tag{
    font-family: 'Lato', sans-serif; font-weight: 400;
    font-size: 20px;
    margin-right: 10px;
}
.name{
    margin-left: 70%;
    font-family: 'Lato', sans-serif; font-weight: 700;
    font-size: 22px;
    width: 15%;
}

.stats{
    display: flex;
    align-items: center;
    justify-content: space-between;
    text-align: center;
    font-family: 'Lato', sans-serif; font-weight: 400;
    font-size: 20px;
    width: 60%;
    margin-right: 2%;
}
.stats p{
    width: 10%
}
.stats p:nth-child(1){
    width: 20%;
    text-align: left;
    
}
.card > div:nth-child(1){
    display: flex;
    align-items: center;
    width: 10%;
    color: black;
    background-color: rgb(65, 85, 201);
    padding-right: 15%;
    border-radius: 15px;
    height: 90px;
}
.card div.image{
    display: block;
    height: 100%; 
}

</style>