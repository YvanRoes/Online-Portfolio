<script>
export default {
  name: 'Portfolio',
  data() {
    return {
      fullName: 'Salah Eddin Aouragh',
      profession: 'Web and App Developer',
      aboutText: "Hello, I'm Salah Eddin Aouragh. Currently pursuing IT studies at Hogeschool Inholland, I am a dedicated and motivated IT student with a genuine passion for programming. My goal is to contribute to the field of technology by applying my skills and knowledge. Born in Haarlem and having spent a significant part of my childhood in Morocco, I have gained invaluable cultural experiences and perspectives. In my free time I like to study about history, especially generals, battles, and wars.",
      skills: ['HTML', 'CSS', 'JavaScript', 'Vue.js', 'Bootstrap', 'Linux', 'Php', 'Java', 'C#']
    };
  }
};
</script>

<style scoped>
.portfolio {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  font-family: 'Arial', sans-serif;
  background-color: #f5f5f5;
  border-radius: 10px;
}

header h1 {
  font-size: 36px;
  margin-bottom: 10px;
  color: #333;
}

header p {
  font-size: 20px;
  color: #666;
  margin-bottom: 20px;
}

section {
  margin-bottom: 30px;
}

section h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

ul {
  list-style-type: disc;
  padding: 0;
  margin-bottom: 10px;
}
</style>


<template>
  <div class="bg-gradient-to-r from-indigo-600 to-purple-900" >
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
      </main>
    </div>
  </div>
</template>
