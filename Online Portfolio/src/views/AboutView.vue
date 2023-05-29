<script>
export default {
  name: 'Portfolio',
  data() {
    return {
      fullName: 'Salah Eddin Aouragh',
      profession: 'Web Developer',
      aboutText: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer sed leo in nunc sodales scelerisque. Quisque iaculis nisi ut tristique iaculis.',
      skills: ['HTML', 'CSS', 'JavaScript', 'Vue.js', 'Bootstrap'],
      projects: [
        {
          id: 1,
          name: 'Project 1',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
        {
          id: 2,
          name: 'Project 2',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        },
        {
          id: 3,
          name: 'Project 3',
          description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
        }
      ],
      email: 'yourname@example.com',
      phoneNumber: '+1234567890',
      address: '123 Main Street, City, Country'
    };
  }
};
</script>

<style scoped>
.portfolio {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  font-family: Arial, sans-serif;
}

header h1 {
  font-size: 30px;
  margin-bottom: 10px;
}

header p {
  font-size: 18px;
  color: #666;
  margin-bottom: 20px;
}

section {
  margin-bottom: 40px;
}

section h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

ul {
  list-style-type: none;
  padding: 0;
}

.projects {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 20px;
}

.project {
  padding: 10px;
  border: 1px solid #ccc;
}

footer p {
  font-size: 16px;
  color: #666;
  margin-bottom: 10px;
}
</style>


<template>
    <div class="portfolio">
      <header>
        <h1>{{ fullName }}</h1>
        <p>{{ profession }}</p>
      </header>
      <main>
        <section>
          <h2>About Me</h2>
          <p>{{ aboutText }}</p>
        </section>
        <section>
          <h2>Skills</h2>
          <ul>
            <li v-for="skill in skills" :key="skill">{{ skill }}</li>
          </ul>
        </section>
        <section>
          <h2>Projects</h2>
          <div class="projects">
            <div v-for="project in projects" :key="project.id" class="project">
              <h3>{{ project.name }}</h3>
              <p>{{ project.description }}</p>
            </div>
          </div>
        </section>
      </main>
      <footer>
        <p>{{ email }}</p>
        <p>{{ phoneNumber }}</p>
        <p>{{ address }}</p>
      </footer>
    </div>
</template>
