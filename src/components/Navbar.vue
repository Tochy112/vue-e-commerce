<template>
  <div class="nav-container">
    <nav>
      <ul>
        <li>
          <router-link to="/">Men</router-link>
        </li>
        <li>
          <router-link to="/">Women</router-link>
        </li>
        <li>
          <router-link to="/">Kids</router-link>
        </li>
        <li>
          <router-link to="/">Sale</router-link>
        </li>
      </ul>

      <div class="img">
        <img src="../assets/allbirds-logo.svg" alt="Logo" />
      </div>

      <ul>
        <li>
          <router-link to="/">Sustainabilty</router-link>
        </li>
        <li>
          <router-link to="/">Rerun</router-link>
        </li>
        <li>
          <router-link to="/">Stores</router-link>
        </li>
        <li>
          <router-link to="/">Profile</router-link>
        </li>
        <li>
          <router-link to="/">About</router-link>
        </li>
        <li>
          <router-link to="/">Cart</router-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style scoped>
    .nav-container{
        padding-bottom: 40px;
    }
     nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
        position: fixed;
        background-color: #fff;
        width: 100vw;
        padding: 15px;
        z-index: 10;
     }
     nav ul li{
        list-style: none;
        display: inline;
        margin:0 20px;
     }
     nav .img{
        width: 100px;
     }
     nav img{
        width: 100%;
     }
     nav a{
        text-decoration: none;
        text-transform: uppercase;
        font-size: 15px;
        font-weight: bold;
        color:#3C4348;
     }
     nav a:hover{
      text-decoration: 1px solid #3C4348 underline;
     }
     /* nav a.router-link-exact-active {
        color: #42b983;
     } */
</style>
