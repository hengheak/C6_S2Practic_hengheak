<template>
  <div class="FullCard">
      <div v-for="fullNames in FullName" :key="fullNames" class="card-title">
        <h3>
            {{fullNames.firstName}}
            {{fullNames.lastName}}
        </h3>
        <p>{{fullNames.comment}}</p>
    </div>

  </div>
</template>

<script>
export default {
    props: {
        FullName:[]

    }
    }


</script>

<style>
.FullCard .card-title{
    width:17%;
    margin:0 auto;
    margin-top:3px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
}

</style>