<template>
    <div class="projects">
      <h2>My Projects</h2>
      <transition-group name="fade" tag="div">
        <div class="project" v-for="project in projects" :key="project.id">
          <div class="project-header" @click="toggleDetails(project.id)">
            <h3>{{ project.title }}</h3>
            <span class="expand-icon" v-if="!project.showDetails">▼</span>
            <span class="expand-icon" v-else>▲</span>
          </div>
          <transition name="slide-fade" mode="out-in">
            <div v-if="project.showDetails" class="project-details">
              <p><strong>Overview:</strong> {{ project.description }}</p>
              <div class="key-learning">
                <h4>Key Learning Objectives:</h4>
                <ul>
                  <li v-for="(objective, index) in project.objectives" :key="index">{{ objective }}</li>
                </ul>
              </div>
              <div class="project-highlights">
                <h4>Project Highlights:</h4>
                <p>{{ project.highlights }}</p>
              </div>
              <div class="skills-gained">
                <h4>Skills Gained:</h4>
                <ul>
                  <li v-for="(skill, index) in project.skills" :key="index">{{ skill }}</li>
                </ul>
              </div>
            </div>
          </transition>
        </div>
      </transition-group>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        projects: [
          {
            id: 1,
            title: 'SIT 103 - Database Fundamentals',
            description: 'SIT 103 introduced me to the fundamentals of designing, implementing, and managing relational database systems. I learned how to create Entity-Relationship (ER) diagrams to model real-world data and how to interact with relational databases using SQL.',
            showDetails: false,
            objectives: [
              'Constructing ER diagrams that accurately represent real-world objects.',
              'Writing SQL queries to manipulate and retrieve data from relational databases.'
            ],
            highlights: 'One of the key highlights was designing an ER diagram for a hypothetical business scenario, ensuring that the model\'s semantics matched those of the real-world object it represented.',
            skills: [
              'Data modeling using ER diagrams',
              'SQL database management and querying'
            ],
          },
          {
            id: 2,
            title: 'SIT 182 - Real World Practices for Cyber Security',
            description: 'SIT 182 provided a practical understanding of cybersecurity by analyzing realistic case studies. I learned to identify and manage risks in communication networks, as well as detect and respond to cyber threats.',
            showDetails: false,
            objectives: [
              'Evaluating risks in network management.',
              'Understanding threats and vulnerabilities.',
              'Developing strategies to prevent and respond to cyberattacks.'
            ],
            highlights: 'Our team worked on a simulated cybersecurity incident response scenario, which required us to develop and implement a strategy to mitigate the threat.',
            skills: [
              'Cybersecurity risk assessment and management',
              'Incident response planning'
            ],
          },
          {
            id: 3,
            title: 'MIS201 - Digital Business Analysis',
            description: 'MIS201 introduced me to the fundamental concepts and methods of business analysis. I gained experience in identifying business opportunities, exploring stakeholder problems, and proposing solutions to satisfy client needs.',
            showDetails: false,
            objectives: [
              'Identifying business opportunities and problems.',
              'Using business analysis techniques such as brainstorming, interviews, and creative problem solving.',
              'Presenting proposals to clients.'
            ],
            highlights: 'I led a group project where we analyzed a real-world business case, conducted stakeholder interviews, and presented a comprehensive solution that met the client\'s requirements.',
            skills: [
              'Business analysis techniques',
              'Stakeholder management and communication'
            ],
          },
          {
            id: 4,
            title: 'SIT224 - Information Technology Systems and Innovation',
            description: 'SIT224 explored the role of information technology in transforming industries and society. I learned about current and emerging technologies and their impact on various sectors.',
            showDetails: false,
            objectives: [
              'Understanding the connection between IT and industry/society.',
              'Practical project planning and management.'
            ],
            highlights: 'I worked on a group project that involved creating a project plan for implementing a modern IT solution. This allowed me to understand the coordination required for successful IT projects.',
            skills: [
              'Technology trends analysis',
              'Project planning and coordination'
            ],
          },
          // Add more project objects here
        ],
      };
    },
    methods: {
      toggleDetails(projectId) {
        const project = this.projects.find((p) => p.id === projectId);
        if (project) {
          project.showDetails = !project.showDetails;
        }
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add project section styles here */
  .projects {
    font-size: 18px;
    line-height: 1.6;
    margin: 20px;
  }
  
  .projects h2 {
    font-size: 24px;
    margin-bottom: 20px;
  }
  
  .project {
    margin-bottom: 30px;
    padding: 20px;
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  .project h3 {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 20px;
    margin-bottom: 10px;
    cursor: pointer;
  }
  
  .expand-icon {
    font-size: 20px;
  }
  
  .project-details {
    background-color: #f8f8f8;
    padding: 10px;
    border: 1px solid #ddd;
    margin-top: 10px;
  }
  
  .key-learning ul,
  .skills-gained ul {
    list-style-type: disc;
    padding-left: 20px;
  }
  
  /* Fade transition effect */
  .fade-enter-active, .fade-leave-active {
    transition: opacity 0.5s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
    opacity: 0;
  }
  
  /* Slide-fade transition effect */
  .slide-fade-enter-active {
    transition: all 0.5s ease;
  }
  .slide-fade-leave-active {
    transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
  }
  .slide-fade-enter, .slide-fade-leave-to /* .slide-fade-leave-active in <2.1.8 */ {
    transform: translateY(10px);
    opacity: 0;
  }
  </style>
  