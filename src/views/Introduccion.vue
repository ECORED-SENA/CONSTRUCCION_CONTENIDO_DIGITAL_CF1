<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
  
    .titulo-principal
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción

    p.mb-3
      b  ¿Sabías que el contenido digital se refiere a toda la información que se muestra en un medio digital?
      br
      br
      | Cuando hablamos de información, nos referimos a los gráficos, presentaciones, audios y videos. Para producir cada uno de estos insumos, es importante conocer sus características y el flujo de trabajo que implica el desarrollo de cada uno de estos contenidos.

    h4.mb-5 En este componente formativo aprenderemos:
    
    .row.align-items-center(data-aos="fade-up")
      .col.d-none.d-md-flex.flex-column.justify-content-center.align-items-end
        .position-relative.mb-4(@mouseover="mostrarIndicador = false")
          .indicador--hover(v-if="mostrarIndicador")
          .intro-btn.intro-btn--reverse
            .intro-btn__icon
              img(src='@/assets/curso/intro-icon-1.svg')
            .intro-btn__text
              span.text-bold ¿Qué es el mundo del contenido digital?

        .intro-btn.intro-btn--reverse.mb-4(@mouseover="mostrarIndicador = false")
          .intro-btn__icon
            img(src='@/assets/curso/intro-icon-2.svg')
          .intro-btn__text
            span.text-bold Los tipos de contenido digital.

        .intro-btn.intro-btn--reverse(@mouseover="mostrarIndicador = false")
          .intro-btn__icon
            img(src='@/assets/curso/intro-icon-3.svg')
          .intro-btn__text
            span.text-bold Los conceptos y características básicas necesarias.

      .col-sm.mb-4.mb-sm-0
        figure
          img(src='@/assets/curso/intro-img.svg', alt='representación ecosistema digital')
    
      .col-sm.col-md.d-flex.flex-column.justify-content-center
        .position-relative.mb-4.d-md-none(@mouseover="mostrarIndicador = false")
          .indicador--hover(v-if="mostrarIndicador")
          .intro-btn
            .intro-btn__icon
              img(src='@/assets/curso/intro-icon-1.svg')
            .intro-btn__text
              span.text-bold ¿Qué es el mundo del contenido digital?

        .intro-btn.mb-4.d-md-none(@mouseover="mostrarIndicador = false")
          .intro-btn__icon
            img(src='@/assets/curso/intro-icon-2.svg')
          .intro-btn__text
            span.text-bold Los tipos de contenido digital.

        .intro-btn.mb-4.d-md-none(@mouseover="mostrarIndicador = false")
          .intro-btn__icon
            img(src='@/assets/curso/intro-icon-3.svg')
          .intro-btn__text
            span.text-bold Los conceptos y características básicas necesarias.


        
        .intro-btn.mb-4(@mouseover="mostrarIndicador = false")
          .intro-btn__icon
            img(src='@/assets/curso/intro-icon-4.svg')
          .intro-btn__text
            span.text-bold ¿Qué son los objetivos de comunicación?

        .intro-btn(@mouseover="mostrarIndicador = false")
          .intro-btn__icon
            img(src='@/assets/curso/intro-icon-5.svg')
          .intro-btn__text
            span.text-bold ¿Cómo se planifican los contenidos digitales?

</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    mostrarIndicador: true,
  }),
}
</script>

<style lang="sass" scoped>
.intro-btn
  display: flex
  align-items: center
  box-shadow: 0px 0px 10px 0px rgba(0,0,0,0.2)
  padding: 5px
  border-radius: 35px
  width: 70px
  overflow: hidden
  transition: width 0.3s ease-in-out, border-radius 0.3s ease-in-out
  cursor: pointer
  position: relative
  &__icon
    width: 60px
    padding: 10px
    background-color: $color-secundario
    border-radius: 50%
    flex-shrink: 0
  &__text
    min-width: 230px
    padding: 0 10px
    text-align: center
    span
      line-height: 1.2em
      display: block

  &:hover
    width: 300px
    border-top-right-radius: 10px
    border-bottom-right-radius: 10px

  &--reverse
    flex-direction: row-reverse
    &:hover
      border-radius: 35px
      border-top-left-radius: 10px
      border-bottom-left-radius: 10px

.indicador--hover
</style>
