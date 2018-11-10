<template>
<div id="quiz-section">
  <h6 id="quiz-section-title">Quiz</h6>
  <p>Try one of our quick 10 question quizzes to test your knowledge</p>
  <p>Select your level</p>
  <section>
    <div id='level'>
      <button class="level-btn" id="easyBtn" @click='setLevel("easy")'>Level 1</button>
      <button class="level-btn" id="standardBtn"  @click='setLevel("standard")'>Level 2</button>
      <button class="level-btn" id="hardBtn"  @click='setLevel("hard")'>Level 3</button>
    </div>
  </section>
  <div v-if='currentQuestion != null && showResult === false' class="focus-in-expand">
    <section class="question-section focus-in-expand">
      <p class="question-index focus-in-expand">{{ currentQuestion.key }}. <span class="question-text">{{ currentQuestion.question }}</span></p>
    </section>
    <section class="answer-section focus-in-expand">
      <!-- Display Answers -->
      <div><input type="radio" class="answer-input" name="answer" :value='currentQuestion.answers[0].answer' v-model="selectedAnswer">{{ currentQuestion.answers[0].answer }}</div>
      <div><input type="radio" class="answer-input" name="answer" :value='currentQuestion.answers[1].answer' v-model="selectedAnswer">{{ currentQuestion.answers[1].answer }}</div>
      <div><input type="radio" class="answer-input" name="answer" :value='currentQuestion.answers[2].answer' v-model="selectedAnswer">{{ currentQuestion.answers[2].answer }}</div>
    </section>
    <section class="submit-section">
      <!-- submit answer -->
      <button class="btn btn-primary submit-btn" @click="submitAnswer(currentQuestion.answers[currentQuestion.correctKey - 1].answer)">Submit</button>
    </section>
  </div>
  <section class="result-section" v-if="showResult">
    <b-alert  variant="success" show>Thank you for completing the quiz. You scored {{ score }} out of 10</b-alert>
    <b-btn v-b-modal.modal>review</b-btn>

    <!-- Modal Component -->
    <b-modal id="modal" title="Your Results" :body-bg-variant="bodyBgVariant" size="lg">
      <ul>
        <li v-for="item in test" :key="item.key" style="margin-bottom:10px;" :class="{incorrect : item.status === 'incorrect'}">
          <div>
            <div class="review-question-section">
              {{ item.key }}.
              <h6 class="review-question">{{ item.question }}</h6>
            </div>
            <div class="question-validate">
              <p>Your Answer: {{ item.selectedAnswer }}</p>
              <p v-if="item.status === 'incorrect'">Correct Answer is: {{ item.answers[item.correctKey -1].answer }}</p>
            </div>
            <div>
              <p style="font-weight:bold; font-color:navy;">You were {{ item.status }}</p>
              <p>{{ item.info }}</p><br>
            </div>
          </div>
        </li>
      </ul>
    </b-modal>
  </section>
</div>
</template>

<script>
import { easy_quiz, standard_quiz, hard_quiz } from "../data/quiz.js";

export default {
  name: "quiz",
  data() {
    return {
      level: "standard",
      score: 0,
      test: null,
      index: 0,
      answerKey: 0,
      selectedAnswer: null,
      currentQuestion: null,
      showResult: false,
      bodyBgVariant: "dark"
    };
  },
  methods: {
    submitAnswer(answer) {
      //document.getElementsByClassName("answer-input").attr.selected = false;
      if (this.selectedAnswer.length < 1) {
        return;
      }
      if (this.selectedAnswer === answer) {
        this.test[this.index].status = "correct";
        this.score++;
      } else {
        this.test[this.index].status = "incorrect";
      }
      this.test[this.index].selectedAnswer = this.selectedAnswer;
      this.index += 1;
      this.currentQuestion = this.test[this.index];
      this.selectedAnswer = "";
      if (this.index >= 10) {
        this.index = 0;
        this.showResult = true;
        return;
      }
    },
    setLevel(level) {
      this.setBtn(level);
      this.level = level;
      this.showResult = false;
      this.score = 0;
      this.index = 0;
      if (this.level === "easy") {
        /* load easy quiz */
        this.test = easy_quiz;
      }
      if (this.level === "standard") {
        /* load standard quiz */
        this.test = standard_quiz;
      }
      if (this.level === "hard") {
        /* load hard quiz */
        this.test = hard_quiz;
      }
      console.log("setLevel -: index: ", this.index);
      this.currentQuestion = this.test[this.index];
    },
    setBtn(level) {
      if (level === "easy") {
        document.getElementById("easyBtn").classList.add("activeBtn");
        document.getElementById("standardBtn").classList.remove("activeBtn");
        document.getElementById("hardBtn").classList.remove("activeBtn");
      }
      if (level === "standard") {
        document.getElementById("easyBtn").classList.remove("activeBtn");
        document.getElementById("standardBtn").classList.add("activeBtn");
        document.getElementById("hardBtn").classList.remove("activeBtn");
      }
      if (level === "hard") {
        document.getElementById("easyBtn").classList.remove("activeBtn");
        document.getElementById("standardBtn").classList.remove("activeBtn");
        document.getElementById("hardBtn").classList.add("activeBtn");
      }
    }
  },
  mounted() {
    this.test = standard_quiz;
    this.score = 0;
    this.index = 0;
    this.currentQuestion = null;
  }
};
</script>

<style scoped>
/* MOBILE DEFAULT VIEW */
#quiz-section {
  background-color: rgba(0, 0, 0, 0.5);
  width:100%;
  padding:20px;
}

#level {
  margin: 0 40px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
}

.level-btn {
  width: 80px;
  font-size: 1rem;
  cursor: pointer;
  padding: 2px;
  color: #c0c0c0;
  background-color: rgba(0, 10, 75, 0.8);
  margin-bottom: 25px;
}

.level-btn:hover {
  color: red;
  background-color: navy;
  font-weight: bold;
}

.activeBtn {
  background-color: transparent;
  color: red;
}

.inactiveBtn {
  background-color: navy;
  color: #c0c0c0;
}

.answer-section {
  display: flex;
  flex-flow: column;
  align-items: flex-start;
  justify-content: flex-start;
  margin-bottom: 30px;
}

.answer-section input {
  margin: 5px 10px 0 20px;
}

.question-section {
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-wrap: wrap;
  padding-left: 5px;
}

.question-text {
  font-size: 1rem;
  text-align: left;
}

.question-index {
  margin-right: 5px;
}

.submit-section {
  display: flex;
  justify-content: center;
}

.submit-btn {
  width: 250px;
}

.review-question {
  color: #c0c0c0;
  text-shadow: 0 2px navy;
  font-weight: bold;
  font-size: 1.3rem;
  margin-bottom: 15px;
}

.review-info {
  font-style: italic;
  color: #c0c0c0;
  text-align: left;
  border-bottom: 2px solid black;
}

.review-question-section {
  display: flex;
  align-items: baseline;
  margin-bottom: 10px;
}

.modal-body {
  background-color: blue;
}

ul {
  padding: 0;
  margin: 0;
}

.incorrect {
  background-color: rgba(143, 113, 104, 0.7);
  border-radius: 4px;
  padding: 5px;
}

.question-validate {
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
}

#b-modal-body {
  background-color: black !important;
}

#quiz-section-title {
  font-size: 1.2rem;
  margin-bottom: 10px;
  color: #c0c0c0;
  text-shadow: 2px 0 red;
}

.focus-in-expand {
	-webkit-animation: focus-in-expand 0.8s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
	        animation: focus-in-expand 0.8s cubic-bezier(0.250, 0.460, 0.450, 0.940) both;
}
/**
 * ----------------------------------------
 * animation focus-in-expand
 * ----------------------------------------
 */
@-webkit-keyframes focus-in-expand {
  0% {
    letter-spacing: -0.5em;
    -webkit-filter: blur(12px);
            filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
            filter: blur(0px);
    opacity: 1;
  }
}
@keyframes focus-in-expand {
  0% {
    letter-spacing: -0.5em;
    -webkit-filter: blur(12px);
            filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
            filter: blur(0px);
    opacity: 1;
  }
}


/* MEDIUM UP VIEW */
@media screen and (min-width: 991px) {
  #quiz-section {
    width:100%;
    padding: 0 20px 20px 20px;
  }

  #quiz-section-title {
    font-size: 1.7rem;
    margin-top: 0;
    margin-bottom: 20px;
    text-shadow: 2px 0 red;
  }

  .review-question {
    text-shadow: 0 2px navy;
    font-size: 1.2rem;
    margin-bottom: 15px;
  }

  .modal-content {
    width:900px;
  }
}
</style>
