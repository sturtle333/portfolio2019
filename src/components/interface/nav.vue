<template>
<div class="nav-header-container" :style="{ 'background-color': Color, color: Color }">
  <div class="nav-header">
    <button :class="{'nav-activated': pg===0}" @click="setPage(0);"><span class="nav-emoji">👋</span><br>Welcome</button>
    <button :class="{'nav-activated': pg===1}" @click="setPage(1);"><span class="nav-emoji">📋</span><br>About</button>
    <button :class="{'nav-activated': pg===2}" @click="setPage(2);"><span class="nav-emoji">📚</span><br>Stack</button>
    <button :class="{'nav-activated': pg===3}" @click="setPage(3);"><span class="nav-emoji">🏆</span><br>Portfolio</button>
  </div>
</div>
</template>

<script>
export default {
  name:'Navigation',
  data() {
    return {
      Color: '#263959',
      dataList: ['#263959','#54546c','#1f4e5f','#333030']
    }
  },
  methods: {
    setPage: function(pg){
      this.$emit('setPage',pg);
      this.Color = this.dataList[pg];
    }
  },
  props: ['pg']
}
</script>

<style>
.nav-header-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  border-right: 30px solid white;
  width: 250px;
  height: 100%;
  transition: background-color 1s, color 0.3s;
  -webkit-transition: background-color 1s, color 0.3s;
}
.nav-header{
  display: flex;
  flex-direction: column;
  item-aligns: center;
  overflow: visiable;
  height: 80%;
}
.nav-header button{
  flex: 1;
  border: none;
  color: white;
  background-color: inherit;
  transition: background-color 1s, color 0.3s;
  -webkit-transition: background-color 1s, color 0.3s;
}
.nav-header button[class=""]:hover{
  background-color: #D8D8D8;
  color: black;
  font-size: 1.2rem;
  font-family: 'Inconsolate', sans-serif;
}
.nav-header .index{
  flex: 2;
}
.nav-header .nav-activated {
  font-weight: bold;
  background-color: #e4e7ec;
  color: inherit;
  font-size: 1.5em;
}
.nav-emoji {
  font-size: 2em;
}

@media(max-width:1000px) {
  .nav-header-container {
    width: 200px;
  }
}

@media(max-width:450px) {
  .nav-header-container {
    border-right: 10px solid white;
    width: 90px;
  }
  .nav-header button{
    font-size: 0.7em;
  }
  .nav-header button[class=""]:hover{
    font-size: 1rem;
  }
  .nav-header .index{
    flex: 2;
  }
  .nav-header .nav-activated {
    font-size: 1em;
  }
  .nav-emoji {
    font-size: 1em;
  }
}
</style>
