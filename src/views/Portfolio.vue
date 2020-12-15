<template>
    <div class="portfolio">
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
        <div class="portfolio-container">
            <h2 class="mb-5">Portfolio</h2>
            <div class="portfoliosite">
                <div class="portfolio-items my-5">
                    <img class="m-2" src="https://res.cloudinary.com/valodagreat/image/upload/v1603191180/roicsvm7o7z4yzabvnmv.png" alt="Horeca" width="300" height="300">
                    <div class="portfolio-data p-2 m-3">
                        <h3 class="mb-4">Horeca cloud</h3>
                        <p class="portfolio-desc">
                            A Website designed for Horeca cloud (Horeca Cloud is a Hospitality cloud based solution designed for Hotels, Restaurant and Cafes in Nigeria).
                        </p>
                        <span class="pr-2 ">
                            <b-button class="btnn" pill variant="light">
                                <a href="https://horecacloud.ng" target="_blank">View Site</a>
                            </b-button>
                        </span>
                    </div>
                </div>
                <hr class="port-hr">
                <div class="portfolio-items my-5">
                    <img class="m-2" src="https://res.cloudinary.com/valodagreat/image/upload/v1606585154/face-recog_yp8cvh.jpg" alt="Horeca" width="300" height="300">
                    <div class="portfolio-data p-2 m-3">
                        <h3 class="mb-4">Face Recognition App</h3>
                        <p class="portfolio-desc">
                            A Website designed for Horeca cloud (Horeca Cloud is a Hospitality cloud based solution designed for Hotels, Restaurant and Cafes in Nigeria).
                        </p>
                        <span class="pr-2 ">
                            <b-button class="btnn" pill variant="light">
                                <a href="https://horecacloud.ng" target="_blank">View Site</a>
                            </b-button>
                        </span>
                    </div>
                </div>
                <hr class="port-hr">
                <div class="portfolio-items my-5">
                    <img class="m-2" src="https://res.cloudinary.com/valodagreat/image/upload/v1606585671/clone_wcyotj.jpg" alt="Horeca" width="300" height="300">
                    <div class="portfolio-data p-2 m-3">
                        <h3 class="mb-4">Whatsapp Clone</h3>
                        <p class="portfolio-desc">
                            A Website designed for Horeca cloud (Horeca Cloud is a Hospitality cloud based solution designed for Hotels, Restaurant and Cafes in Nigeria).
                        </p>
                        <span class="pr-2 ">
                            <b-button class="btnn" pill variant="light">
                                <a href="https://valodagreat.github.io/whatsapp/" target="_blank">View Site</a>
                            </b-button>
                        </span>
                    </div>
                </div>
                <hr class="port-hr">
                <div class="portfolio-items my-5">
                    <img class="m-2" src="https://res.cloudinary.com/valodagreat/image/upload/v1606586217/screenshot-valodagreat-github-io-dashboard-1606586191068_f2skgi.png" alt="Horeca" width="300" height="300">
                    <div class="portfolio-data p-2 m-3">
                        <h3 class="mb-4">Employee Dashboard</h3>
                        <p class="portfolio-desc">
                            A Website designed for Horeca cloud (Horeca Cloud is a Hospitality cloud based solution designed for Hotels, Restaurant and Cafes in Nigeria).
                        </p>
                        <span class="pr-2 ">
                            <b-button class="btnn" pill variant="light">
                                <a href="https://valodagreat.github.io/dashboard/" target="_blank">View Site</a>
                            </b-button>
                        </span>
                    </div>
                </div>
                <hr class="port-hr">
            </div>
            <Footer />
        </div>

    </div>
</template>

<script>
import Footer from '../components/HelloWorld'
export default {
    name: "Portfolio",
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
    h3{
        color: white;
        font-family: 'Mukta', sans-serif;
    }
    .portfolio-desc{
        color: white;
        font-family: 'Mukta', sans-serif;
        font-size: large;
    }
    .portfoliosite{
        max-width: 800px;
        margin: 0px auto;
    }
    .portfolio-items{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    hr.port-hr{
        border: 1px solid white;
        width: 100%;
    }
    @media screen and (max-width:768px){
        .portfolio-items{
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
    }
    }
</style>