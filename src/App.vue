<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: "soma",
    };
  },
  methods: {
    calcularResultado() {
      const num1 = parseFloat(this.numero1);
      const num2 = parseFloat(this.numero2);

      if (this.operacao === "soma") {
        return num1 + num2;
      } else if (this.operacao === "subtracao") {
        return num1 - num2;
      } else if (this.operacao === "multiplicacao") {
        return num1 * num2;
      } else if (this.operacao === "divisao") {
        return num1 / num2;
      }
    },
  },
};
</script>
<template>
  <div>
    <div class="campos">
      <label>Inserir um valor:</label>
      <input type="number" v-model="numero1" />
      <label>Inserir um valor:</label>
      <input type="number" v-model="numero2" />
    </div>
    <select v-model="operacao">
      <option value="soma">Soma</option>
      <option value="subtracao">Subtração</option>
      <option value="multiplicacao">Multiplicação</option>
      <option value="divisao">Divisão</option>
    </select>
    <div>
      Resultado: {{ calcularResultado() }}
    </div>
  </div>
</template>
<style scoped>
</style>