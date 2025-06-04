<template>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <div class="col-12 text-center">
          <div class="footer-content">
            <div class="social-links mb-3">
              <a href="https://github.com/" target="_blank" class="social-link">
                <i class="fab fa-github"></i>
              </a>
              <a href="https://www.linkedin.com/feed/" target="_blank" class="social-link">
                <i class="fab fa-linkedin"></i>
              </a>
              <a href="mailto:malonjualure@gmail.com" class="social-link">
                <i class="fas fa-envelope"></i>
              </a>
            </div>
            <p class="copyright">
              &copy; 2025 Laure Malonju. Tous droits réservés.
            </p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  background: var(--card-bg);
  backdrop-filter: blur(10px);
  padding: 2rem 0;
  margin-top: 2rem;
  box-shadow: 0 -5px 20px rgba(0, 0, 0, 0.1);
}

.footer-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.social-links {
  display: flex;
  gap: 1.5rem;
  margin-bottom: 1rem;
}

.social-link {
  color: var(--primary-color);
  font-size: 1.5rem;
  transition: all 0.3s ease;
}

.social-link:hover {
  color: var(--accent-color);
  transform: translateY(-3px);
}

.copyright {
  color: var(--text-color);
  margin: 0;
  font-size: 0.9rem;
  opacity: 0.8;
}
</style> 