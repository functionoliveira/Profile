<template>
  <div class="container">
    <background-video :srcVideo="bgVideo" />
    <!-- Profile -->
    <div class="profile">
      <glass-card>
        <profile-section />
      </glass-card>
    </div>
    
    <div class="main">
      <scroll>
        <!-- Introduction -->
        <glass-card class="mb-1" id="home">
          <home-section />
        </glass-card>

        <!-- Work Experiences -->
        <glass-card class="mb-1" id="experience">
          <h2>Experiência</h2>
          <timeline label="2015 - 2015" title="Teste de software" subtitle="Procergs" description="Lorem ipsum" />
          <separator />
          <h2>Formação</h2>
          <timeline label="2015 - 2015" title="Teste de software" subtitle="Procergs" description="Lorem ipsum" />
        </glass-card>

        <!-- References -->
        <glass-card class="mb-1" id="reference">
          <references-section />
          <separator />
          <interests-section />
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
import ProfileSection from '~/layouts/ProfileSection'
import HomeSection from '~/layouts/HomeSection'
import ReferencesSection from '~/layouts/ReferencesSection'
import ClientsSection from '~/layouts/ClientsSection'
import InterestsSection from '~/layouts/InterestsSection'

export default {
  components: {
    HomeSection,
    ProfileSection,
    ContactSection,
    ReferencesSection,
    ClientsSection,
    InterestsSection,
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

#contact {
  margin-bottom: 75px;
}
</style>
