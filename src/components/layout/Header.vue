<template>
  <div class="header-wrapper">
    <nav class="header-nav__primary" aria-label="primary">
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
    <nav class="header-nav__secondary" aria-label="secondary">
      <ul class="header-nav__link-list--secondary">
        <li class="header-nav__link-list__item"><a href="/en/about/">About</a></li>
        <li class="header-nav__link-list__item"><a href="/en/jobs/">Jobs</a></li>
        <li class="header-nav__link-list__item"><a href="/en/ausbildung/">Apprenticeships</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
import LogoIcon from '../icons/LogoIcon.vue'
export default {
  components: {
    LogoIcon,
  },
}
</script>

<style scoped lang="scss">
.header-wrapper {
  width: 100%;
  padding-top: 2rem;

  .header-nav__primary {
    width: 100%;
    box-sizing: border-box;
    margin-bottom: 2rem;
    font-family: 'Futura PT medium', sans-serif;

    .header-nav__logo {
      display: block;
      position: absolute;
      text-decoration: none;
      z-index: 30;
      width: 60px;
      height: 28px;
      margin: 0 32px 20px 40px;

      svg {
        width: 100%;
        height: 100%;
        fill: #000;
      }
    }
    .header-nav__primary-wrapper {
      width: 100%;
      .header-nav__link-list {
        display: flex;
        flex-direction: row;
        align-items: center;
        padding-left: 8.75em;
        padding-right: 2.5em;
        list-style: none;
      }

      .header-nav__link-list .header-nav__link-list__item:first-child {
        margin-left: 0;
        padding-left: 0;
      }

      .header-nav__link-list__item {
        margin: 0 0.3125em;
        padding: 0 0.625em;

        a {
          color: #000;
          font-size: 2rem;
          line-height: 1.5;
          text-decoration: none;
        }
      }
      .header-nav__more-button {
        position: relative;
        color: var(--color-text-link-secondary);
        background-color: var(--vt-c-white);
        border: none;
        display: flex;
        align-items: center;
        cursor: pointer;

        span {
          font-size: 2rem;
        }

        .more__plus {
          position: inherit;
          width: 18px;
          height: 18px;
          margin-left: 5px;

          &:after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 1px;
            height: 16px;
            transform: translate(-50%, -50%);
            background-color: var(--color-text-link-secondary);
          }

          &:before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(90deg);
            width: 1px;
            height: 16px;
            background-color: var(--color-text-link-secondary);
          }
        }
      }
      .try {
        margin-left: auto;

        a {
          color: var(--color-text-link-primary);
        }
      }
      .login {
        padding-right: 0;
        margin-right: 0;

        a {
          font-size: 1.6rem;
        }
      }
    }

    .header-nav__button {
      display: none;
    }

    .header-nav__more {
      display: none;
    }
  }

  .header-nav__separator {
    width: 100%;
    height: 0;
    border-top: 2px solid var(--color-nav-separator);
  }

  .header-nav__secondary {
    padding: 20px 40px;
    box-sizing: border-box;
    .header-nav__link-list--secondary {
      list-style: none;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: flex-start;
      padding: 0;

      .header-nav__link-list__item {
        margin: 0 0.625em;
        padding: 0 0.625em;

        a {
          text-decoration: none;
          color: var(--vt-c-black);
          font-size: 1.6rem;
        }
      }
      .header-nav__link-list__item:first-child a {
        color: var(--color-text-link-secondary);
      }

      .header-nav__link-list__item:first-child {
        margin-left: 0;
        padding-left: 0;
      }

      .header-nav__link-list__item:last-child {
        margin-right: 0;
        padding-right: 0;
      }
    }
  }
}

@media screen and (max-width: 128rem) {
  .header-wrapper {
    .nav-list {
      .header-nav__logo {
        margin: 0 32px 20px 20px;
      }
    }
  }
}
</style>
