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
              <p class="screen__text">Категорически запрещено кормить птиц:</p>
              <ul class="screen__text">
                <li>молоком и сыром;</li>
                <li>мясными продуктами и рыбой;</li>
                <li>хлебом и хлебобулочными изделиями.</li>
              </ul>
              <h2 class="screen__subtitle" style="margin-top: 60px">Покупка</h2>
              <p class="screen__text">
                На территории России разведением и продажей иранских бойных голубей занимаются крупные голубиные фермы Владивостока, Москвы, Новосибирска,
                Екатеринбурга, Хабаровска, Челябинска, Красноярска, Омска, Оренбурга.
              </p>
              <p class="screen__text">
                Как и внешние характеристики птиц, так и цена на них могут быть различными. Стоимость напрямую зависит не только от вида, но и от лётных
                качеств. Самые лучшие птицы обитают в Иране.
              </p>
              <p class="screen__text">
                В России «иранцев» предлагают по цене от одной до 2,5 тысяч рублей за голубя. Птицы из хороших линий могут стоить значительно дороже, более
                сотни долларов.
              </p>
              <h2 class="screen__subtitle" style="margin-top: 60px">Заключение</h2>
              <p class="screen__text">
                Иранские бойные голуби – одна из древнейших пород голубей в мире. Птицы отличаются привлекательными внешними характеристиками,
                неприхотливостью в содержании. Они имеют несколько разновидностей, каждая из которых - особенная и необычная.
              </p>
              <p class="screen__text">
                Бойные голуби довольно долго живут, в среднем около 15 лет, но некоторые особи доживают до 35 лет. Добиться такого долголетия можно только
                при правильном уходе.
              </p>
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
import Doves from "@/components/Doves";
import Logo from "@/components/Logo";
import Background from "@/components/Background";

export default {
  name: "Page-14",
  data() {
    return {
      pagePrev: 'page-13',
      pageNext: 'home',
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