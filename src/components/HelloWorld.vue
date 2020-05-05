<template>
  <div class="elemento" :class="addClass" @click="seleccionar()" ></div>
</template>

<script>
export default {
  name: "hello-world",
  data() {
    return {
      isSelected: false
    };
  },
  computed:{
    addClass(){
      return this.isSelected? "seleccionado": "";
    }
  },
  methods:{
    seleccionar(){
      this.$emit('hijo-seleccionado')
      this.isSelected = !this.isSelected
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.elemento {
  height: 40px;
  width: 40px;
  margin: 80px;
  border-color: black;
  border-style: solid;
  border-width: 2px;
}

.seleccionado{
  background-color: blue;
}
</style>
