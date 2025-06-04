<template>
  <div class="skills py-5" id="skills">
    <div class="container">
      <h2 class="text-center mb-5">Compétences</h2>
      <div class="row g-4">
        <!-- Frontend -->
        <div class="col-md-6 col-lg-4">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title text-center mb-4">
                <i class="fas fa-laptop-code text-primary"></i>
                Frontend
              </h3>
              <ul class="list-unstyled">
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Vue.js</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>React</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>JavaScript</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>HTML5/CSS3</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Tailwind</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Bootstrap</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Backend -->
        <div class="col-md-6 col-lg-4">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title text-center mb-4">
                <i class="fas fa-server text-primary"></i>
                Backend
              </h3>
              <ul class="list-unstyled">
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Java (Spring Boot)</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Node.js / Express.js</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>.NET Core</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Django</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Symfony</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>PHP</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Bases de données -->
        <div class="col-md-6 col-lg-4">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title text-center mb-4">
                <i class="fas fa-database text-primary"></i>
                Bases de données
              </h3>
              <ul class="list-unstyled">
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Firebase</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>MariaDB</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>PostgreSQL</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>MySQL</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>SQL Server</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Gestion de projet -->
        <div class="col-md-6 col-lg-4">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title text-center mb-4">
                <i class="fas fa-tasks text-primary"></i>
                Gestion de projet
              </h3>
              <ul class="list-unstyled">
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Jira</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Trello</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>GanttProject</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Scrum / Kanban</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Documentation</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Spécifications</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- DevOps & Outils -->
        <div class="col-md-6 col-lg-4">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title text-center mb-4">
                <i class="fas fa-tools text-primary"></i>
                DevOps & Outils
              </h3>
              <ul class="list-unstyled">
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Git / GitHub</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Docker</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>CI/CD</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>VS Code / IntelliJ</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Ubuntu / Windows</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Swagger</li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Autres compétences -->
        <div class="col-md-6 col-lg-4">
          <div class="card h-100">
            <div class="card-body">
              <h3 class="card-title text-center mb-4">
                <i class="fas fa-plus-circle text-primary"></i>
                Autres compétences
              </h3>
              <ul class="list-unstyled">
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>ERP</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Pack Office</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Google Workspace</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Allemand (B1)</li>
                <li class="mb-2"><i class="fas fa-check text-success me-2"></i>Anglais (B1)</li>
              </ul>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills'
}
</script>

<style scoped>
.card {
  transition: transform 0.3s ease;
}
.card:hover {
  transform: translateY(-5px);
}
.card-title i {
  font-size: 2rem;
  margin-bottom: 1rem;
  display: block;
}

.list-unstyled li {
  transition: all 0.3s ease;
}

.list-unstyled li:hover {
  padding-left: 5px;
  color: var(--bs-primary);
}
</style> 