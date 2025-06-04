<template>
  <div class="projects py-5" id="projects">
    <div class="container">
      <h2 class="text-center mb-5">Projets Représentatifs</h2>
      <div class="row g-4">
        <!-- Système de Gestion de Bibliothèque -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <div class="d-flex justify-content-between align-items-start mb-2">
                <h5 class="card-title">Système de Gestion de Bibliothèque</h5>
                <span class="badge bg-primary">2025</span>
              </div>
              <p class="card-text">Projet Agile en équipe simulant un environnement DSI. Gestion complète des ressources d'une bibliothèque.</p>
              <div class="mb-3">
                <h6 class="mb-2">Fonctionnalités clés :</h6>
                <ul class="list-unstyled">
                  <li><i class="fas fa-check text-success me-2"></i>Gestion d'utilisateurs et emprunts</li>
                  <li><i class="fas fa-check text-success me-2"></i>Notifications en temps réel</li>
                  <li><i class="fas fa-check text-success me-2"></i>Documentation Swagger</li>
                  <li><i class="fas fa-check text-success me-2"></i>Tests et recette fonctionnelle</li>
                </ul>
              </div>
              <div class="tech-stack mb-3">
                <span class="badge bg-secondary me-1">Git</span>
                <span class="badge bg-secondary me-1">Docker</span>
                <span class="badge bg-secondary me-1">Agile</span>
                <span class="badge bg-secondary me-1">Swagger</span>
              </div>
              <div class="d-flex gap-2">
                <a href="https://github.com/library-management-system" target="_blank" class="btn btn-outline-dark">
                  <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://library-demo.herokuapp.com" target="_blank" class="btn btn-primary">
                  <i class="fas fa-external-link-alt"></i> Démo
                </a>
              </div>
            </div>
          </div>
        </div>

        <!-- Application de Signature Électronique -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <div class="d-flex justify-content-between align-items-start mb-2">
                <h5 class="card-title">Application de Signature Électronique</h5>
                <span class="badge bg-primary">2024</span>
              </div>
              <p class="card-text">Application complète de signature électronique avec authentification sécurisée et notifications par email.</p>
              <div class="mb-3">
                <h6 class="mb-2">Réalisations :</h6>
                <ul class="list-unstyled">
                  <li><i class="fas fa-check text-success me-2"></i>Authentification JWT</li>
                  <li><i class="fas fa-check text-success me-2"></i>Emails automatiques (Nodemailer)</li>
                  <li><i class="fas fa-check text-success me-2"></i>Tests unitaires</li>
                  <li><i class="fas fa-check text-success me-2"></i>Déploiement Heroku</li>
                </ul>
              </div>
              <div class="tech-stack mb-3">
                <span class="badge bg-secondary me-1">Vue.js</span>
                <span class="badge bg-secondary me-1">Node.js</span>
                <span class="badge bg-secondary me-1">Express.js</span>
                <span class="badge bg-secondary me-1">JWT</span>
                <span class="badge bg-secondary me-1">Heroku</span>
              </div>
              <div class="d-flex gap-2">
                <a href="https://github.com/e-signature-app" target="_blank" class="btn btn-outline-dark">
                  <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://e-signature-demo.herokuapp.com" target="_blank" class="btn btn-primary">
                  <i class="fas fa-external-link-alt"></i> Démo
                </a>
              </div>
            </div>
          </div>
        </div>

        <!-- Analyse de Sentiments Twitter -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <div class="d-flex justify-content-between align-items-start mb-2">
                <h5 class="card-title">Analyse de Sentiments Twitter</h5>
                <span class="badge bg-primary">2024</span>
              </div>
              <p class="card-text">API REST pour l'analyse de sentiments des tweets avec traitement de données et visualisation.</p>
              <div class="mb-3">
                <h6 class="mb-2">Points clés :</h6>
                <ul class="list-unstyled">
                  <li><i class="fas fa-check text-success me-2"></i>API REST avec Spring Boot</li>
                  <li><i class="fas fa-check text-success me-2"></i>Traitement NLTK/Text Blob</li>
                  <li><i class="fas fa-check text-success me-2"></i>Dashboard de visualisation</li>
                  <li><i class="fas fa-check text-success me-2"></i>Déploiement AWS Lambda</li>
                </ul>
              </div>
              <div class="tech-stack mb-3">
                <span class="badge bg-secondary me-1">Spring Boot</span>
                <span class="badge bg-secondary me-1">AWS Lambda</span>
                <span class="badge bg-secondary me-1">NLTK</span>
                <span class="badge bg-secondary me-1">REST API</span>
              </div>
              <div class="d-flex gap-2">
                <a href="https://github.com/twitter-sentiment-analysis" target="_blank" class="btn btn-outline-dark">
                  <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://twitter-sentiment-demo.aws.com" target="_blank" class="btn btn-primary">
                  <i class="fas fa-external-link-alt"></i> Démo
                </a>
              </div>
            </div>
          </div>
        </div>

        <!-- Application de Gestion de Tâches -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <div class="d-flex justify-content-between align-items-start mb-2">
                <h5 class="card-title">Application de Gestion de Tâches</h5>
                <span class="badge bg-primary">2024</span>
              </div>
              <p class="card-text">Application desktop avec architecture MVVM pour la gestion de tâches et projets.</p>
              <div class="mb-3">
                <h6 class="mb-2">Caractéristiques :</h6>
                <ul class="list-unstyled">
                  <li><i class="fas fa-check text-success me-2"></i>Architecture MVVM</li>
                  <li><i class="fas fa-check text-success me-2"></i>Tests d'intégration</li>
                  <li><i class="fas fa-check text-success me-2"></i>Documentation utilisateur</li>
                  <li><i class="fas fa-check text-success me-2"></i>Déploiement Azure</li>
                </ul>
              </div>
              <div class="tech-stack mb-3">
                <span class="badge bg-secondary me-1">C#</span>
                <span class="badge bg-secondary me-1">WPF</span>
                <span class="badge bg-secondary me-1">MVVM</span>
                <span class="badge bg-secondary me-1">Azure</span>
              </div>
              <div class="d-flex gap-2">
                <a href="https://github.com/task-management-wpf" target="_blank" class="btn btn-outline-dark">
                  <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://task-manager-demo.azure.com" target="_blank" class="btn btn-primary">
                  <i class="fas fa-external-link-alt"></i> Démo
                </a>
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
  name: 'Projects'
}
</script>

<style scoped>
.card {
  transition: transform 0.3s ease;
  border: none;
  box-shadow: 0 2px 15px rgba(0,0,0,0.1);
}

.card:hover {
  transform: translateY(-5px);
}

.tech-stack .badge {
  font-size: 0.8rem;
  padding: 0.5em 0.8em;
  margin-bottom: 0.5rem;
}

.list-unstyled li {
  margin-bottom: 0.5rem;
}

.card-title {
  color: var(--bs-primary);
  font-weight: 600;
}

.badge.bg-primary {
  font-weight: 500;
  font-size: 0.8rem;
}
</style> 