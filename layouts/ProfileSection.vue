<template>
  <div class="profile-section">
    <avatar :image="imgProfile" description="Foto de perfil: Dev Rafael Oliveira." />
    <h3>Rafael Pereira Oliveira</h3>
    <h4>Desenvolvedor Fullstack</h4>
    <social-media />
  </div>
</template>
<script>
// assets
import imgProfile from "~/assets/images/profile.png";
// components
import Avatar from "~/components/Avatar";
import SocialMedia from '~/components/social-media/SocialMedia'

export default {
  components: { Avatar, SocialMedia },
  data () {
    return {
      imgProfile
    }
  }
}
</script>

<style lang="scss" scoped>
.profile-section {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  padding: 10px 6px;

  .avatar {
    width: 160px;
    height: 160px;
    margin-bottom: 10px;
  }

  .social-media {
    margin-top: 16px;
  }
}
</style>
