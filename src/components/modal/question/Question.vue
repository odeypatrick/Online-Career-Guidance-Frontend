<template>
    <div>
        <h1>Questions</h1>

        <div class="questions">
            <div class="question-item" v-for="(question, index) in questions" :key="index">
                <div>
                    {{ question.text }} <small>{{ question.department }}</small>
                </div>
                <div class="checkboxes">
                    <input type="radio" v-model="question.value" value="0" @change="addNum(question.department, index)">
                    <input type="radio" v-model="question.value" value="1" @change="addNum(question.department, index)">
                    <input type="radio" v-model="question.value" value="2" @change="addNum(question.department, index)">
                    <input type="radio" v-model="question.value" value="3" @change="addNum(question.department, index)">
                </div>
            </div>

            <button class="btn" @click="getCourse">Get Course</button>
            <br><br>
            <div class="votes">
                <div class="depts" v-for="(department, index) in departments" :key="index">
                    {{ department.name }}: {{ department.value }} votes
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Question from '../../../Question'

export default {
    data() {
        return {
            questions: Question,
            departments: [
                { name: "Biology", value: 0 },
                { name: "Chemistry", value: 0 },
                { name: "Physics", value: 0 },
                { name: "Maths", value: 0 },
                { name: "PE", value: 0 }
            ],

        }
    },
    methods: {
        addNum(questionDepartment, index) {
            this.departments.forEach(department => {
                if(department.name == questionDepartment) {
                    department.value += Number(this.questions[index].value)
                }
            })
        },
        getCourse() {
            let val = 0;
            this.questions.forEach(question => {
                if(question.department == "PE") {
                    val = val + Number(question.value)
                }
            })
            console.log(val)
        }
    }
}
</script>

<style scoped>
    .question-item {
        display: flex;
        justify-content: space-between;
        margin-bottom: 20px;
    }

    .questions {
        padding: 10px;
    }

    .checkboxes {
        display: flex
    }

    .checkboxes  input {
        margin-right: 10px;
    }
</style>



