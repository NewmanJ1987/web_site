<template>
    <div id="content">
        <nav>
            <p class="menu-button">home</p>
            <p class="menu-button">about me</p>
            <p class="menu-button">services</p>
            <p class="menu-button">contact</p>
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
