<template>
  <div class="ma-10">
    <center>
      <h1 class="indigo--text">Encontre um professor próximo a você</h1>
    </center>
    <!-- div Search -->
    <SearchForm />

    <!-- Lista de professores -->
    <TeacherList />
    <!-- ... -->
    <!-- card info professor -->
    <!-- ... -->
  </div>
</template>

<script>
import SearchForm from "../components/content/teacher-search/SearchForm";
import TeacherList from "../components/content/teacher-search/TeacherList";
export default {
  name: "TeacherSearch",
  components: {
    SearchForm,
    TeacherList
  }
};
</script>

<style scoped></style>
