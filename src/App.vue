<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Julius+Sans+One&display=swap');

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    overflow-x: hidden;
    
  }

  body {
    background-color: black;
    height: 100%;
    font-family: 'Julius Sans One', sans-serif;
  }

  .slider::-webkit-scrollbar {
    width: 6px;
    height: 6px;
  }
  .slider::-webkit-scrollbar-track {
    border-radius: 10px;
    background: transparent;
  }
  .slider::-webkit-scrollbar-thumb{
    border-radius: 10px;
    background: gray;
  }
</style>
