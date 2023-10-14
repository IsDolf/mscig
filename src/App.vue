<template>
  <h1 class="text-center m-3">Marin Santaleza</h1>
  <h4 class="text-center m-3 mb-5">Days without smoking</h4>

  <div class="d-flex justify-content-center">
    <div class="dot"><p class='display-1 fw-bold m-auto'>{{ daysPassed }}</p></div>
  </div>
  <p class="text-center m-5">
{{ randomBenefit }}
  </p>
</template>

<script setup>
import dayjs from "dayjs"

const startDate = dayjs("2023-10-01");
const currentDate = dayjs();

const daysPassed = currentDate.diff(startDate, 'day');

const benefits = [
  "Improved Lung Function",
  "Reduced Risk of Disease",
  "Increased Energy Levels",
  "Better Sense of Taste and Smell",
  "Improved Circulation",
  "Enhanced Skin Health",
  "Savings on Finances",
  "Better Oral Health",
  "Improved Quality of Life",
  "Decreased Risk of Stroke",
  "Lowered Blood Pressure",
  "Reduced Risk of Heart Attack",
  "Improved Fertility",
  "Enhanced Exercise Performance",
  "Reduced Coughing and Wheezing",
  "Decreased Risk of Chronic Obstructive Pulmonary Disease (COPD)",
  "Improved Mood and Mental Health",
  "Decreased Risk of Cataracts",
  "Lowered Risk of Diabetes",
  "Improved Immune System Function",
  "Reduced Risk of Osteoporosis",
  "Better Hearing",
  "Improved Sense of Well-Being",
  "Enhanced Senses",
  "Increased Life Expectancy",
];

function getRandomBenefit(benefits) {
  const randomIndex = Math.floor(Math.random() * benefits.length);
  return benefits[randomIndex];
}

const randomBenefit = getRandomBenefit(benefits);
</script>

<style scoped>
.dot {
  height: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 250px;
  background-color: #bbb;
  border-radius: 50%;
  background-color: #8ec5fc;
  background-image: linear-gradient(62deg, #8ec5fc 0%, #e0c3fc 100%);
}

</style>
