<template>
<div class="container-fluid d-flex h-100 flex-column" id="app">
    <Header/>
    <div class="row bg-darl flex-fill d-flex justify-content-start">
        <SideNav/>
        <Main/>
  </div>

            <footer class="row">
                <div class="col" style="font-size:larger;">
                    --------------Footer--------------<br><br>
                </div>
            </footer>

</div>

</template>

<script>
import SideNav from "./components/sidebar";
import aCard from "./components/aCard";
import Header from "./components/header";
import Main from "./components/maincontent";


export default {
  name: 'App',
  components: {
        SideNav,
        aCard,
        Header,
        Main
    },

    mounted() {
        this.$nextTick(function() {
            console.log("We're ready to run")
        });
  }
}
</script>

<style>
html,body {
  height: 100%;
}

.flex-fill {
    flex:1;
}

.card {
    /* background: #222437; */
    background: #2C2C45;

    color: rgb(255, 255, 255);
}

input {
  width: 220px;
}

#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
