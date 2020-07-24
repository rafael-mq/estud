<template>
  <div class="d-flex flex-wrap">
    <v-card
      width="500"
      color="indigo lighten-4"
      v-for="item in teachers"
      :key="item.id"
      class="pa-3 ma-3 "
    >
      <div class="d-flex flex-no-wrap justify-space-around">
        <v-avatar class="profile rounded" tile size="120">
          <v-img :src="item.avatar" alt="123"></v-img>
          <!-- <span v-if="item.avatar">
          </span> -->
          <!-- <span v-else class="white--text headline">{{ initials(item) }}</span> -->
        </v-avatar>

        <div>
          <v-card-title>{{ item.firstName }}</v-card-title>

          <v-rating
            half-increments
            readonly
            small
            :empty-icon="ratingIcons.emptyIcon"
            :full-icon="ratingIcons.fullIcon"
            :half-icon="ratingIcons.halfIcon"
            v-model="item.rating"
          ></v-rating>
        </div>
      </div>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "TeacherList",
  data: function() {
    return {
      ratingIcons: {
        emptyIcon: "mdi-heart-outline",
        fullIcon: "mdi-heart",
        halfIcon: "mdi-heart-half-full"
      },
      teachers: [
        {
          firstName: "Rafael",
          lastName: "Moreira Queiroz",
          // avatar: "https://i.pravatar.cc/500",
          avatar:
            "https://s.gravatar.com/avatar/68b08ba8f49c2c2ac47d238c3ac38fcb?s=150",
          id: "teacher1",
          rating: 4.8
        },
        {
          firstName: "Rafael",
          lastName: "Moreira Queiroz",
          // avatar: "https://i.pravatar.cc/500",
          avatar:
            "https://s.gravatar.com/avatar/68b08ba8f49c2c2ac47d238c3ac38fcb?s=150",
          id: "teacher2",
          rating: 4.8
        },
        {
          firstName: "Rafael",
          lastName: "Moreira Queiroz",
          // avatar: "https://i.pravatar.cc/500",
          avatar:
            "https://s.gravatar.com/avatar/68b08ba8f49c2c2ac47d238c3ac38fcb?s=150",
          id: "teacher3",
          rating: 4.8
        }
      ]
    };
  },
  methods: {
    initials: teacher =>
      teacher.firstName[0].toUpperCase() +
      teacher.lastName
        .split(" ")
        .pop()[0]
        .toUpperCase()
  }
};
</script>

<style></style>
