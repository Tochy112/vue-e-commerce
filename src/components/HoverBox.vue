<template>
  <div class="container">
    <h2 style="text-align:center; margin: 20px auto;">Our Favourites</h2>
    <div class="wrapper">
      <div class="parent-box" :key="data.id" v-for="data in box_data">
        <div class="img">
          <img :src="data.image" alt="images" />
        </div>
        <div class="box-footer">
          <h2>{{ data.footer1 }}</h2>
          <hr />
          <p>{{ data.footer2 }}</p>
        </div>
        <div class="child-box" >
           <div class="btn-div">
                <Button content="SHOP MEN" />
                <Button content="SHOP WOMEN" />
           </div>
        </div>
    </div>
    </div>
  </div>
</template>

<script>
import Asset1 from '@/assets/WRUM-Women__1_.jpg'
import Asset2 from '@/assets/sneaker1.jpg'
import Asset3 from '@/assets/Women_s_Breezers.avif'
import Button from '@/components/Button.vue'

export default {
  name: 'HoverBox',
  components: {
    Button
  },
  data () {
    return {
      box_data: [
        {
          id: 1,
          image: Asset1,
          footer1: 'Wool Runner',
          footer2: 'Cozy Sneaker'
        },
        {
          id: 2,
          image: Asset2,
          footer1: 'Tree Runner',
          footer2: 'Light and Breezy Sneaker'
        },
        {
          id: 3,
          image: Asset3,
          footer1: 'Tree Breezer',
          footer2: 'Breezy Flat'
        }
      ]
    }
  }
}
</script>

<style scoped>
.wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.parent-box {
  width: 400px;
  height: 500px;
  margin: 30px auto;
  box-shadow: rgb(51, 51, 51,0.5) 5px 0px 9px 0px;
  position: relative;
}
.img {
  height: 400px;
  width: 100%;
}
img {
  height: 100%;
  width: 100%;
  transition: all .5s ease-in-out;

}
.box-footer {
  padding: 20px 15px;
}
hr{
  color: #333;
}
h2, p{
    color: #333;
}
.child-box{
    background-color: rgba(51, 51, 51,0.5);
    width: 400px;
    height: 400px;
    position: absolute;
    bottom: 100px;
    display: none;
}
.parent-box:hover .child-box,
.parent-box:hover img{
    display:block;
    transform:scale(101%);
}
.btn-div{
    display: flex;
    flex-direction: column;
    text-align: center;
    margin: 35% auto;
    gap: 10px;
}
</style>
