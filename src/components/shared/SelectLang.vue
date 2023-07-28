<script setup>
import Arrow from '../icons/smallArrow.vue';
</script>

<template>
  <div
    class="language-selector"
    @click="handleOpenOptions">
    <div class="language-selector-lang">
      <img class="language-selector-lang__icon" :src="`src/assets/images/langs/${locale}.png`" alt="flag">
      <span class="language-selector-lang__text">{{ $t(`lang.${locale}`) }}</span>
    </div>
    <Arrow class="language-selector-arrow"/>
  </div>
  <div
    class="language-selector-wrapper"
    v-if="openOptions">
    <div
      class="language-selector-option"
      v-for="(lang, index) in langs"
      :key="index"
      @click="changeLang(lang)">
      <img class="language-selector-option__icon" :src="`src/assets/images/langs/${lang}.png`" alt="flag">
      <span class="language-selector-option__text">{{ $t(`lang.${lang}`) }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SelectLang',
  data() {
    return {
      langs: [
        'en',
        'pt',
      ],
      locale: this.$i18n.locale,
      openOptions: false,
    };
  },
  methods: {
    handleOpenOptions() {
      const arrow = document.querySelector('.language-selector-arrow');
      arrow.classList.toggle('up');
      this.openOptions = !this.openOptions;
    },
    changeLang(lang) {
      this.$i18n.locale = lang;
      this.locale = lang;
      this.handleOpenOptions();
    },
  },
}
</script>

<style scoped>
.language-selector {
  display: flex;
  align-items: center;
  justify-content: space-between;
  cursor: pointer;
  padding: 10px 10px;
  border-radius: 10px;
  gap: 20px;
  min-width: 160px;
}
.language-selector:hover {
  color: var(--color-nav-text);
  line-height: 24px;
  text-decoration-line: underline;
}
.language-selector-lang {
  display: flex;
  align-items: center;
  gap: 10px;
}
.language-selector-lang__icon {
  width: 20px;
  height: 20px;
}
.language-selector-lang__text {
  color: var(--color-nav-text);
  text-shadow: 0px 8px 16px 0px var(--color-nav-text-shadow);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
}
.language-selector-arrow {
  width: 10px;
  height: 10px;
  transition: .5s;
}
.up {
  transform: rotate(180deg);
}
.language-selector-wrapper {
  background-color: var(--color-background-soft);
  position: absolute;
  right: 0;
  padding: 5px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  transform: translateY(80%);
  width: 160px;
}
.language-selector-option {
  display: flex;
  align-items: center;
  gap: 10px;
  cursor: pointer;
  padding: 5px 15px;
  border-radius: 10px;
}
.language-selector-option:hover {
  background-color: var(--color-background-hover);
}
.language-selector-option__icon {
  width: 20px;
  height: 20px;
}
.language-selector-option__text {
  color: var(--color-text);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
}

@media screen and (max-width: 820px) {
  .language-selector {
    display: none;
  }
}
</style>