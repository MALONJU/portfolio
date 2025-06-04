<script>
import Home from './components/Home.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
import Resume from './components/Resume.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Home,
    About,
    Projects,
    Skills,
    Contact,
    Resume,
    Footer
  },
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId)
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' })
      }
    }
  }
}
</script>

<template>
  <div class="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
      <div class="container">
        <a class="navbar-brand" href="#">Laure Bibiche</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link" href="#" @click="scrollToSection('home')">Accueil</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#about" @click="scrollToSection('about')">À propos</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#resume" @click="scrollToSection('resume')">CV</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#projects" @click="scrollToSection('projects')">Projets</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#skills" @click="scrollToSection('skills')">Compétences</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#contact" @click="scrollToSection('contact')">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <main>
      <Home />
      <About />
      <Resume />
      <Projects />
      <Skills />
      <Contact />
    </main>

    <Footer />
  </div>
</template>

<style>
@import 'bootstrap/dist/css/bootstrap.min.css';
@import '@fortawesome/fontawesome-free/css/all.min.css';

main {
  padding-top: 56px;
}

.navbar {
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.nav-link {
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: var(--bs-primary) !important;
}
</style>
