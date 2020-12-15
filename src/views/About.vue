<template>
  <div class="about">
    <Particles
      id="tsparticles"
      class="particles"
      :options="{
            background: {
                color: {
                    value: '#007bff'
                }
            },
            fpsLimit: 60,
            interactivity: {
                detectsOn: 'canvas',
                events: {
                    onClick: {
                        enable: true,
                        mode: 'push'
                    },
                    onHover: {
                        enable: true,
                        mode: 'repulse'
                    },
                    resize: true
                },
                modes: {
                    bubble: {
                        distance: 400,
                        duration: 2,
                        opacity: 0.8,
                        size: 40
                    },
                    push: {
                        quantity: 4
                    },
                    repulse: {
                        distance: 200,
                        duration: 0.4
                    }
                }
            },
            particles: {
                color: {
                    value: '#ffffff'
                },
                links: {
                    color: '#ffffff',
                    distance: 150,
                    enable: true,
                    opacity: 0.5,
                    width: 1
                },
                collisions: {
                    enable: true
                },
                move: {
                    direction: 'none',
                    enable: true,
                    outMode: 'bounce',
                    random: false,
                    speed: 6,
                    straight: false
                },
                number: {
                    density: {
                        enable: true,
                        value_area: 800
                    },
                    value: 80
                },
                opacity: {
                    value: 0.5
                },
                shape: {
                    type: 'circle'
                },
                size: {
                    random: true,
                    value: 5
                }
            },
            detectRetina: true
        }"
    />
    <div class="about-container">
      <div class="abt-scnd-container">
        <div class="img-container pt-3 px-3">
          <img src="https://res.cloudinary.com/valodagreat/image/upload/v1606254253/caleb_r40hjv.jpg" alt="Valoew image" width="200" height="200">
        </div>
        <div class="abt-intro-text pt-3 px-3">
          <h2 class="pb-2">About me</h2>
          <p>Fullstack Web Developer skilled at designing sites,applications and writing clean code. I enhance applications and improve performance through testing and validations against requirements and performance standards.</p>
        </div> 
      </div>
      <div class="abt-scnd-cont">
        <div class="abt-scnd-text px-3">
          <p>I'm good at implementing successful content based on user needs</p>
          <p>I'm also skilled at completing daily assignments and contributing to team success.Always willing to take on any tasks.I adapt quickly to new needs and policies.</p>
        </div>
      </div>
      <div class="skills-cont p-2">
        <h2 class="p-3">Programming skills</h2>
        <div class="lang-cont">
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606564407/view_bbua3d.png" size="8rem"></b-avatar>
            <h4 class="py-2">Vue Js</h4>
          </div>
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606564695/react_elymwo.png" size="8rem"></b-avatar>
            <h4 class="py-2">React Js</h4>
          </div>
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606564828/js_znbofw.png" size="8rem"></b-avatar>
            <h4 class="py-2">Vanilla Js</h4>
          </div>
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606565066/node_krgy6o.png" size="8rem"></b-avatar>
            <h4 class="py-2">Node Js</h4>
          </div>
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606565242/postgres_zid3kr.png" size="8rem"></b-avatar>
            <h4 class="py-2">PostgreSQL</h4>
          </div>
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606565472/mongo_ouezgn.png" size="8rem"></b-avatar>
            <h4 class="py-2">MongoDB</h4>
          </div>
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606565722/sass_rqrwn6.png" size="8rem"></b-avatar>
            <h4 class="py-2">SCSS</h4>
          </div>
          <div class="lang-items">
            <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606565846/firebase_zblnoo.png" size="8rem"></b-avatar>
            <h4 class="py-2">Firebase</h4>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from '../components/HelloWorld'

export default {
  components: {
        Footer
    },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Mukta&display=swap');
  .particles{
    position: fixed;
    height: 100%;
    width: 100%;
    z-index: -1;
  }
  .abt-scnd-container{
    display: flex;
    justify-content:space-between;
    align-items: center;
    max-width: 750px;
    margin: 0px auto;
    min-height: 50vh;
  }
  .skills-cont{
    max-width: 750px;
    margin: 0px auto;
    text-align: center;
  }
  .lang-cont{
    display: flex;
    -webkit-box-pack: center;
    justify-content: center;
    flex-flow: row wrap;
  }
  .lang-items{
    position: relative;
    margin: 1.2rem;
  }
  .abt-scnd-cont{
    display: flex;
    justify-content:space-between;
    align-items: center;
    max-width: 750px;
    margin: 0px auto;
  }
  .abt-intro-text,.abt-scnd-text,.skills-cont h2,.lang-items h4{
    color: white;
    font-family: 'Mukta', sans-serif;
  }
  .abt-intro-text p,.abt-scnd-text p{
    font-size: large;
  }
  @media screen and (max-width:768px){
    .abt-scnd-container{
    display: flex;
    flex-direction: column;
    justify-content:space-between;
    align-items: center;
  }
  .abt-scnd-container h2{
    text-align:center;
  }
  }
</style>