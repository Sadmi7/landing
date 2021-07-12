<template>
  <div class="InfoSection">
    <div class="InfoSection_MainText">
      Но с другой <br />
      стороны...
    </div>
    <div class="InfoSection_Graph">
      <img
        class="InfoSection_BusinessGraphic"
        alt="BusinessGraphic"
        src="@/assets/graph.png"
      />
      <div class="MobileGraph">
        <img alt="verticalVector" src="@/assets/verticalVector.png" />
        <div class="GraphPoint1">
          <div class="GraphPoint1_Circle"></div>
          <div class="GraphPoint1_Text">
            Интересен трейдинг, прошёл обучение
          </div>
        </div>
        <div class="GraphPoint2">
          <div class="GraphPoint2_Circle"></div>
          <div class="GraphPoint2_Text">
            Начал торговать, думая что теперь покорю мир
          </div>
        </div>
        <div class="GraphPoint3">
          <div class="GraphPoint3_Circle"></div>
          <div class="GraphPoint3_Text">Получаю какую-то прибыль</div>
        </div>
        <div class="GraphPoint4">
          <div class="GraphPoint4_Circle"></div>
          <div class="GraphPoint4_Text">Не хватает мнения профессионала</div>
        </div>
        <div class="GraphPoint5">
          <div class="GraphPoint5_Circle"></div>
          <div class="GraphPoint5_Text">Не с кем обсудить свою торговлю</div>
        </div>
        <div class="GraphPoint6">
          <div class="GraphPoint6_Circle"></div>
          <div class="GraphPoint6_Text">Не знаю за что хвататься</div>
        </div>
        <div class="GraphPoint7">
          <div class="GraphPoint7_Circle"></div>
          <div class="GraphPoint7_Text">
            Трачу много времени на отбор инструментов
          </div>
        </div>
      </div>
      <img
        class="InfoSection_Businessman"
        alt="Businessman"
        src="@/assets/businessman.png"
      />
      <div class="InfoSection_Text">
        <img class="InfoSection_Image" alt="Info" src="@/assets/info.png" />
        Спустя пол года наступает выгорание и мысль “а может бросить это всё”
        берёт верх, хотя по факту начиналось всё хорошо
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "InfoSection",
};
</script>

<style lang="scss">
/* eslint-disable */
@import "./infoSection.scss";
</style>
