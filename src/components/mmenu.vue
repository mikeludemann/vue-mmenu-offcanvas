<template lang="html">
  <section id="mmenu">
    
  </section>
</template>

<script>
import Vue from "vue";
import $ from "jquery";

import 'mmenu-js/dist/mmenu'
import 'mmenu-js/dist/mmenu.css';

// Core
import Mmenu from "mmenu-js/dist/core/oncanvas/mmenu.oncanvas";

// Core Add-Ons
import offcanvas from "mmenu-js/dist/core/offcanvas/mmenu.offcanvas";
import screenReader from "mmenu-js/dist/core/screenreader/mmenu.screenreader";
import scrollBugFix from "mmenu-js/dist/core/scrollbugfix/mmenu.scrollbugfix";

// Extensions
/*
import borderstyle from "mmenu-js/dist/extensions/borderstyle/";
import effects from "mmenu-js/dist/extensions/effects";
import fullscreen from "mmenu-js/dist/extensions/fullscreen";
import listview from "mmenu-js/dist/extensions/listview";
import multiline from "mmenu-js/dist/extensions/multiline";
import pagedim from "mmenu-js/dist/extensions/pagedim";
import popup from "mmenu-js/dist/extensions/popup";
import positioning from "mmenu-js/dist/extensions/positioning";
import shadows from "mmenu-js/dist/extensions/shadows";
import themes from "mmenu-js/dist/extensions/themes";
import tileview from "mmenu-js/dist/extensions/tileview";
*/

// Wrappers
import angular from "mmenu-js/dist/wrappers/angular/mmenu.angular";
import bootstrap from "mmenu-js/dist/wrappers/bootstrap/mmenu.bootstrap";
import magento from "mmenu-js/dist/wrappers/magento/mmenu.magento";
import olark from "mmenu-js/dist/wrappers/olark/mmenu.olark";
import turbolinks from "mmenu-js/dist/wrappers/turbolinks/mmenu.turbolinks";
import wordpress from "mmenu-js/dist/wrappers/wordpress/mmenu.wordpress";

// Add-Ons
import autoheight from "mmenu-js/dist/addons/autoheight/mmenu.autoheight";
import backbutton from "mmenu-js/dist/addons/backbutton/mmenu.backbutton";
import columns from "mmenu-js/dist/addons/columns/mmenu.columns";
import counters from "mmenu-js/dist/addons/counters/mmenu.counters";
import dividers from "mmenu-js/dist/addons/dividers/mmenu.dividers";
import drag from "mmenu-js/dist/addons/drag/mmenu.drag";
import dropdown from "mmenu-js/dist/addons/dropdown/mmenu.dropdown";
import fixedelements from "mmenu-js/dist/addons/fixedelements/mmenu.fixedelements";
import iconbar from "mmenu-js/dist/addons/iconbar/mmenu.iconbar";
import iconpanels from "mmenu-js/dist/addons/iconpanels/mmenu.iconpanels";
import keyboardnavigation from "mmenu-js/dist/addons/keyboardnavigation/mmenu.keyboardnavigation";
import lazysubmenus from "mmenu-js/dist/addons/lazysubmenus/mmenu.lazysubmenus";
import navbars from "mmenu-js/dist/addons/navbars/mmenu.navbars";
import pagescroll from "mmenu-js/dist/addons/pagescroll/mmenu.pagescroll";
import searchfield from "mmenu-js/dist/addons/searchfield/mmenu.searchfield";
import sectionindexer from "mmenu-js/dist/addons/sectionindexer/mmenu.sectionindexer";
import setselected from "mmenu-js/dist/addons/setselected/mmenu.setselected";
import sidebar from "mmenu-js/dist/addons/sidebar/mmenu.sidebar";
import toggles from "mmenu-js/dist/addons/toggles/mmenu.toggles";

const Navi = Vue.component('mmenu', {
  props: {
    id: {
      type: String
    },
    options: {
      type: Object
    }
  },
  mounted(){
    Mmenu.addons = {
      // Core
      offcanvas,
      screenReader,
      scrollBugFix,
      // Extensions
      /*
      borderstyle,
      effects,
      fullscreen,
      listview,
      multiline,
      pagedim,
      popup,
      positioning,
      shadows,
      themes,
      tileview,
      */
      // Wrappers
      angular,
      bootstrap,
      magento,
      olark,
      turbolinks,
      wordpress,
      // Add-Ons
      autoheight,
      backbutton,
      columns,
      counters,
      dividers,
      drag,
      dropdown,
      fixedelements,
      iconbar,
      iconpanels,
      keyboardnavigation,
      lazysubmenus,
      navbars,
      pagescroll,
      searchfield,
      sectionindexer,
      setselected,
      sidebar,
      toggles
    };

    window.Mmenu = Mmenu;

    document.addEventListener(
      "DOMContentLoaded", () => {
        new Mmenu("#" + this.id, this.options);
      }
    );
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  },
  template: `
    <nav :id="id">
      <slot></slot>
    </nav>
  `
});

const NaviList = Vue.component('NaviList', {
  props: {
    class: {
      type: String
    }
  },
  mounted(){
    
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  },
  template: `
    <ul :class="class">
      <slot></slot>
    </ul>
  `
});

const NaviListItem = Vue.component('NaviListItem', {
  props: {
    class: {
      type: String
    }
  },
  mounted(){
    
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  },
  template: `
    <li :class="class">
      <slot></slot>
    </li>
  `
});

const NaviListText = Vue.component('NaviListText', {
  props: {
    class: {
      type: String
    }
  },
  mounted(){
    
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  },
  template: `
    <span :class="class">
      <slot></slot>
    </span>
  `
});

const NaviListLink = Vue.component('NaviListLink', {
  props: {
    url: {
      type: String
    }
  },
  mounted(){
    
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  },
  template: `
    <a :href="url">
      <slot></slot>
    </a>
  `
});

export default  {
  name: 'mmenu',
  components: {
    Navi,
    NaviList,
    NaviListItem,
    NaviListText,
    NaviListLink
  }
}
</script>

<style scoped lang="scss">
  .mmenu {

  }
</style>
