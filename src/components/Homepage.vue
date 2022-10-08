<template>
  <div class="homepage">
    <div class="toolbar">
      <div class="logo">
        <img src="@/assets/logo.png" alt="logo"/>
      </div>
      <ActionButton action="Inscreva-se"
                    link="https://docs.google.com/forms/d/e/1FAIpQLSerFi5Jv7Zh70xrVXzH6426DRS09IRWhsluNVAiAqrHGHPP1w/viewform"/>
    </div>
    <div class="love">
      <img src="../assets/love.jpeg">
    </div>
    <div class="info">
      <span>Tenha um encontro verdadeiro com Aquele que te criou!</span>
    </div>
    <div class="video">
      <iframe width="700" height="350"
              src="https://www.youtube.com/embed/RD7ziUammxA">
      </iframe>
    </div>
<!--    <div class="images">-->
<!--      <div class="right">-->
<!--        <img src="../assets/2.jpg">-->
<!--        <img src="../assets/3.jpg">-->
<!--      </div>-->
<!--      <div class="right">-->
<!--        <img src="../assets/4.jpg">-->
<!--        <img src="../assets/5.jpg">-->
<!--      </div>-->
<!--    </div>-->
    <div class="info">
      <span>A cura de Deus através do testemunho de pessoas que já vivenciaram esta experiência.</span>
    </div>
    <div class="video">
      <iframe width="700" height="350"
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
            title="Dê uma olhada no nosso calendário de 2022!"
            subtitle="Coloque na sua agenda, programe-se e venha participar conosco."
            warn="As vagas são limitadas!"
        />
      </div>
      <div class="doc">
        <img src="../assets/calendar.jpg">
      </div>
    </div>
    <div class="join-team">
      <Banner
          title="Venha fazer parte da próxima equipe!"
          subtitle="Temos um encontro marcado com você!"
          warn="Vagas limitadas"
      >
        <div class="action">
          <ActionButton action="Garanta a inscrição"
                        link="https://docs.google.com/forms/d/e/1FAIpQLSerFi5Jv7Zh70xrVXzH6426DRS09IRWhsluNVAiAqrHGHPP1w/viewform"/>
        </div>
      </Banner>
    </div>
    <div class="whatsapp">
      <Banner
          title="Ficou alguma dúvida?"
          subtitle="Estamos disponíveis pelo WhatsApp."
      >
        <div class="action">
          <ActionButton action="Entre em contato"
                        link="https://api.whatsapp.com/send/?phone=556135430366&text=Ol%C3%A1%2C+interessei-me+pelo+projeto+e+gostaria+de+mais+detalhes.&type=phone_number&app_absent=0"/>
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
import { Options, Vue } from 'vue-class-component';
import ActionButton from './utils/ActionButton.vue';
import SocialNetwork from './utils/SocialNetwork.vue';
import Banner from './utils/Banner.vue';

@Options({
  components: {
    ActionButton, SocialNetwork, Banner,
  },
})
export default class Homepage extends Vue {}
</script>

<style scoped lang="scss">
.homepage {
  .toolbar {
    display: flex;
    align-items: center;
    justify-content: space-between;

    margin: 0 24px;

    .logo {
      img {
        width: 75px;
      }
    }
  }

  .love {
    display: flex;
    justify-content: center;
    margin: 24px 0;

    img {
      width: 20%;
      max-width: 300px;
    }
  }

  .images {
    display: flex;
    justify-content: center;
    margin-top: 48px;

    img {
      width: 300px;
      height: 200px;
      margin-left: 24px;
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

    padding-top: 32px;
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

  .join-team {
    margin-top: 16px;
  }

  .whatsapp {
    margin-top: 16px;
  }

  .footer {
    display: block;
    text-align: center;

    margin-top: 24px;

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

@media screen and (max-width: 420px) {
  .homepage {
    .calendar {
      display: block;

      .doc {
        display: flex;
        justify-content: center;
        margin-bottom: 16px;

        img {
          height: 250px;
        }
      }
    }
  }
}
</style>
