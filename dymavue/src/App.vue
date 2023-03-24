<template>
  <form @submit.prevent="ajoutTodo">
    <label for="add-todo">Ajouter une tâche</label>
    <input v-model="tache" id="add-todo" placeholder="Tâche à effectuer..." />
    <button>Ajouter</button>
  </form>
  <ul>
    <template v-for="(todo, index) in todos" :key="todo.id">
      <li>
        {{ todo.titre }}
        <button @click="suppTodo(todo.id)">Supprimer</button>
      </li>
    </template>
  </ul>
</template>


<script setup lang="ts">
import { ref } from 'vue';

const tache = ref('');
const todos = ref([
  {
    id: 1,
    titre: 'Apprendre VueJS3',
  },
  {
    id: 2,
    titre: 'Réussir le test technique',
  },
  {
    id: 3,
    titre: 'Décrocher le stage :)',
  },

]);

let nouvelleTacheId = 4;

function ajoutTodo() {
  todos.value.push({
    id: nouvelleTacheId++,
    titre: tache.value,
  });
  tache.value = '';
}

function suppTodo(id) {
  const index = todos.value.findIndex((todo) => todo.id === id);
  if (index !== -1) {
    todos.value.splice(index, 1);
  }
}

</script>
