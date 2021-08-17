<template>
  <main id="Main">
    <Banner />
    <Context />
    <Valores />
    <Eixos />
    <Chancela />
    <Agenda />
    <Mapa />
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

  export default {
    components: {
      Banner,
      Context,
      Valores,
      Eixos,
      Chancela,
      Agenda,
      Mapa
    }
  }
</script>
