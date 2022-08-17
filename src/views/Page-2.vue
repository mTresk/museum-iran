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
              <h2 style="margin-bottom: 15px" class="screen__subtitle">ВНЕШНИЙ ВИД</h2>
              <p class="screen__text">
                «Иранцы» – голуби, у которых нет строго регламентированных стандартов. Они обладают средними размерами и вырастают до 34-45 см.
              </p>
              <p class="screen__text">И хотя птицы делятся на несколько разновидностей, у них имеются общие черты:</p>
              <ul class="screen__text">
                <li>голова зауженная, обтекаемой округлой или овальной формы;</li>
                <li>клюв длинный. Его размер может достигать 20-25 мм;</li>
                <li>тело рельефное, удлинённое, с развитой мускулатурой и плотным костяком;</li>
                <li>ноги гладкие, высокие. У представителей некоторых пород лапы укороченные, покрытые оперением;</li>
                <li>крылья плотно прижаты к туловищу. Их длина достигает 21-30 см, а размах составляет около 60-70 см;</li>
                <li>хвост состоит из 12 рулевых перьев и достигает 13 см в длину;</li>
                <li>перьевой покров плотно прилегает к телу, что придаёт дополнительную обтекаемость в полете.</li>
              </ul>
              <p class="screen__text">Нередко попадаются белые голуби, птицы с красным, чёрным, жёлтым оперением. Иногда они бывают сизыми.</p>
              <p class="screen__text">Самыми ценными считаются голуби, обладающие комбинированными расцветками:</p>
              <ul class="screen__text">
                <li>с цветной головой и хвостом;</li>
                <li>однотонные;</li>
                <li>с белой головой и пёстрым телом;</li>
                <li>с цветными боками (тело белое, а крылья - цветные);</li>
                <li>с цветной головой (чёрного, жёлтого, красного и других оттенков);</li>
                <li>с цветным или белым хвостом;</li>
                <li>с цветными кольцами, расположенными вокруг шеи.</li>
              </ul>
              <p class="screen__text">Обычно эти породы не меняют окрас оперения с возрастом или в период линьки и после нее.</p>
              <p class="screen__text">
                На западе Ирана при разведении голубей отбор племенных особей проводится по окрасу. Местные селекционеры предпочитают птиц, на теле которых
                присутствует идеальный рисунок без дефектов.
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
import Background from "@/components/Background";
import Logo from "@/components/Logo";
import Doves from "@/components/Doves";

export default {
  name: "Page-2",
  data() {
    return {
      pagePrev: 'page-1',
      pageNext: 'page-3',
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