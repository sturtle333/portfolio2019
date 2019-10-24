<template>
<div class="info" @mouseover="isHover = true;">
  <div class="emoji" :class="{hovering: isHover}">
    <slot name="icon"></slot>
  </div>
  <div class="text">
    <slot name="desc"></slot>
  </div>
</div>
</template>

<script>
export default {
  name: 'info',
  data () {
    return {
      isHover: false
    }
  }
}
</script>

<style scoped>
.info {
  display: flex;
  flex-directiom: row;

  font-size: 20px;
  width: 20em;

  transition: color 1s;
  -webkit-transition: color 1s;
}
.info:hover {
  color: white;
  border-radius: 30px;
  background-color: #54546c;
  font-weight: bold;

  padding-right: 1.4em;
}


.emoji {
  width: 1.4em;
  height: 1.4em;

  text-align: center;
  vertical-align: middle;

  border-radius: 30px;
  padding: 10px;

  background-color: #54546c;
}

.text {
  font-size: 1.2em;
}
</style>
