<template>
  <div class="about">
    <h2>About Me</h2>
    <p>I am a dedicated student currently pursuing a Bachelor of IT degree at Deakin University.</p>
    <p>Throughout my academic journey, I have developed a passion for technology and a keen interest in web development. I am eager to learn and apply my skills in HTML, CSS, JavaScript, and Vue.js to create innovative and user-friendly web solutions.</p>
    <p>My goal is to graduate with a strong foundation in IT, equipped with problem-solving skills and the ability to work effectively in cross-functional teams. I am excited to embark on a journey of continuous learning and growth in the ever-evolving field of technology.</p>

    <h2>My Hobbies</h2>
    <table class="hobbies-table">
      <thead>
        <tr>
          <th>Hobby</th>
          <th>Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Coding</td>
          <td>Exploring new programming languages and building projects.</td>
        </tr>
        <tr>
          <td>Technology Enthusiast</td>
          <td>Staying up-to-date with the latest tech trends and gadgets.</td>
        </tr>
        <tr>
          <td>Reading</td>
          <td>Enjoying books on technology, science fiction, and fantasy.</td>
        </tr>
        <tr>
          <td>Hiking</td>
          <td>Exploring nature trails and enjoying the great outdoors.</td>
        </tr>
        <!-- Add more hobbies as needed -->
      </tbody>
    </table>

    <h2>Additional Information</h2>
    <p v-if="showAdditionalInfo">
      I enjoy taking on new challenges and problem-solving in the world of technology. 
      Whether it's coding a complex application or designing a user-friendly website, I thrive on pushing boundaries and creating innovative solutions
    </p>

    <button @click="showAdditionalInfo = !showAdditionalInfo">
      Toggle Additional Info
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showAdditionalInfo: false,
    };
  },
};
</script>

<style scoped>
/* Add my about page styles here */
.about {
  font-size: 18px;
  line-height: 1.6;
  margin: 20px;
}

.about h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

.hobbies-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

.hobbies-table th,
.hobbies-table td {
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

.hobbies-table th {
  background-color: #f2f2f2;
}

/* Add more styles as needed */
</style>
