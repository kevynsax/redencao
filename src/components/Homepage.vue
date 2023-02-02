<template>
    <div class="homepage">
        <div class="toolbar">
            <div class="logo">
                <img src="@/assets/logo.png" alt="logo"/>
            </div>
            <ActionButton
                action="Faça sua inscrição"
                link="https://docs.google.com/forms/d/e/1FAIpQLSerFi5Jv7Zh70xrVXzH6426DRS09IRWhsluNVAiAqrHGHPP1w/viewform"/>
        </div>
        <div class="cover">
            <div class="background">
                <img src="../assets/cover_bg.jpg">
            </div>
            <div class="love">
                <img src="../assets/love.png">
            </div>
            <div class="subtitle">
                <span>Tenha um encontro verdadeiro <br/>com Aquele que te criou!</span>
            </div>
        </div>
        <div class="video">
            <iframe
                width="700" height="350"
                src="https://www.youtube.com/embed/RD7ziUammxA">
            </iframe>
        </div>
        <div class="images">
            <img src="../assets/1.jpg">
            <img src="../assets/3.jpg">
            <img src="../assets/4.jpg">
            <img src="../assets/5.jpg">
        </div>
        <div class="info">
            <span>A cura de Deus através do testemunho <br/> de pessoas que já vivenciaram esta experiência.</span>
        </div>
        <div class="video">
            <iframe
                width="700" height="350"
                src="https://www.youtube.com/embed/Vl4pym3JzbE">
            </iframe>
        </div>
        <div class="info">
            <span>Respostas, transformações, guerras vencidas.</span>
            <span>Permita-se viver mudanças profundas aqui.</span>
        </div>
        <div class="about">
            <span>Perdão</span>
            <span>Encontre sua verdadeira identidade</span>
            <span>Supere velhas crises e prejuízos que ainda o resistem</span>
            <span>Cura e restauração em todos os níveis (corpo, alma e espírito)</span>
            <span>Oportunidade de fazer a vida ter sentido</span>
            <span>Relação com amigos, familiares e outras pessoas</span>
            <span>Restauração familiar</span>
            <span>Despertamento de proposito</span>
            <span></span>
        </div>
        <div class="calendar">
            <div class="info">
                <Banner
                    title="Dê uma olhada no nosso calendário de 2023!"
                    subtitle="Coloque na sua agenda, programe-se e venha participar conosco."
                    warn="As vagas são limitadas!"
                />
            </div>
            <div class="doc">
                <img src="../assets/calendar.png">
            </div>
        </div>
        <div class="join-team">
            <Banner
                title="Venha fazer parte da próxima equipe!"
                subtitle="Temos um encontro marcado com você!"
                warn="Vagas limitadas"
                background="white"
            >
                <div class="action">
                    <ActionButton
                        action="Garanta sua inscrição"
                        link="https://docs.google.com/forms/d/e/1FAIpQLSerFi5Jv7Zh70xrVXzH6426DRS09IRWhsluNVAiAqrHGHPP1w/viewform"/>
                </div>
            </Banner>
        </div>
        <div class="whatsapp">
            <Banner
                title="Ficou alguma dúvida?"
                subtitle="Estamos disponíveis pelo WhatsApp."
                background="#C8FFEC"
            >
                <div class="action">
                    <ActionButton
                        action="Entre em contato"
                        link="https://api.whatsapp.com/send/?phone=556135430366&text=Ol%C3%A1%2C+interessei-me+pelo+projeto+e+gostaria+de+mais+detalhes.&type=phone_number&app_absent=0"
                        background="#58EF5D"
                    />
                </div>
            </Banner>
        </div>
        <div class="footer">
            <span>"Incrível o que o amor de Deus pode fazer"</span>
            <div class="networks">
                <SocialNetwork symbol="Facebook" link="https://www.facebook.com/redencaodf"/>
                <SocialNetwork symbol="Instagram" link="https://www.instagram.com/redencaodf/"/>
                <SocialNetwork symbol="YouTube" link="https://www.youtube.com/c/Reden%C3%A7%C3%A3oDF"/>
            </div>
            <div class="logo">
                <img src="@/assets/logo.png" alt="logo"/>
            </div>
        </div>
    </div>
</template>

<script>
import {Options, Vue} from 'vue-class-component';
import ActionButton from './utils/ActionButton.vue';
import SocialNetwork from './utils/SocialNetwork.vue';
import Banner from './utils/Banner.vue';

@Options({
    components: {
        ActionButton, SocialNetwork, Banner,
    },
})
export default class Homepage extends Vue {
}
</script>

<style scoped lang="scss">
.homepage {
    .toolbar {
        display: flex;
        align-items: center;
        justify-content: space-between;

        margin: 24px;

        .logo {
            img {
                width: 75px;
            }
        }
    }

    .cover {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        min-height: 440px;
        padding-bottom: 40px;

        z-index: 1;

        .love img {
            max-width: 300px;
        }

        .background img{
            position: absolute;
            background-image: url("../assets/cover_bg.jpg");
            top: 0;
            left: 0;
            object-fit: cover;
            object-position: 50% 80%;
            z-index: -1;
            width: 100%;
            height: 600px;
            filter: brightness(.8);

            -webkit-mask-image:-webkit-gradient(linear, left top, left bottom, from(rgba(0,0,0,1)), to(rgba(0,0,0,0)));
            mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
        }

        .subtitle{
            text-align: center;
            color: white;
            text-shadow: 2px 0 10px rgb(0, 0, 0);
            font-weight: bold;
            font-size: 24px;
        }
    }


    .images {
        margin-top: 48px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;

        img {
            margin: 16px;
            width: 400px;
        }
    }

    .action {
        display: flex;
        justify-content: center;

        margin-top: 16px;
    }

    .info {
        margin-top: 36px;

        span {
            display: block;
            font-weight: bold;
            text-align: center;
            color: darkgray;
        }
    }

    .video {
        display: flex;
        justify-content: center;

        padding: 32px 0;
    }

    .about {
        padding-top: 32px;

        span {
            display: block;
            text-align: center;
            margin-top: 4px;

            &:first-child {
                margin-top: unset;
                font-weight: bold;
            }
        }
    }

    .calendar {
        display: flex;
        justify-content: space-around;

        background-color: whitesmoke;
        margin-top: 32px;

        .info {
            span {
                display: block;
                margin-top: 16px;
                text-align: center;

                &:first-child {
                    margin-top: unset;
                    font-weight: bold;
                }
            }

            .warn {
                color: darkred;
            }
        }

        .doc {
            display: flex;
            align-items: center;

            img {
                height: 400px;
            }
        }
    }

    .footer {
        display: block;
        text-align: center;

        padding: 40px 0;

        background: #989898;

        span{
            font-weight: bold;
        }

        .networks {
            display: flex;
            justify-content: center;
            margin-top: 16px;

            > * {
                margin: 0 4px;
            }
        }

        .logo {
            display: flex;
            justify-content: center;

            margin-top: 32px;

            img {
                width: 100px;
            }
        }
    }
}

@media screen and (max-width: 428px) {
    .homepage {
        .calendar {
            display: block;

            .doc {
                display: flex;
                justify-content: center;
                margin-bottom: 16px;
            }
        }
    }
}
</style>
