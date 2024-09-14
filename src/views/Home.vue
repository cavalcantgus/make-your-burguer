<template>
  <Banner/>
  <div class="main-container">
    <h1>HOME</h1>
    <v-btn color="secundary" @click="showForm">Fazer pedido</v-btn>

    <BurguerForm
    :visible="formVisible"
    @save="saveOrder"
    @cancel="cancelOrder"/>
  </div>
</template>

<script>
import BurguerForm from '@/components/BurguerForm.vue'
import Banner from '../components/Banner.vue'

export default {
  name: 'Home',
  components: {
    Banner,
    BurguerForm
  },
  data() {
    return {
      formVisible: false
    }
  },
  methods: {
    showForm() {
      this.formVisible = true
    },
    saveOrder() {
      console.log('Pedido feito')
      this.cancelOrder()
    },
    cancelOrder() {
      this.formVisible = false
    }
  }     
}

</script>
