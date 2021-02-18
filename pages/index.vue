<template>
  <div class="container">
    <background-video :srcVideo="bgVideo" />
    <!-- Profile -->
    <div class="profile">
      <glass-card>
        <avatar :image="imgProfile" description="Foto de perfil: Dev Rafael Oliveira." />
        <h3>Rafael Pereira Oliveira</h3>
        <h4>Desenvolvedor Fullstack</h4>
      </glass-card>
    </div>
    
    <div class="main">
      <scroll>
        <!-- Introduction -->
        <glass-card class="mb-3" id="home">
          <h2 class="title">Hello, Night City!</h2>
          <p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy. Various versions have evolved over the years, sometimes by accident, sometimes on purpose (injected humour and the like).</p>
          <separator />
          <div class="row">
            <div class="col">
              <span class="subtitle">Informações Pessoais</span>
              <div>
                <span>Nome</span>
                <span>Rafael Pereira Oliveira</span>
              </div>
              <div>
                <span>Idade</span>
                <span>23 Anos</span>
              </div>
              <div>
                <span>Endereço</span>
                <span>Rio Grande do Sul, Viamão</span>
              </div>
              <div>
                <span>E-mail</span>
                <span>dev.rafael.oliveira@gmail.com</span>
              </div>
            </div>
            <div class="col">
              <span class="subtitle">Idiomas</span>
              <score-balls :score="9" title="português" label="fluente" />
              <score-balls :score="6" title="ingles" label="intermediário" />
            </div>
          </div>
          <separator />
          <div class="row">
            <div class="col">
              <span class="subtitle">Habilidades Profissionais</span>
              <bar-score :score="95" title="Javascrip" legend="mestre">
                <js-icon />
              </bar-score>
              <bar-score :score="95" title="NodeJS" legend="mestre">
                <node-icon />
              </bar-score>
              <bar-score :score="95" title="Django" legend="mestre">
                <dj-icon />
              </bar-score>
              <bar-score :score="95" title="HTML5" legend="mestre">
                <html-icon />
              </bar-score>
              <bar-score :score="95" title="Sass" legend="mestre">
                <sass-icon />
              </bar-score>
              <bar-score :score="95" title="SQL" legend="mestre">
                <db-icon />
              </bar-score>
            </div>
            <div class="col">
              <span class="subtitle">Habilidades Extras</span>
              <checklist />
            </div>
          </div>
        </glass-card>

        <!-- Work Experiences -->
        <glass-card class="mb-3" id="experience">
          <h2>Experiência</h2>
          <timeline label="2015 - 2015" title="Teste de software" subtitle="Procergs" description="Lorem ipsum" />
          <separator />
          <h2>Formação</h2>
          <timeline label="2015 - 2015" title="Teste de software" subtitle="Procergs" description="Lorem ipsum" />
        </glass-card>

        <!-- References -->
        <glass-card class="mb-1" id="reference">
          <h2>Referências</h2>
          <separator />
          <h2>Clientes</h2>
        </glass-card>

        <!-- Interests -->
        <glass-card class="mb-1" id="interests">
          <h2>Interesses</h2>
        </glass-card>

        <!-- Contact -->
        <glass-card id="contact">
          <contact-section />
        </glass-card>
      </scroll>
    </div>

    <nav-menu />
  </div>
</template>

<script>
// assets
import bgVideo from '~/assets/videos/synthwave-video.mp4'
import imgProfile from "~/assets/images/profile.png";
import JsIcon from "~/icons/JsIcon";
import NodeIcon from "~/icons/NodeIcon";
import HtmlIcon from "~/icons/HtmlIcon";
import SassIcon from "~/icons/SassIcon";
import DbIcon from "~/icons/DbIcon";
import DjIcon from "~/icons/DjIcon";

// components
import BackgroundVideo from '~/components/BackgroundVideo'
import GlassCard from "~/components/GlassCard";
import Avatar from "~/components/Avatar";
import Scroll from "~/components/Scroll";
import Separator from "~/components/Separator";
import ScoreBalls from "~/components/ScoreBalls";
import BarScore from "~/components/BarScore";
import Checklist from "~/components/Checklist";
import Timeline from "~/components/Timeline";
import NavMenu from "~/components/NavMenu";

// layout
import ContactSection from '~/layouts/ContactSection'

export default {
  components: {
    ContactSection,
    NavMenu,
    BackgroundVideo,
    GlassCard,
    Avatar,
    Scroll,
    Separator,
    ScoreBalls,
    Timeline,
    Checklist,
    BarScore,
    JsIcon,
    NodeIcon,
    HtmlIcon,
    SassIcon,
    DbIcon,
    DjIcon
  },
  data () {
    return {
      imgProfile,
      bgVideo
    }
  }
}
</script>

<style>
.container {
  padding: 36px;
  margin: 0 auto;
  height: 100vh;
  display: grid;
  overflow: hidden;
  grid-template-areas:
    'header header header header header header'
    'menu main main main main right'
    'menu main main main main right';
}

.title {
  display: block;
  font-weight: 500;
  font-size: 42px;
  letter-spacing: 1px;
  margin-bottom: 24px;
}

.subtitle {
  display: block;
  margin-bottom: 12px;
  font-weight: 400;
  font-size: 20px;
  word-spacing: 5px;
}

p {
  margin-bottom: 36px;
}

.links {
  padding-top: 15px;
}
</style>
