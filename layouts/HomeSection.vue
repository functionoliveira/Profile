<template>
  <div class="home-section">
    <h2 class="title">Hello, Night City!</h2>
    <p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English. Many desktop publishing packages and web page editors now use Lorem Ipsum as their default model text, and a search for 'lorem ipsum' will uncover many web sites still in their infancy. Various versions have evolved over the years, sometimes by accident, sometimes on purpose (injected humour and the like).</p>
    <separator />
    <div class="home-section__wrap">
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
    <div class="home-section__wrap">
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
  </div>
</template>

<script>
// assets
import JsIcon from "~/icons/JsIcon";
import NodeIcon from "~/icons/NodeIcon";
import HtmlIcon from "~/icons/HtmlIcon";
import SassIcon from "~/icons/SassIcon";
import DbIcon from "~/icons/DbIcon";
import DjIcon from "~/icons/DjIcon";

// components
import Separator from "~/components/Separator";
import ScoreBalls from "~/components/ScoreBalls";
import BarScore from "~/components/BarScore";
import Checklist from "~/components/Checklist";

export default {
  components: {
    Separator,
    ScoreBalls,
    Checklist,
    BarScore,
    JsIcon,
    NodeIcon,
    HtmlIcon,
    SassIcon,
    DbIcon,
    DjIcon
  }
}
</script>

<style lang="scss" scoped>
.home-section {

  &__wrap {
    display: flex;

    .col {
      margin-right: 32px;

      .subtitle {
        margin-bottom: 32px;
      }
    }
  }
}
</style>
