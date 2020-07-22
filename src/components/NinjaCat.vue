<template>
  <div class="container">
    <img :src="require(`../assets/${name}.png`)">
    <div>
      <button class="btn-large red darken-4 waves-effect waves-dark" @click="showNinja()">Mostrar Ninja</button>
      <button class="btn-large red darken-4 waves-effect waves-dark" @click="showCat()">Mostrar Gato</button>
    </div>
    <!-- <div id="modal1" class="modal">
      <div class="modal-content">
        <h4>Modal Header</h4>
        <p>A bunch of text</p>
      </div>
      <div class="modal-footer">
        <a href="#!" class="modal-close waves-effect waves-green btn-flat">Agree</a>
      </div>
    </div> -->
  </div>
</template>

<script>
export default {
  name: 'NinjaCat',
  props: {
    msg: String
  },
  data() {
    return{
      name: "ninja"
    }
  },
  methods: {
    showNinja() {
      this.name = "ninja";
    },
    showCat() {
      this.name = "cat";
    }
  },
  beforeUpdate() {
    alert('La imagen actual está a punto de cambiar')
  }
}
</script>

<style scoped>
.container {
  display: grid;
  place-items: center;
}
</style>
