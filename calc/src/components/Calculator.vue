<template>
  <div class="p-3" style="max-width: 400px; margin: 50px auto; background: #234">
    <div style="color:aqua; text-align: right; background: #31475e; margin: 0 3px 5px 3px;">
      {{calculatorValue || 0}}
    </div>

  <div class="row no-gutters">
    <div class="col-3" v-for="n in calculatorElements" :key="n">
    <div class="lead" @click="action(n)">
      {{n}}
    </div>  
    </div>
  </div>
  </div>
</template>


<script>


export default {
  name: 'Calculator',
  props: {
    msg: String
  },

  data() {
    return {
      calculatorValue: '',
      calculatorElements: ['X', '*', '/', '-', 
                          7, 8, 9, '+', 
                          4, 5, 6, '%', 
                          1, 2, 3, '=',
                          0, '.'],
    operator: null,
    previousCalculatorValue: '',
    }
  },

  methods: {
    action(n){
      if(!isNaN(n) || n === '.'){
        this.calculatorValue += n + '';
      }

      if (n === 'X') {
        this.calculatorValue = '';
      }

      if (n === '%') {
        this.calculatorValue = this.calculatorValue / 100 + '';
      }

      if (['/', '*', '-', '+'].includes(n)){
        this.operator = n;
        this.previousCalculatorValue = this.calculatorValue;
        this.calculatorValue = '';
      }

      if(n === '=') {
        this.calculatorValue = eval(
          this.previousCalculatorValue + this.operator + this.calculatorValue
        );

        this.previousCalculatorValue = '';
        this.operator = null;
      }
    }
  }
}

</script>

<style scoped>
  .bg-vue-dark {
    background: #31475e;
  }

  .lead{
    vertical-align: middle;
    color: white;
    text-align: center;
    background: #31475e;
    margin: 3px;
    height: 40px;
  }

  .lead:hover {
    cursor: pointer;
    background:dimgrey;
  }

</style>
