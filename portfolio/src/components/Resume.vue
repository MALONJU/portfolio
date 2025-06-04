<template>
  <div class="resume py-5" id="resume">
    <div class="container">
      <h2 class="text-center mb-5">Curriculum Vitae</h2>
      
      <!-- Téléchargement CV -->
      <div class="text-center mb-5">
        <a href="/CV_Bibiche_Malonju_d (1).pdf" download class="btn btn-primary btn-lg">
          <i class="fas fa-download me-2"></i>Télécharger mon CV
        </a>
      </div>

      <!-- Sections du CV -->
      <div class="row g-4">
        <!-- Formation -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title mb-4">
                <i class="fas fa-graduation-cap text-primary me-2"></i>
                Formation
              </h3>
              <div class="timeline">
                <div class="timeline-item">
                  <span class="badge bg-primary">2025</span>
                  <h4>Formation Architecte web et mobile</h4>
                  <p class="text-muted">Digital School of paris</p>
                </div>
                <!-- Ajoutez d'autres formations ici -->
              </div>
            </div>
          </div>
        </div>

        <!-- Certifications -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title mb-4">
                <i class="fas fa-certificate text-primary me-2"></i>
                Certifications
              </h3>
              <ul class="list-unstyled">
                <li class="mb-3">
                  <i class="fas fa-check-circle text-success me-2"></i>
                  <strong>Vue.js</strong> - Vue.js Fundamentals
                </li>
                <li class="mb-3">
                  <i class="fas fa-check-circle text-success me-2"></i>
                  <strong>Spring Boot</strong> - Spring Certified Developer en cour sur Udemy
                </li>
                <!-- Ajoutez d'autres certifications ici -->
              </ul>
            </div>
          </div>
        </div>

        <!-- Langues -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title mb-4">
                <i class="fas fa-language text-primary me-2"></i>
                Langues
              </h3>
              <div class="mb-3">
                <div class="d-flex justify-content-between align-items-center mb-2">
                  <span>Allemand</span>
                  <span class="badge bg-primary">B1</span>
                </div>
                <div class="progress">
                  <div class="progress-bar" role="progressbar" style="width: 65%"></div>
                </div>
              </div>
              <div class="mb-3">
                <div class="d-flex justify-content-between align-items-center mb-2">
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

        <!-- Centres d'intérêt -->
        <div class="col-md-6">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title mb-4">
                <i class="fas fa-heart text-primary me-2"></i>
                Centres d'intérêt
              </h3>
              <div class="row g-2">
                <div class="col-6">
                  <div class="interest-item p-3 text-center">
                    <i class="fas fa-code fa-2x mb-2"></i>
                    <p>Développement</p>
                  </div>
                </div>
                <div class="col-6">
                  <div class="interest-item p-3 text-center">
                    <i class="fas fa-robot fa-2x mb-2"></i>
                    <p>Intelligence Artificielle</p>
                  </div>
                </div>
                <!-- Ajoutez d'autres centres d'intérêt ici -->
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
  name: 'Resume'
}
</script>

<style scoped>
.resume {
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

.timeline-item {
  position: relative;
  padding-left: 20px;
  margin-bottom: 30px;
  border-left: 2px solid var(--bs-primary);
}

.timeline-item:last-child {
  margin-bottom: 0;
}

.timeline-item .badge {
  margin-bottom: 10px;
}

.progress {
  height: 8px;
  background-color: #e9ecef;
}

.progress-bar {
  background-color: var(--bs-primary);
}

.interest-item {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
}

.interest-item:hover {
  transform: translateY(-3px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.interest-item i {
  color: var(--bs-primary);
}
</style> 