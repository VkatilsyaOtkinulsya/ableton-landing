<script setup>
import LogoIcon from '@/components/icons/LogoIcon.vue';
import { ref, computed, watch } from 'vue';
import { useScroll, useElementSize, useDebounceFn } from '@vueuse/core';

const primaryNav = ref(null);
const { height: primaryNavHeight } = useElementSize(primaryNav);
const { y } = useScroll(window);

const isSticky = ref(false);
const updateSticky = useDebounceFn(() => {
  isSticky.value = y.value > primaryNavHeight.value;
  document.body.classList.toggle('sticky-secondary-nav', isSticky.value);
}, 10);

watch(y, updateSticky);
</script>

<template>
  <div class="header-wrapper">
    <nav ref="primaryNav" class="header-nav__primary" aria-label="primary">
      <a href="#" class="header-nav__logo">
        <LogoIcon></LogoIcon>
      </a>
      <button class="header-nav__button"></button>
      <div class="header-nav__primary-wrapper">
        <ul class="header-nav__link-list">
          <li class="header-nav__link-list__item"><a href="/en/live/">Live</a></li>
          <li class="header-nav__link-list__item"><a href="/en/push/">Push</a></li>
          <li class="header-nav__link-list__item"><a href="/en/move/">Move</a></li>
          <li class="header-nav__link-list__item"><a href="/en/note/">Note</a></li>
          <li class="header-nav__link-list__item"><a href="/en/link/">Link</a></li>
          <li class="header-nav__link-list__item"><a href="/en/shop/">Shop</a></li>
          <li class="header-nav__link-list__item"><a href="/en/packs/">Packs</a></li>
          <li class="header-nav__link-list__item"><a href="/en/help/">Help</a></li>
          <li class="header-nav__link-list__item">
            <button class="header-nav__more-button">
              <span>More</span>
              <div class="more__plus"></div>
            </button>
          </li>
          <li class="header-nav__link-list__item try">
            <a href="/en/trial/">Try Live 12 for free</a>
          </li>
          <li class="header-nav__link-list__item login">
            <a href="/en/login-huegin">Log in or register</a>
          </li>
        </ul>
        <div class="header-nav__more" aria-hidden="true">Smth</div>
      </div>
    </nav>
    <div class="header-nav__separator"></div>
    <div class="header-nav__secondary--wrapper">
      <nav
        ref="secondaryNav"
        class="header-nav__secondary"
        :class="{ sticky: isSticky }"
        aria-label="secondary"
      >
        <ul class="header-nav__link-list--secondary">
          <li class="header-nav__link-list__item"><a href="/en/about/">About</a></li>
          <li class="header-nav__link-list__item"><a href="/en/jobs/">Jobs</a></li>
          <li class="header-nav__link-list__item"><a href="/en/ausbildung/">Apprenticeships</a></li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import './Header.module.scss';
</style>
