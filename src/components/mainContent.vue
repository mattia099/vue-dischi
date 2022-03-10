<template>
  <main>
    <div class="card-wrapper">
      <cardItem v-for="(element,index) in cardList" :key="index" :card="element" />
    </div>
  </main>
</template>

<script>
import cardItem from './cardItem.vue'
export default {
    components :{
      cardItem,
    },

    data : function(){
      return{
        cardList : []
      }
    },

    methods :{
        axiosGet : function(){
            require('axios').get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( (res) => {
                this.cardList = res.data.response;
              })
        }
    },
    created(){
      this.axiosGet();
    }
}
</script>

<style lang="scss" scoped>
    main{
      background-color: #1E2D3B;
      height: calc(100vh - 75px);
      .card-wrapper{
        padding-top: 60px;
        max-width: 1160px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
      }
    }
</style>