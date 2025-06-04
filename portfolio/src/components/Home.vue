<template>
  <div class="home min-vh-100 d-flex align-items-center" @mousemove="handleMouseMove">
    <div class="particles-container" ref="particlesContainer"></div>
    <div class="animated-background"></div>
    <div class="container text-center position-relative">
      <div class="name-container" :style="getParallaxStyle(20)">
        <h1 class="glitch-text" data-text="Bibiche Laure">Bibiche Laure</h1>
      </div>
      
      <div class="typing-container" :style="getParallaxStyle(10)">
        <h2 class="typed-text mb-4"></h2>
      </div>

      <div class="skills-cloud" :style="getParallaxStyle(-10)">
        <span class="skill-tag" v-for="(skill, index) in skills" :key="index" 
              :style="{ 
                animationDelay: `${index * 0.2}s`,
                transform: `rotate(${Math.random() * 20 - 10}deg)`
              }">
          {{ skill }}
        </span>
      </div>

      <div class="mt-5 button-container" :style="getParallaxStyle(5)">
        <a href="#" class="glow-button me-3">
          <span class="button-content">Voir mon CV</span>
          <span class="button-glow"></span>
        </a>
        <a href="#about" class="neon-button">
          <span class="button-content">En savoir plus</span>
          <span class="button-border"></span>
        </a>
      </div>

      <div class="scroll-indicator" :style="getParallaxStyle(-5)">
        <div class="mouse">
          <div class="wheel"></div>
        </div>
        <div class="arrow-scroll">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      skills: [
        'Vue.js', 'React', 'Node.js', 'Spring Boot',
        'JavaScript', 'TypeScript', 'Java', 'Python',
        'DevOps', 'Git', 'Docker', 'AWS'
      ],
      mouseX: 0,
      mouseY: 0
    }
  },
  mounted() {
    this.initTypeWriter();
    this.initParticles();
  },
  methods: {
    handleMouseMove(e) {
      this.mouseX = (e.clientX / window.innerWidth - 0.5) * 2;
      this.mouseY = (e.clientY / window.innerHeight - 0.5) * 2;
    },
    getParallaxStyle(intensity) {
      return {
        transform: `translate(${this.mouseX * intensity}px, ${this.mouseY * intensity}px)`
      }
    },
    initTypeWriter() {
      const text = "Développeuse Web Full Stack";
      const typedTextElement = this.$el.querySelector('.typed-text');
      let i = 0;
      
      const type = () => {
        if (i < text.length) {
          typedTextElement.textContent += text.charAt(i);
          i++;
          setTimeout(type, Math.random() * 100 + 50);
        }
      };
      
      setTimeout(type, 1000);
    },
    initParticles() {
      const canvas = document.createElement('canvas');
      const container = this.$refs.particlesContainer;
      container.appendChild(canvas);
      const ctx = canvas.getContext('2d');
      
      const particles = [];
      const particleCount = 50;
      
      function resize() {
        canvas.width = container.offsetWidth;
        canvas.height = container.offsetHeight;
      }
      
      class Particle {
        constructor() {
          this.reset();
        }
        
        reset() {
          this.x = Math.random() * canvas.width;
          this.y = Math.random() * canvas.height;
          this.size = Math.random() * 2 + 1;
          this.speedX = Math.random() * 2 - 1;
          this.speedY = Math.random() * 2 - 1;
          this.opacity = Math.random() * 0.5 + 0.2;
        }
        
        update() {
          this.x += this.speedX;
          this.y += this.speedY;
          
          if (this.x < 0 || this.x > canvas.width) this.speedX *= -1;
          if (this.y < 0 || this.y > canvas.height) this.speedY *= -1;
        }
        
        draw() {
          ctx.beginPath();
          ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
          ctx.fillStyle = `rgba(255, 255, 255, ${this.opacity})`;
          ctx.fill();
        }
      }
      
      function init() {
        resize();
        for (let i = 0; i < particleCount; i++) {
          particles.push(new Particle());
        }
      }
      
      function animate() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        particles.forEach(particle => {
          particle.update();
          particle.draw();
        });
        requestAnimationFrame(animate);
      }
      
      window.addEventListener('resize', resize);
      init();
      animate();
    }
  }
}
</script>

<style scoped>
.home {
  position: relative;
  overflow: hidden;
  background: linear-gradient(135deg, #1a1a1a, #2a2a2a);
}

.particles-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.animated-background {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(125deg, #1a1a1a, #2d2d2d, #1a1a1a);
  background-size: 400% 400%;
  animation: gradientShift 15s ease infinite;
  opacity: 0.8;
}

.container {
  z-index: 2;
}

.name-container {
  margin-bottom: 2rem;
  transition: transform 0.1s ease-out;
}

.glitch-text {
  font-size: 4.5rem;
  font-weight: bold;
  color: white;
  text-shadow: 2px 2px rgba(255, 255, 255, 0.2);
  position: relative;
  animation: glitch 5s infinite;
}

.glitch-text::before,
.glitch-text::after {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.glitch-text::before {
  left: 2px;
  text-shadow: -2px 0 #ff00c1;
  clip: rect(44px, 450px, 56px, 0);
  animation: glitch-anim 5s infinite linear alternate-reverse;
}

.glitch-text::after {
  left: -2px;
  text-shadow: -2px 0 #00fff9, 2px 2px #ff00c1;
  animation: glitch-anim2 1s infinite linear alternate-reverse;
}

.typing-container {
  height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.typed-text {
  font-size: 2rem;
  color: white;
  border-right: 3px solid var(--accent-color);
  padding-right: 5px;
  animation: blink 0.7s infinite;
}

.skills-cloud {
  margin: 2rem 0;
  perspective: 1000px;
}

.skill-tag {
  display: inline-block;
  padding: 0.5rem 1rem;
  margin: 0.5rem;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(5px);
  border-radius: 20px;
  color: white;
  font-weight: 500;
  animation: floatIn 0.5s ease-out forwards;
  opacity: 0;
  transform-origin: center;
}

.button-container {
  position: relative;
  z-index: 2;
}

.glow-button, .neon-button {
  position: relative;
  padding: 1rem 2rem;
  font-size: 1.1rem;
  font-weight: 600;
  text-decoration: none;
  overflow: hidden;
  transition: all 0.3s ease;
  border-radius: 30px;
}

.glow-button {
  background: var(--primary-color);
  color: white;
  border: none;
}

.neon-button {
  background: transparent;
  color: white;
  border: 2px solid var(--accent-color);
}

.button-content {
  position: relative;
  z-index: 1;
}

.button-glow {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at center, var(--accent-color) 0%, transparent 70%);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.glow-button:hover .button-glow {
  opacity: 0.5;
  animation: pulse 1.5s infinite;
}

.neon-button:hover {
  box-shadow: 0 0 20px var(--accent-color);
  text-shadow: 0 0 8px var(--accent-color);
}

@keyframes gradientShift {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

@keyframes glitch-anim {
  0% { clip: rect(31px, 9999px, 94px, 0); }
  4.166666666666666% { clip: rect(91px, 9999px, 100px, 0); }
  8.333333333333332% { clip: rect(85px, 9999px, 41px, 0); }
  12.5% { clip: rect(54px, 9999px, 93px, 0); }
  16.666666666666664% { clip: rect(66px, 9999px, 25px, 0); }
  20.833333333333336% { clip: rect(67px, 9999px, 75px, 0); }
  25% { clip: rect(67px, 9999px, 11px, 0); }
  29.166666666666668% { clip: rect(44px, 9999px, 27px, 0); }
  33.33333333333333% { clip: rect(73px, 9999px, 37px, 0); }
  37.5% { clip: rect(51px, 9999px, 46px, 0); }
  41.66666666666667% { clip: rect(89px, 9999px, 64px, 0); }
  45.83333333333333% { clip: rect(8px, 9999px, 42px, 0); }
  50% { clip: rect(78px, 9999px, 4px, 0); }
  54.166666666666664% { clip: rect(86px, 9999px, 49px, 0); }
  58.333333333333336% { clip: rect(12px, 9999px, 86px, 0); }
  62.5% { clip: rect(65px, 9999px, 62px, 0); }
  66.66666666666666% { clip: rect(52px, 9999px, 47px, 0); }
  70.83333333333334% { clip: rect(96px, 9999px, 78px, 0); }
  75% { clip: rect(6px, 9999px, 46px, 0); }
  79.16666666666666% { clip: rect(25px, 9999px, 37px, 0); }
  83.33333333333334% { clip: rect(85px, 9999px, 85px, 0); }
  87.5% { clip: rect(96px, 9999px, 53px, 0); }
  91.66666666666666% { clip: rect(56px, 9999px, 71px, 0); }
  95.83333333333334% { clip: rect(14px, 9999px, 77px, 0); }
  100% { clip: rect(67px, 9999px, 91px, 0); }
}

@keyframes glitch-anim2 {
  0% { clip: rect(65px, 9999px, 99px, 0); }
  100% { clip: rect(93px, 9999px, 18px, 0); }
}

@keyframes blink {
  0%, 100% { border-color: transparent; }
  50% { border-color: var(--accent-color); }
}

@keyframes floatIn {
  from {
    opacity: 0;
    transform: translateY(20px) rotateX(45deg);
  }
  to {
    opacity: 1;
    transform: translateY(0) rotateX(0);
  }
}

@keyframes pulse {
  0% { transform: scale(1); opacity: 0.5; }
  50% { transform: scale(1.05); opacity: 0.8; }
  100% { transform: scale(1); opacity: 0.5; }
}

.scroll-indicator {
  position: absolute;
  bottom: 2rem;
  left: 50%;
  transform: translateX(-50%);
  opacity: 0.7;
  transition: opacity 0.3s ease;
}

.mouse {
  width: 26px;
  height: 42px;
  border: 2px solid rgba(255, 255, 255, 0.8);
  border-radius: 13px;
  margin: 0 auto;
  position: relative;
}

.wheel {
  width: 4px;
  height: 8px;
  background: white;
  border-radius: 2px;
  position: absolute;
  top: 6px;
  left: 50%;
  transform: translateX(-50%);
  animation: scroll 1.5s infinite;
}

.arrow-scroll {
  padding-top: 10px;
}

.arrow-scroll span {
  display: block;
  width: 10px;
  height: 10px;
  border-bottom: 2px solid rgba(255, 255, 255, 0.8);
  border-right: 2px solid rgba(255, 255, 255, 0.8);
  transform: rotate(45deg);
  margin: -5px auto;
  animation: arrow 2s infinite;
}

.arrow-scroll span:nth-child(2) {
  animation-delay: -0.2s;
}

.arrow-scroll span:nth-child(3) {
  animation-delay: -0.4s;
}

@keyframes scroll {
  0% {
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }
  100% {
    opacity: 0;
    transform: translateX(-50%) translateY(20px);
  }
}

@keyframes arrow {
  0% {
    opacity: 0;
    transform: rotate(45deg) translate(-20px, -20px);
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: rotate(45deg) translate(20px, 20px);
  }
}
</style> 