<template>
    <header>
        <div class="row">
            <div id="title" >Newman Thurairatnam</div>
            <div id="side_logo" ><img src="../assets/side_logo.svg" align="right" ></div>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header{
    background-color: black;
    font-family: 'Mrs Sheppards';
}

.row::after{
    content: "";
    clear: both;
    display: table;

}
#title{
    float: left;
    padding: 0;
    width: 60%;
    text-align: right;

}
#side_logo{
    float: right;
    padding: 0;
    width: 40%;
}

</style>
