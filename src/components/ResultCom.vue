<template>
   <div class="result">
        <div class="title">{{results[resultIndex].title}}</div>
        <div class="desc">
            {{results[resultIndex].desc}}
        </div>
    </div>
</template>

<script>
export default {
name: 'ResultCom',
props:{results:{
    type: Array
}
,totalCorrect:{
    type: Array
}},
data(){

},
methods:{

},
computed:{
    resultIndex(){
        let index = 0;
// e: element, i: index
    this.results.forEach((e, i) => {
    if(e.min <= this.totalCorrect && e.max >= this.totalCorrect ){
        index = i;

    }
});

        return index;
    }
}
}
</script>

<style>

</style>