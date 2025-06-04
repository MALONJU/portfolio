<template>
  <div class="about py-5" id="about">
    <div class="container">
      <h2 class="text-center mb-5">À Propos</h2>
      <div class="row">
        <div class="col-md-4 mb-4 mb-md-0">
          <div class="card h-100">
            <div class="card-body text-center">
              <img src="../assets/BIBICHE.png" alt="Photo de profil" class="img-fluid rounded-circle mb-4" style="width: 200px; height: 200px; object-fit: cover;">
              <h3 class="mb-3">Laure Bibiche</h3>
              <p class="lead mb-4">Développeur Full Stack</p>
              <div class="d-flex justify-content-center gap-3">
                <a href="https://github.com/" target="_blank" class="btn btn-outline-dark">
                  <i class="fab fa-github"></i>
                </a>
                <a href="https://www.linkedin.com/feed/" target="_blank" class="btn btn-outline-primary">
                  <i class="fab fa-linkedin"></i>
                </a>
                <a href="/cv.pdf" download class="btn btn-outline-success">
                  <i class="fas fa-download"></i>
                </a>
              </div>
            </div>
          </div>
        </div>

        <div class="col-md-8">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="mb-4">Mon Parcours</h3>
              <p class="lead">Développeur Web passionné par la création d'applications web modernes et performantes, avec une expertise particulière en Vue.js, Node.js  avec express.js et java spring boot et les technologies web modernes.</p>
              
              <div class="mb-4">
                <h4 class="mb-3">Points Forts</h4>
                <div class="row g-3">
                  <div class="col-md-6">
                    <div class="strength-item p-3">
                      <i class="fas fa-code text-primary me-2"></i>
                      <strong>Full Stack</strong>
                      <p class="mb-0">Maîtrise du développement frontend et backend</p>
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="strength-item p-3">
                      <i class="fas fa-project-diagram text-primary me-2"></i>
                      <strong>Gestion de Projet</strong>
                      <p class="mb-0">Expérience en méthodologies Agile/Scrum</p>
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="strength-item p-3">
                      <i class="fas fa-database text-primary me-2"></i>
                      <strong>Bases de données</strong>
                      <p class="mb-0">SQL et NoSQL</p>
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="strength-item p-3">
                      <i class="fas fa-tools text-primary me-2"></i>
                      <strong>DevOps</strong>
                      <p class="mb-0">CI/CD, Docker, Cloud</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="mb-4">
                <h4 class="mb-3">Ce que je recherche</h4>
                <ul class="list-unstyled">
                  <li class="mb-2">
                    <i class="fas fa-check text-success me-2"></i>
                    Opportunités en développement web full stack
                  </li>
                  <li class="mb-2">
                    <i class="fas fa-check text-success me-2"></i>
                    Projets innovants et challengeants
                  </li>
                  <li class="mb-2">
                    <i class="fas fa-check text-success me-2"></i>
                    Collaboration en équipe
                  </li>
                  <li class="mb-2">
                    <i class="fas fa-check text-success me-2"></i>
                    Environnement favorisant l'apprentissage continu
                  </li>
                </ul>
              </div>

              <div>
                <h4 class="mb-3">Langues</h4>
                <div class="row g-3">
                  <div class="col-md-6">
                    <div class="language-item">
                      <div class="d-flex justify-content-between mb-2">
                        <span>Allemand</span>
                        <span class="badge bg-primary">B1</span>
                      </div>
                      <div class="progress">
                        <div class="progress-bar" role="progressbar" style="width: 65%"></div>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-6">
                    <div class="language-item">
                      <div class="d-flex justify-content-between mb-2">
                        <span>Anglais</span>
                        <span class="badge bg-primary">B1</span>
                      </div>
                      <div class="progress">
                        <div class="progress-bar" role="progressbar" style="width: 65%"></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about {
  background-color: #f8f9fa;
}

.card {
  border: none;
  box-shadow: 0 2px 15px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
}

.strength-item {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
}

.strength-item:hover {
  transform: translateY(-3px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.progress {
  height: 8px;
  background-color: #e9ecef;
}

.progress-bar {
  background-color: var(--bs-primary);
}

.btn-outline-dark:hover,
.btn-outline-primary:hover,
.btn-outline-success:hover {
  transform: translateY(-2px);
}

.language-item {
  margin-bottom: 1rem;
}

.list-unstyled li {
  transition: all 0.3s ease;
}

.list-unstyled li:hover {
  padding-left: 5px;
  color: var(--bs-primary);
}
</style> 