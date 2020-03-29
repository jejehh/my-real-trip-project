<template>
  <div id="trip">
      <img :src="trip.imageUrl" alt="" width="250" height="180">
      <p id="tip">{{trip.tip}}</p>
      <p id="title">{{trip.title}}</p>
      <p id="price">{{trip.price}}</p>
    <!-- <span>{{trip}}</span> -->
  </div>
</template>

<script>
 
export default {
    name: "trip",
    components: {

    },
    props: ['trip']
}


</script>


<style lang="scss">

#trip {
  border: 1px solid gainsboro;
  height: 300px ;
  margin-right: 15px;

}

#tip{
   margin: 5px 0 2px 10px;
   color: #848c94;
    font-size: 12px;
    height: 16px;
    letter-spacing: -.2px;
}

#title {
  margin-left: 10px;
  line-height: 20px;
  font-weight: bold;
  font-size: 14px;
  max-height: 40px;
}

#price{
  margin-left: 10px;
  color: #666d75;
  font-size: 14px;
  font-weight: 500;
  position: absolute;
  bottom:12px;
}

</style>
