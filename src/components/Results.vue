<template>
<div>
    <p >Reaction time = {{this.score}}  ms</p>
    <p class="rank">{{ rank }}</p>
</div>

</template>

<script>
export default{
props : ['score'],
data(){

    return{
        rank: null
    }
    
},
mounted(){
    if(this.score < 250){
        this.rank = "Ninja reflex"
    }
    else if(this.score <400){
        this.rank = "Good reflex"


    }
    else {
        this.rank = "slow"
    }
}


}
</script>

<style>
.rank{
    font-size: 1.4em;
    color:aquamarine;
    font-weight: bold;
}

</style>