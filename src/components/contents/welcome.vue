<template>
<div class="contents-container-welcome">
    <div class="welcome-header">
      <p class="title">
        <span style="font-size: 1.5em; color: white;"> { </span>
        <span>Hello, World!</span>
        <span style="font-size: 1.5em; color: white;"> } </span>
      </p>
      <p class="subtitle">Developer portfolio</p>
    </div>
    <span class="content-description">Resently</span>
    <div class="welcome-content">
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
      <div></div>
    </div>
</div>
</template>

<script>
export default {
  name: 'Welcome'
}
</script>

<style>
.contents-container-welcome{
  display: flex;
  flex-direction: column;
  background-color: #e4e7ec;
  color: #263959;
  overflow: hidden;
}

.welcome-header {
  margin: 0;
  font-family: 'Inconsolate', sans-serif;
  font-size: 80%;
  letter-spacing: 10px;
  line-height: 6em;
  flex: inital;
  overflow: hidden;
}

.title {
  display: inline;
  font-size: 5em;
  margin: 0;
}
.title span {
  vertical-align: baseline;
}
.subtitle {
  font-size: 1.5em;
  margin: 0;
}


.content-description {
  font-size: 2em;
  align-self: flex-start;
  background-color: white;
}


.welcome-content {
  flex: 1 1;
  background-color: white;

  display: flex;
  flex-flow: row wrap;
  justify-content: space-around;
  align-content: space-around;
  align-items: center;
}
.welcome-content div {
  border: 3px solid #263959;
  width: 30%;
  height: 40%;
}


@media(max-width:1100px){
  .welcome-header {
    margin-top: 100px;
    text-align: left;
  }
  .title {
    font-size: 3em;
  }
  .subtitle {
    font-size: 3em;
  }


  .welcome-content {
    margin-bottom: 25%;
  }
}


@media(max-width:450px){
  .welcome-header {
    margin: 0;
    margin-bottom: 1em;
    line-height: 2em;
  }
  .title {
    display: inline;
    font-size: 1em;
    margin: 0;
  }
  .title span {
    display: block;
    vertical-align: baseline;
  }
  .subtitle {
    font-size: 1em;
    margin: 0;
  }


  .content-description {
    font-size: 0.5em;
  }

  .welcome-content div {
    width: 40%;
    height: 25%;
  }
}

@media(max-width:400px){
  .welcome-header {
    margin: 0;
    margin-bottom: 1em;
    letter-spacing: 5px;
    line-height: 2em;
  }
  .title {
    display: inline;
    font-size: 1em;
    margin: 0;
  }
  .title span {
    display: block;
    vertical-align: baseline;
  }
  .subtitle {
    font-size: 1em;
    margin: 0;
  }


  .content-description {
    font-size: 0.5em;
  }

  .welcome-content div {
    width: 40%;
    height: 25%;
  }
}
</style>
