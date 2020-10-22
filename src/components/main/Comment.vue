<template>
  <div class="comment-container">
    <div class="button-wrapper">
      <v-dialog v-model="dialog.on" width="500">
        <template v-slot:activator="{ on, attrs }">
          <button v-bind="attrs" v-on="on">
            댓글 {{ comments.length }}개 모두 보기
          </button>
        </template>
        <comment-push
          :comments="comments"
          :user-img="userImg"
          :index="index"
          :dialog="dialog"
        ></comment-push>
      </v-dialog>
    </div>
    <div class="comments-wrapper">
      <v-row
        v-for="(comment, i) in comments"
        :key="i"
        align="center"
        no-gutters
      >
        <p>
          <strong>{{ comment.name }}</strong> {{ comment.text }}
        </p>
        <v-spacer></v-spacer>
        <v-btn icon><v-icon>mdi-heart-outline</v-icon></v-btn>
      </v-row>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Comment',
    props: ['comments', 'userImg', 'index'],
    components: {
      CommentPush: () => import('@/components/main/CommentPush.vue'),
    },
    data() {
      return {
        dialog: {on: false},
      };
    },
  };
</script>

<style lang="scss" scoped>
  .comment-container {
    padding: 0 16px;
  }
  .comments-wrapper {
    p {
      margin-bottom: 0;
    }
  }
  .button-wrapper {
    button {
      color: gray;
      margin-bottom: 5px;
    }
  }
</style>
