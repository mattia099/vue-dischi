<template>
  <div class="card">
    <figure class="poster">
      <img :src="card.poster">
    </figure>
    
    <h4 class="title">
      {{ card.title }}
    </h4>

    <p class="author">
      {{ card.author }}
    </p>

    <p class="year">
      {{card.year}}
    </p>
  </div>
</template>

<script>
export default {
    props :{
        card : Object
    } 
}
</script>

<style lang="scss" scoped>
    .card{
        text-align: center;
        width: 18%;
        background-color: #2E3A46;
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-top: 30px;
        margin-bottom: 10px;
        gap: 10px;
        .poster{
            width: 160px;
        }
        .title{
            color: white;
            text-transform: uppercase;
        }
        .author, .year{
            color: grey;
        }

    }
</style>