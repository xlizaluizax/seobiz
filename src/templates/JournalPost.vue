<template>
  <Layout>
    <div class="journal">
      <div class="container journal-container">
        <div class="journal-header">
          <h1 v-html="$page.post.title" class="journal-title"/>
          <div class="journal-meta">
            <div class="journal-author">
              <span class="label">Автор</span>
              <span class="author-name" v-text="$page.post.author"/>
            </div>
            <div class="journal-date">
              <span class="label">Дата</span>
              <div v-text="$page.post.date"/>
            </div>
            <div class="journal-time">
              <span class="label">Чтение займет</span>
              <span>{{ $page.post.timeToRead }} min read</span>
            </div>
          </div>
        </div>

        <JournalContent :content="$page.post.content"/>
      </div>
    </div>
  </Layout>
</template>

<page-query>
query JournalPost ($path: String!) {
  post: journalPost (path: $path) {
    title
    author
    date (format: "D. MMMM YYYY")
    timeToRead
    content
  }
}
</page-query>

<script>
import JournalContent from "@/components/JournalContent";

export default {
  components: {
    JournalContent
  },
  metaInfo() {
    return {
      title: this.$page.post.title
    };
  }
};
</script>

<style scoped>
.journal-container {
  max-width: 1200px;
}
.journal-header {
  padding: 1rem 0 3rem 0;
}
.journal-title {
  font-size: 4rem;
  margin: 0 0 3rem 0;
  padding: 0;
}
.journal-meta {
  display: flex;
  flex-wrap: wrap;
  font-size: 1rem;
}
.journal-meta > div {
  margin-right: 3rem;
}
.journal-meta > div:last-of-type {
  margin: 0;
}
</style>
