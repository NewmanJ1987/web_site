<template>
    <div id="content">
        <nav>
            <p v-on:click="updateContent('home')" v-on:mouseover="mouseOver('home')" v-on:mouseleave="mouseLeave('home')" v-bind:class="menuSelectClass('home')">home</p>
            <p v-on:click="updateContent('about_me')" v-on:mouseover="mouseOver('about_me')" v-on:mouseleave="mouseLeave('about_me')" v-bind:class="menuSelectClass('about_me')">about me</p>
            <p v-on:click="updateContent('services')" v-on:mouseover="mouseOver('services')" v-on:mouseleave="mouseLeave('services')" v-bind:class="menuSelectClass('services')">services</p>
            <p v-on:click="updateContent('contact')" v-on:mouseover="mouseOver('contact')" v-on:mouseleave="mouseLeave('contact')" v-bind:class="menuSelectClass('contact')">contact</p>
        </nav>
    <main>
        <span class="content-seperator"></span>
        <div id="main-content">{{content}}</div>
        <span class="content-seperator"></span>
    </main>
    </div>

</template>

<script>
export default {
  name: "Content",
  props: {},
  data() {
    return {
      active_home: false,
      active_about_me: false,
      active_services: false,
      active_contact: false,
      content: "Blteah"
    };
  },
  methods: {
    mouseLeave: function(menu_item) {
      switch (menu_item) {
        case "home":
          this.active_home = false;
          break;
        case "about_me":
          this.active_about_me = false;
          break;
        case "services":
          this.active_services = false;
          break;
        case "contact":
          this.active_contact = false;
          break;
      }
    },
    mouseOver: function(menu_item) {
      switch (menu_item) {
        case "home":
          this.active_home = true;
          break;
        case "about_me":
          this.active_about_me = true;
          break;
        case "services":
          this.active_services = true;
          break;
        case "contact":
          this.active_contact = true;
          break;
      }
    },
    updateContent: function(menu_item) {
      switch (menu_item) {
        case "home":
          this.content = "Home";
          break;
        case "about_me":
          this.content = "About Me";
          break;
        case "services":
          this.content = "Services";
          break;
        case "contact":
          this.content = "Contact";
          break;
      }
    },
      menuSelectClass: function(menu_item) {
      switch (menu_item) {
        case "home":
          return {'menu-button-active': this.active_home, 'menu-button': !this.active_home}
        case "about_me":
          return {'menu-button-active': this.active_about_me, 'menu-button': !this.active_about_me}
        case "services":
          return {'menu-button-active': this.active_services, 'menu-button': !this.active_services}
        case "contact":
          return {'menu-button-active': this.active_contact, 'menu-button': !this.active_contact}
      }
    }
  },
  computed: {

  }
};
</script>

<style scoped>
#content {
  border-radius: 25px;
  margin: 0.5em auto;
  background: rgba(104, 104, 104, 0.26);
  padding: 20px 0px;
  width: 96%;
  height: 75%;
}

#main-content {
  text-align: center;
  color: black;
  font-family: " Calibri", sans-serif;
  font-size: 20px;
}
nav {
  text-align: center;
}
.menu-button {
  height: auto;
  width: auto;
  background-color: #bbb;
  border-radius: 50%;
  border: 1px solid white;
  display: inline-block;
  font-family: "Montserrat";
  font-size: 25px;
  margin: 0.5em;
  padding-top: 10px;
  padding-right: 15px;
  padding-bottom: 15px;
  padding-left: 10px;
}

.menu-button-active {
  height: auto;
  width: auto;
  background-color: rgb(66, 66, 66);
  border-radius: 50%;
  border: 1px solid white;
  display: inline-block;
  font-family: "Montserrat";
  font-size: 25px;
  margin: 0.5em;
  padding-top: 10px;
  padding-right: 15px;
  padding-bottom: 15px;
  padding-left: 10px;
}

.content-seperator {
  display: table;
  background: white;
  width: 100%;
  height: 0.25em;
}
.content-seperator span {
  display: table-cell;
}
</style>
