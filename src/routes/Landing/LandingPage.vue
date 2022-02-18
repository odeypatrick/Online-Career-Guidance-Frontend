<template>
  <div class="landing-view">
      <div class="container">
          <div class="texts">
            <h1>Career Guidiance and Counselling</h1>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae, et possimus. Vel ullam omnis illum impedit, voluptate dolorem dicta expedita.</p>
            <button class="btn" @click="showModal=true">GET STARTED</button>
        </div>
      </div>

    <Modal v-if="showModal" v-on:close-modal="showModal = false"/>
  </div>
</template>

<script>
import Modal from '../../components/modal/Modal.vue'
export default {
    components: {
        Modal
    },
    data() {
        return {
            showModal: false
        }
    },
}
</script>

<style scoped>
    .landing-view{
        height: 100vh;
        background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.9)), url('../../assets/bg.jpg');
        background-size: cover;
        color: #fff;
        background-attachment: fixed;
    }

    .landing-view .texts {
        width: 80%;
        padding-top: 10em;
        margin: 0 auto;
    }

    .texts h1, p {
        margin-bottom: 20px;
        width: 50%;
    }

    .texts .btn {
        padding: 15px 20px;
        background-color: #0088aa;
        border: none;
        border-radius: 5px;
        font-weight: bold;
        color: #fff;
        cursor: pointer;
    }
</style>