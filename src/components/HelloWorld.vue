<template>
  <div>
    <div class="footer">
      <svg v-if="screen > 768" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#0099ff" fill-opacity="1" d="M0,64L48,64C96,64,192,64,288,90.7C384,117,480,171,576,160C672,149,768,75,864,64C960,53,1056,107,1152,112C1248,117,1344,75,1392,53.3L1440,32L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path>
      <a xlink:href="mailto:vcaleb01@gmail.com" target="_blank">
        <text x="700" y="200" fill="white">vcaleb01@gmail.com</text>
      </a>
      <a xlink:href="https://github.com/valodagreat/" target="_blank">
        <g><text x="670" y="250" fill="white" class="icon_size">&#xf09b;</text></g>
      </a>
      <a xlink:href="https://twitter.com/valo_dagreat" target="_blank">
        <g><text x="720" y="250" fill="white" class="icon_size">&#xf099;</text></g>
      </a>
      <a xlink:href="https://www.facebook.com/valentine.ifedayo.3" target="_blank">
        <g><text x="770" y="250" fill="white" class="icon_size">&#xf09a;</text></g>
      </a>
      <a xlink:href="https://wa.me/2348108541029" target="_blank">
        <g><text x="820" y="250" fill="white" class="icon_size">&#xf232;</text></g>
      </a>
      <a xlink:href="www.linkedin.com/in/valentine-ifedayo-b2b0951b5" target="_blank">
        <g><text x="870" y="250" fill="white" class="icon_size">&#xf0e1;</text></g>
      </a>
      <text x="690" y="290" fill="white">© 2020 Ifedayo Valentine</text>
      </svg>
      <div v-if="screen < 768" class="footer_cont">
        <div class="footer_det">
          <a href="mailto:vcaleb01@gmail.com" class="gmail" target="_blank">vcaleb01@gmail.com</a>
          <div class="footer_links">
            <a href="https://github.com/valodagreat/" target="_blank">
              <span style="font-size: 2em;">
                <i class="fab fa-github"></i>
              </span>
            </a>
            <a href="https://twitter.com/valo_dagreat" target="_blank">
              <span style="font-size: 2em;">
                <i class="fab fa-twitter"></i>
              </span>
            </a>
            <a href="https://www.facebook.com/valentine.ifedayo.3" target="_blank">
              <span style="font-size: 2em;">
                <i class="fab fa-facebook"></i>
              </span>
            </a>
            <a href="https://wa.me/2348108541029" target="_blank">
              <span style="font-size: 2em;">
                <i class="fab fa-whatsapp"></i>
              </span>
            </a>
            <a href="www.linkedin.com/in/valentine-ifedayo-b2b0951b5" target="_blank">
              <span style="font-size: 2em;">
                <i class="fab fa-linkedin-in"></i>
              </span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      screen : screen.width
          }
  },
  mounted(){
    this.screen = screen.width
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="css">
  .icon_size{
    font-size: 2rem;
  }
  svg a{
    padding: 1rem;
  }
  .footer svg{
    height: 100%;
    width: 100%;
  }
  .footer_det a{
    color: white;
    text-decoration: none;
  }
  svg text {
    font-family: FontAwesome;
  }
  .footer_links a{
    padding: 0.5rem;
  }
  .gmail{
    text-align: center;
  }
  .footer_det{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .footer_cont{
    margin-left: auto;
    margin-right: auto;
  }
</style>
