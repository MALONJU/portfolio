<template>
  <div class="contact py-5" id="contact">
    <div class="container">
      <h2 class="text-center mb-5">Contact</h2>
      <div class="row">
        <div class="col-md-6 mb-4 mb-md-0">
          <form @submit.prevent="handleSubmit" class="card p-4">
            <div class="mb-3">
              <label for="name" class="form-label">Nom</label>
              <input type="text" class="form-control" id="name" v-model="form.name" required>
            </div>
            <div class="mb-3">
              <label for="email" class="form-label">Email</label>
              <input type="email" class="form-control" id="email" v-model="form.email" required>
            </div>
            <div class="mb-3">
              <label for="message" class="form-label">Message</label>
              <textarea class="form-control" id="message" rows="5" v-model="form.message" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary" :disabled="loading">
              <span v-if="loading" class="spinner-border spinner-border-sm me-2" role="status"></span>
              {{ loading ? 'Envoi...' : 'Envoyer' }}
            </button>
          </form>
        </div>
        <div class="col-md-6">
          <div class="card p-4">
            <h3 class="mb-4">Retrouvez-moi sur</h3>
            <div class="d-flex flex-column gap-3">
              <a href="https://www.linkedin.com/feed/" target="_blank" class="btn btn-outline-primary">
                <i class="fab fa-linkedin me-2"></i>LinkedIn
              </a>
              <a href="https://github.com/" target="_blank" class="btn btn-outline-dark">
                <i class="fab fa-github me-2"></i>GitHub
              </a>
              <a href="mailto:malonjualure@gmail.com" class="btn btn-outline-info">
                <i class="fas fa-envelope me-2"></i>malonjualure@gmail.com
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      loading: false,
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    async handleSubmit() {
      this.loading = true
      try {
        // Envoyer le formulaire à votre service de messagerie
        const formData = {
          name: this.form.name,
          email: this.form.email,
          message: this.form.message,
          to: 'malonjualure@gmail.com'
        }
        
        // Simuler l'envoi (à remplacer par votre logique d'envoi réelle)
        await new Promise(resolve => setTimeout(resolve, 1000))
        
        // Réinitialiser le formulaire
        this.form = { name: '', email: '', message: '' }
        alert('Message envoyé avec succès!')
      } catch (error) {
        alert('Une erreur est survenue. Veuillez réessayer.')
      } finally {
        this.loading = false
      }
    }
  }
}
</script>

<style scoped>
.contact {
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

.btn {
  padding: 0.8rem 1.5rem;
  font-weight: 500;
  transition: all 0.3s ease;
}

.btn i {
  font-size: 1.2rem;
}

.btn-outline-primary:hover {
  background-color: #0077b5;
  border-color: #0077b5;
}

.btn-outline-dark:hover {
  background-color: #24292e;
  border-color: #24292e;
}

.btn-outline-info:hover {
  background-color: #0dcaf0;
  border-color: #0dcaf0;
}
</style> 