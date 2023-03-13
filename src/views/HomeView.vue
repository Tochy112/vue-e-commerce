<template>
  <div>
    <div class="home">
      <div class="home-content">
        <h1>Water Colors</h1>
        <p>
          Our Wool Runner Mizziles are back in new colors ready for the rain.
        </p>
        <div class="btn-div">
          <Button content="SHOP MEN" />
          <Button content="SHOP WOMEN" />
        </div>
      </div>
    </div>
    <!-- favourites section -->
    <HoverBox />
  </div>
</template>

<script>
import Button from '@/components/Button.vue'
import HoverBox from '@/components/HoverBox.vue'
export default {
  name: 'HomeView',
  components: {
    Button,
    HoverBox
  }
}
</script>

<style scoped>
.home {
  background-image: url(../assets/Wet_Option.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
}
h1 {
  font-size: 50px;
}
p {
  font-weight: bold;
}
.home-content {
  padding: 55vh 0 0 30px;
  color: #fff;
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.btn-div {
  display: flex;
  gap: 10px;
}

@media screen and (max-width: 780px) {
  .home {
    background-image: url(../assets/Wet_Option-Mobil.jpg);
  }
}
</style>
