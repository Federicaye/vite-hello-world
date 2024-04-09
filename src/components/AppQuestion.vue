<template>
    <div>
        <button @click="computerScienceQuestion">start quiz</button>
       
        <div v-for="(question, index) in arrayQuestion" :key="index">
            <p>{{ arrayQuestion[index].question }}</p>
            <input type="radio" :value="index" name="answer" v-model="selectedOptions">
            <label>{{ arrayQuestion[index].correct_answer }}</label>
            <input type="radio" :value="index" name="answer" v-model="selectedOptions">
            <label>{{ arrayQuestion[index].incorrect_answers[0] }}</label>
            <input type="radio" :value="index" name="answer" v-model="selectedOptions">
            <label>{{ arrayQuestion[index].incorrect_answers[1] }}</label>
            <input type="radio" :value="index" name="answer" v-model="selectedOptions">
            <label>{{ arrayQuestion[index].incorrect_answers[2] }}</label> 
        </div>
       
    </div>
</template>

<script>
import axios from 'axios';
export default {
    name: 'AppQuestion',
    data() {
        return {
            selectedOption: false,
            arrayQuestion: []

        }
    },
    methods: {
        computerScienceQuestion() {
            axios.get('https://opentdb.com/api.php?amount=10&category=18&difficulty=easy&type=multiple').then((response) => {
                this.computerQuestions = response.data.results[0].question;
                this.answers = response.data.results[0].incorrect_answers;
                this.answer = response.data.results[0].correct_answer;
                this.arrayQuestion = response.data.results;
                console.log(this.arrayQuestion);

            })
        }
    }
}
</script>

<style lang="scss" scoped></style>