<template>
  <div class="blog-container">
    <h1>Mini Blog</h1>
    <div class="blog-grid">
      <div
        v-for="(post, index) in blogPosts"
        :key="index"
        class="blog-post"
        :class="{
          'left-post-1': index === 0,
          'left-post-2': index === 1,
          'center-post': index === 2,
          'right-post-1': index === 3,
          'right-post-2': index === 4
        }"
      >
        <img :src="post.image" :alt="post.title" class="blog-image" />
        <div class="blog-content">
          <p>{{ post.title }}</p>
          <span>{{ post.date }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      blogPosts: [
        {
          title: 'Barsa',
          date: 'July 19, 2019',
          image: 'https://play-lh.googleusercontent.com/Aqp_wNSGx1JGiuOD5FHk3fa5iQcZ2NzB9hy75N5lBrDm2OrQ_Jnka7__-yXQe1pjHCM'
        },
        {
          title: 'Real',
          date: 'July 19, 2019',
          image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/8/8a/FC_Real_Madrid_Logo.svg/186px-FC_Real_Madrid_Logo.svg.png'
        },
        {
          title: 'PSG.',
          date: 'July 19, 2019',
          image: 'https://upload.wikimedia.org/wikipedia/en/thumb/a/a7/Paris_Saint-Germain_F.C..svg/1200px-Paris_Saint-Germain_F.C..svg.png'
        },
        {
          title: 'Bayern',
          date: 'July 19, 2019',
          image: 'https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/FC_Bayern_M%C3%BCnchen_logo_%282017%29.svg/640px-FC_Bayern_M%C3%BCnchen_logo_%282017%29.svg.png'
        },
        {
          title: 'Atletico',
          date: 'July 19, 2019',
          image: 'https://upload.wikimedia.org/wikipedia/ru/thumb/0/01/FC_Atletico_Madrid_Logo.svg/195px-FC_Atletico_Madrid_Logo.svg.png'
        }
      ]
    };
  }
}
</script>

<style scoped>
.blog-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

h1 {
  text-align: center;
  font-size: 2em;
  margin-bottom: 20px;
}

.blog-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas: 
    "left1 center right1"
    "left2 center right2";
  gap: 20px;
}

.blog-post {
  position: relative;
  overflow: hidden;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.blog-image {
  width: 100%;
  height: auto;
  display: block;
}

.blog-content {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.6);
  color: white;
  padding: 10px;
  font-size: 1.1em;
  transition: background 0.3s ease-in-out;
}

.blog-content p {
  margin: 0;
  font-weight: bold;
}

.blog-content span {
  font-size: 0.9em;
}

.blog-post:hover .blog-content {
  background: rgba(0, 0, 0, 0.8);
}
</style>
