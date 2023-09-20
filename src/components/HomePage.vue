<template>
  <div class="home">
    <div class="header">
      <h1>Welcome to My Portfolio</h1>
      <p class="subtitle">Exploring the World of Information Technology</p>
    </div>
    <div class="content">
      <p>
        Hello, I'm Tanvir Rahman Taiyeb, a passionate first-year university student on a quest to conquer the ever-evolving realm of Information Technology.
      </p>
      <p>
        My journey began with a curious mind and a determination to harness the power of technology to shape the future. From coding to problem-solving, I've embraced the challenges of this dynamic field with unwavering enthusiasm.
      </p>
      <p>
        As a tech enthusiast, I'm constantly exploring the latest trends and innovations. Whether it's mastering new programming languages, building innovative projects, or staying up-to-date with cutting-edge tech, I'm always ready to dive in.
      </p>
      <p>
        Beyond the digital world, I find solace in the pages of books, especially those on technology, science fiction, and fantasy. When I'm not immersed in code, you'll likely find me hiking along nature trails, reconnecting with the great outdoors.
      </p>
    </div>
    <div class="skills">
      <h2>Skills</h2>
      <ul class="skills-list">
        <li class="skill-item">
          <i class="fas fa-check-circle"></i>
          <span class="skill-text">Web Development with HTML, CSS, JavaScript, and Vue.js</span>
        </li>
        <li class="skill-item">
          <i class="fas fa-check-circle"></i>
          <span class="skill-text">Problem Solving and Critical Thinking</span>
        </li>
        <li class="skill-item">
          <i class="fas fa-check-circle"></i>
          <span class="skill-text">Continuous Learning and Adaptability</span>
        </li>
        <li class="skill-item">
          <i class="fas fa-check-circle"></i>
          <span class="skill-text">Effective Team Collaboration</span>
        </li>
        <li class="skill-item">
          <i class="fas fa-check-circle"></i>
          <span class="skill-text">Stay Up-to-Date with Technology Trends</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
/* Add home page styles here */

.home {
  padding: 20px;
  text-align: center;
  background-color: #f0f0f0;
}

.header {
  background-color: #007BFF;
  color: white;
  padding: 20px;
  border-radius: 8px 8px 0 0;
}

.header h1 {
  font-size: 36px;
  margin-bottom: 10px;
}

.subtitle {
  font-size: 18px;
  margin-top: 5px;
}

.content {
  background-color: white;
  padding: 20px;
  border-radius: 0 0 8px 8px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  line-height: 1.6;
  text-align: left;
  font-size: 18px;
}

.skills {
  margin-top: 40px; /* Increased margin-top for separation */
}

.skills h2 {
  font-size: 24px;
  margin-bottom: 20px; /* Increased margin-bottom for separation */
}

.skills-list {
  list-style-type: disc; /* Add this line to display bullet points */
  padding: 0;
  text-align: left;
}

.skill-item {
  display: flex;
  align-items: center;
  margin-bottom: 15px; /* Increased margin-bottom for spacing */
}

.skill-item i {
  margin-right: 10px;
  font-size: 24px;
  color: #007BFF; /* Added a color to icons */
}

.skill-text {
  font-size: 18px;
  color: #333; /* Added a color to skill text */
}
</style>
