<template>
    <div id="content">
        <nav>
            <p  v-on:mouseover="mouseOver('home')" v-on:mouseleave="mouseLeave('home')" v-bind:class="{'menu-button-active': active_home, 'menu-button': !active_home}" > home</p>
            <p v-on:mouseover="mouseOver('about_me')" v-on:mouseleave="mouseLeave('about_me')" v-bind:class="{'menu-button-active': active_about_me, 'menu-button': !active_about_me}">about me</p>
            <p v-on:mouseover="mouseOver('services')" v-on:mouseleave="mouseLeave('services')" v-bind:class="{'menu-button-active': active_services, 'menu-button': !active_services}">services</p>
            <p v-on:mouseover="mouseOver('contact')" v-on:mouseleave="mouseLeave('contact')" v-bind:class="{'menu-button-active': active_contact, 'menu-button': !active_contact}">contact</p>
        </nav>
    <main>
        <span class="content-seperator"></span>
        <div id="main-content">Blah</div>
        <span class="content-seperator"></span>
    </main>
    </div>

</template>

<script>
export default {
  name: 'Content',
  props: {
  },
  data(){
    return {
        active_home:false,
        active_about_me:false,
        active_services:false,
        active_contact:false,
      
      }
  },
  methods: {
    mouseLeave: function(menu_item) {
      switch(menu_item){
        case 'home':
          this.active_home=false;
          break;
        case 'about_me':
          this.active_about_me=false;
          break;
        case 'services':
          this.active_services=false;
          break;
        case 'contact':
          this.active_contact=false;
          break;   
      }
      
    },
    mouseOver: function(menu_item){
        switch(menu_item){
          case 'home':
            this.active_home=true;
            break;
          case 'about_me':
            this.active_about_me=true;
            break;
          case 'services':
            this.active_services=true;
            break;
          case 'contact':
            this.active_contact=true;
            break;   
      }
    }
    
  }
}
</script>

<style scoped>
#content {
    border-radius: 25px;
    margin: .5em auto;
    background:rgba(104, 104, 104, .26);
    padding: 20px 0px;
    width: 96%;
    height: 75%;

}

nav{
    text-align: center;
}
.menu-button {
    height: auto;
    width: auto;
    background-color: #bbb;
    border-radius: 50%;
    border: 1px solid white;
    display: inline-block;
    font-family: 'Montserrat';
    font-size: 25px;
    margin: .5em;
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
    font-family: 'Montserrat';
    font-size: 25px;
    margin: .5em;
    padding-top: 10px;
    padding-right: 15px;
    padding-bottom: 15px;
    padding-left: 10px;
}

.content-seperator{
    display: table;
    background: white;
    width: 100%;
    height: .25em;
}
.content-seperator span{
    display: table-cell;
}

</style>
