<template>
    <footer>
        &copy; 2018 Newman Thurairatnam
    </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    msg: String
  }
}
</script>

<style scoped>
footer{
    background-color: black;
    height: 1em;
    width: 100%;
    bottom: 0;
    position: absolute;
    font-family: 'Montserrat';
    font-size: 16px;
    text-align: center;

}

</style>
