
<style>
body {
  height: 100vh;
  padding: 0;
  margin: 0;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: black;
  height: 100%;
  overflow-x:hidden;
  overflow-y:hidden;
  font-family: 'Roboto Mono', monospace;
}

.selected-gif {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 75%;
}

@media only screen and (min-width : 480px) {
  .wrapper {
    display: grid;
    grid-template-columns: 27% 73%;
  }
}

</style>

<template>
<div id="app">
  <Header/>
  <div class="wrapper" >
    <div>
      <div>
          <SearchBar/>
      </div>
      <div class="selected-gif">
        <SelectedGif/>
      </div>
    </div>
    <div>
      <div>
        <GifList/>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import SelectedGif from './app/components/SelectedGif.vue';
import GifList from './app/components/GifList.vue';
import SearchBar from './app/components/SearchBar.vue';
import Header from './app/components/Header.vue';

export default {
  name: 'app',
  components: { SelectedGif, GifList, SearchBar, Header}
}
</script>
