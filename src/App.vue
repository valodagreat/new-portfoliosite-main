<template>
  <div id="app">
      <nav class="navybar">
        <div class="brand-title"><router-link to="/"><b-icon icon="code-slash" font-scale="1.2"></b-icon> 𝓥𝖆𝖑𝖔𝖊𝖜</router-link></div>
        <a href="#" @click="toggle" class="toggle-button">
          <span class="bar"></span>
          <span class="bar"></span>
          <span class="bar"></span>
        </a>
        <div class="navybar-links">
          <ul>
            <li v-for="linkName in linkNames" :key="linkName">
              <router-link :to="linkName | lowercase">{{linkName}}</router-link>
            </li>
          </ul>
        </div>
      </nav>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: "App",
  data(){
    return {
      linkNames: ['About','Portfolio','Contact']
    }
  },
  filters: {
    lowercase(v){
      return v.toLowerCase()
    }
  },
  methods: {
    toggle(){
      const navybar = document.getElementsByClassName('navybar-links')[0];
      navybar.classList.toggle('active')
    }
  }
}
</script>

<style>
*{
  box-sizing: border-box;
}
body {
  font-family: Avenir, Helvetica, Arial, sans-serif !important;
  -webkit-font-smoothing: antialiased !important;
  -moz-osx-font-smoothing: grayscale !important;
  margin: 0;
  padding: 0;
}
.navybar{
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #007bff;
  color: white;
  position: sticky;
  top: 0px;
  left: 0px;
  z-index: 100;
  padding: 1rem;
}
.brand-title{
  font-size: 2.5rem;
  margin: .5rem;
}
.brand-title a{
  text-decoration: none;
  color: white;
}
.brand-title a:hover{
  text-decoration: none;
  color: white;
}
.router-link-exact-active {
      color: white;
}
.navybar-links ul{
  margin: 0;
  padding: 0;
  display: flex;
}
.navybar-links li{
  list-style: none;
}
.navybar-links li a{
  text-decoration: none;
  color: white;
  padding: 1rem;
  display: block;
  font-size: 1.2rem;
}
.navybar-links li:hover{
  background-color: #2d8dfa;
}
.toggle-button{
  position:absolute;
  top: 2.75rem;
  right: 2rem;
  display: none;
  flex-direction: column;
  justify-content: space-between;
  height: 21px;
  width: 30px;
  
}
.toggle-button .bar{
  height: 4px;
  width: 100%;
  background-color: white;
  border-radius: 10px;
}
@media screen and (max-width:768px){
  .toggle-button{
    display: flex;
  }
  .navybar-links{
    display:none;
    width: 100%;
  }
  .navybar{
    flex-direction: column;
    align-items:flex-start;
  }
  .navybar-links ul{
    flex-direction: column;
    width: 100%;
  }
  .navybar-links li{
    text-align: center;
  }
  .navybar-links li a{
    padding: .5rem 1rem;
  }
  .navybar-links.active{
    display: flex;
    background-color: #0099ff;
  }
}
</style>
