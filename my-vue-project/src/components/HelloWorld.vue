<template>
  <div class="section">
    <img src="https://play-lh.googleusercontent.com/Aqp_wNSGx1JGiuOD5FHk3fa5iQcZ2NzB9hy75N5lBrDm2OrQ_Jnka7__-yXQe1pjHCM" alt="Sample Image" class="image" />
    <img src="https://upload.wikimedia.org/wikipedia/ru/thumb/8/8a/FC_Real_Madrid_Logo.svg/186px-FC_Real_Madrid_Logo.svg.png" alt="Sample Image" class="image" />
    <img src="https://upload.wikimedia.org/wikipedia/en/thumb/a/a7/Paris_Saint-Germain_F.C..svg/1200px-Paris_Saint-Germain_F.C..svg.png" alt="Sample Image" class="image" />
    <p>
      This is a sample section with an image and text. Customize this as needed.
    </p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

.image {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

p {
  margin-top: 20px;
  font-size: 18px;
  color: #333;
  text-align: center;
  max-width: 600px;
}
</style>
