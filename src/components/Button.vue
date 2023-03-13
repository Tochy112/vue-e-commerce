<template>
  <div>
    <button :style="{backgroundColor: bgcolor, color: color}">
        {{ content }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'Button',
  props: {
    content: String,
    color: String,
    bgcolor: String
  }
}
</script>

<style scoped>
button {
  color: #3c4348;
  background-color: #fff;
  border: 1px solid #fff;
  padding: 15px;
  max-width: max-content;
  font-weight: bold;
  font-size: medium;
  transition: all .2s ease-in-out;
  cursor: pointer;
  border-radius: 5px;
}
button:hover{
    background-color: #3c4348;
    color: #fff;
    border: 1px solid #3c4348;
}
</style>
