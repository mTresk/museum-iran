<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <div class="screen__content">
            <div class="screen__info">
              <h2 class="screen__subtitle">Специфика полёта</h2>
              <p class="screen__text">
                Птицы могут летать медленно, но за короткое время способны набирать нужную высоту. А основной особенностью иранских голубей является умение
                надолго фиксироваться в одной точке.
              </p>
              <p class="screen__text">
                При обеспечении отличных условий содержания и сбалансированном питании голуби станут не только сильными, но и выносливыми, а
                продолжительность полёта будет только увеличиваться.
              </p>
              <p class="screen__text">
                В среднем эти голуби проводят в небе от 3 до 10 часов подряд. Птицы, продолжительность полёта которых составляет менее 180 минут,
                выбраковываются.
              </p>
              <p class="screen__text">
                Если молодые иранские голуби готовятся к состязаниям, к ним предъявляются особые требования. Такие особи должны уметь возвращаться домой или
                в ту точку, из которой были выпущены. Птицы, которые не владеют этими навыками, подлежат отбраковке.
              </p>
              <ul class="screen__text">
                <li>голова зауженная, обтекаемой округлой или овальной формы;</li>
                <li>клюв длинный. Его размер может достигать 20-25 мм;</li>
                <li>тело рельефное, удлинённое, с развитой мускулатурой и плотным костяком;</li>
                <li>ноги гладкие, высокие. У представителей некоторых пород лапы укороченные, покрытые оперением;</li>
                <li>крылья плотно прижаты к туловищу. Их длина достигает 21-30 см, а размах составляет около 60-70 см;</li>
                <li>хвост состоит из 12 рулевых перьев и достигает 13 см в длину;</li>
                <li>перьевой покров плотно прилегает к телу, что придаёт дополнительную обтекаемость в полете.</li>
              </ul>
            </div>
          </div>
          <Navigation :page-next="pageNext" :page-prev="pagePrev"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import {mapActions} from 'vuex'
import Navigation from "@/components/Navigation";
import Background from "@/components/Background";
import Logo from "@/components/Logo";
import Doves from "@/components/Doves";

export default {
  name: "Page-3",
  data() {
    return {
      pagePrev: 'page-2',
      pageNext: 'page-4',
    }
  },
  components: {
    Doves,
    Logo,
    Background,
    Navigation
  },
  mounted() {
    this.animate()
  },
  methods: {
    ...mapActions([
      'animate'
    ]),
  }
}
</script>