<template>
  <div :class="$style.vueFooter">
    <vue-grid>
      <vue-grid-row>
        <vue-grid-item>
          <small>&copy; Copyright {{year}} Flashtatu </small>
        </vue-grid-item>

        <vue-grid-item>
          <a href="https://github.com/matheus510" target="_blank" rel="noopener" aria-label="github profile">
            <vue-icon-github-alt />
          </a>
          <a href="https://twitter.com/math510" target="_blank" rel="noopener" aria-label="twitter profile">
            <vue-icon-twitter-square />
          </a>
        </vue-grid-item>

        <vue-grid-item>
          <small><a href="https://github.com/matheus510/flashtatu_pwa/blob/master/LICENSE" target="_blank"
                    rel="noopener">MIT
                                   License</a>
          </small>
        </vue-grid-item>
      </vue-grid-row>
    </vue-grid>
  </div>
</template>

<script lang="ts">
  import VueGrid              from '../VueGrid/VueGrid';
  import VueGridItem          from '../VueGridItem/VueGridItem';
  import VueGridRow           from '../VueGridRow/VueGridRow';
  import VueIconGithubAlt     from '../icons/VueIconGithubAlt/VueIconGithubAlt';
  import VueIconTwitterSquare from '../icons/VueIconTwitterSquare/VueIconTwitterSquare';

  export default {
    name:       'VueFooter',
    components: {
      VueIconTwitterSquare,
      VueIconGithubAlt,
      VueGrid,
      VueGridItem,
      VueGridRow,
    },
    computed:   {
      year() {
        return new Date().getFullYear();
      },
    },
  };
</script>

<style lang="scss" module>
  @import "../../styles";

  .vueFooter {
    padding:    $footer-padding;
    background: $footer-bg;
    color:      $footer-color;
    text-align: center;

    i {
      height: $font-size-h1;
      width:  $font-size-h1;
      fill:   $brand-accent;
      margin: 0 $space-unit * 2;
    }

    small {
      display: inline-block;
      margin:  $space-unit * 2 0;
    }
  }
</style>
