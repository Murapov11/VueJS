<template>
  <div>
    <div class="filters">
      <button @click="filterByDate">Filter by Date</button>
      <button @click="filterByRating">Filter by Rating</button>
    </div>
    <div class="person-cards">
      <div v-for="person in people" :key="person.id" class="card">
        <img :src="person.Avatar" alt="Person Avatar">
        <h3>{{ person.PersonName }}</h3>
        <p><strong>Topic:</strong> {{ person.Topic }}</p>
        <p><strong>Date:</strong> {{ person.PubDate }}</p>
        <p><strong>Rating:</strong> {{ person.Rating }}</p>
        <p><strong>Commentary:</strong> {{ person.Commentary }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import _ from 'lodash';

export default {
  data() {
    return {
      people: [
        { id: 1, PersonName: 'John Doe', Avatar: 'avatar1.png', PubDate: '2024-09-01', Rating: 4.5, Commentary: 'Excellent!', Topic: 'Technology' },
        { id: 2, PersonName: 'Jane Smith', Avatar: 'avatar2.png', PubDate: '2024-09-03', Rating: 3.8, Commentary: 'Pretty good', Topic: 'Art' },
        { id: 3, PersonName: 'Mike Johnson', Avatar: 'avatar3.png', PubDate: '2024-08-30', Rating: 4.9, Commentary: 'Outstanding!', Topic: 'Science' },
        // Add more person objects here
      ]
    };
  },
  methods: {
    filterByDate() {
      this.people = _.orderBy(this.people, ['PubDate'], ['desc']);
    },
    filterByRating() {
      this.people = _.orderBy(this.people, ['Rating'], ['desc']);
    }
  }
};
</script>

<style>
.person-cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 20px;
}
.card {
  border: 1px solid #ccc;
  padding: 16px;
  border-radius: 8px;
  text-align: center;
}
img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}
.filters button {
  margin: 10px;
  padding: 10px;
}
</style>
