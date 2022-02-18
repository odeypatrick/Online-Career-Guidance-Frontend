<template>
  <div class="modal">
      <div class="close-btn">&times;</div>
      <div class="modal-content">
          <h3>Begin Test</h3>
          <div class="start-form">
              <form @submit.prevent="startTest" v-if="!showQuestions">
                  <div>
                    <label>Department</label>
                    <div>
                        <input type="text" placeholder="Eg. Science">
                    </div>
                  </div>
                  <div>
                    <label>Current Class of Study</label>
                    <div>
                        <input type="text" placeholder="Eg. Science">
                    </div>
                  </div>
                  <button class="btn start-btn" @click="showQuestions = !showQuestions">GET STARTED</button>
              </form>
          </div>

          <div class="questions" v-if="showQuestions">
              <Question/>
          </div>
      </div>
  </div>
</template>

<script>
import Question from './question/Question'

export default {
    components: {
        Question
    },
    data() {asdfghjkl
        return {
            showQuestions: false
        }
    },
    created(){
        // window.onclick = (e) => {
        //     if(e.target.className == 'modal') {
        //         this.$emit('close-modal')
        //     }
        // }
    },
    methods: {
        startTest(){

        }
    }
}
</script>

<style>
    .modal {
        height: 100%;
        width: 100%;
        background-color: rgba(0,0,0,0.8);
        position: fixed;
        top: 0;
        left: 0;
    }

    .modal-content {
        height: 500px;
        width: 60%;
        margin: 7% auto;
        background-color: #fff;
        color: #000;
        box-shadow: 0 0 10px 0 #1b1b1b;
        border-radius: 20px;
    }

    .close-btn {
        float: right;
        margin: 0px 10px;
        font-size: 30px;
        cursor: pointer;
        color: #ccc
    }

    .close-btn:hover {
        color: #fff
    }
</style>