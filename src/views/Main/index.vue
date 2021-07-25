<template>
  <main id="Main">
    <Banner />
    <Context />
    <Valores />
    <Eixos />
    <Chancela />
    <Agenda />
    <Mapa />
    <Noticias />
    <Newsletter />
  </main>
</template>

<script>
  import Banner from './../../sections/Banner';
  import Context from './../../sections/Context';
  import Valores from './../../sections/Valores';
  import Eixos from './../../sections/Eixos';
  import Chancela from './../../sections/Chancela';
  import Agenda from './../../sections/Agenda';
  import Mapa from './../../sections/Mapa';
  import Noticias from './../../sections/Noticias';
  import Newsletter from './../../sections/Newsletter';

  export default {
    components: {
      Banner,
      Context,
      Valores,
      Eixos,
      Chancela,
      Agenda,
      Mapa,
      Noticias,
      Newsletter
    }
  }
</script>
