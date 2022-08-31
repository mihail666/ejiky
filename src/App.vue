<template>
  <MainContainer>
    <template v-slot:header>
      <header-e-j/>
    </template>
    <main>
      <router-view />
    </main>
    <template v-slot:footer>
      <FooterEJ />
    </template>
  </MainContainer>
</template>

<script>
import HeaderEJ from '@/components/HeaderEJ'
import FooterEJ from '@/components/FooterEJ'
import MainContainer from '@/components/MainContainer'
export default {
  components: {
    MainContainer,
    HeaderEJ,
    FooterEJ
  }
}
</script>

<style lang="scss">

</style>
