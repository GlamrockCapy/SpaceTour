<template>
  <header class="header">
    <div class="header__container">
      <!-- Логотип -->
      <div class="header__logo">
        <svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="20" cy="20" r="15" stroke="#1e40af" stroke-width="2"/>
          <circle cx="20" cy="20" r="8" fill="#1e40af" opacity="0.5"/>
          <path d="M20 5 L25 15 L20 20 L15 15 Z" fill="#1e40af"/>
        </svg>
        <span class="header__title">SpaceTour</span>
      </div>

      <!-- Навигация -->
      <nav class="header__nav">
        <a href="#home" class="header__link">Начало</a>
        <a href="#popular" class="header__link">Популярные путешествия</a>
        <a href="#constructor" class="header__link">Конструктор путешествия</a>
        <a href="#test" class="header__link">Тест физических способностей</a>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.header {
  background: linear-gradient(135deg, #1e40af 0%, #3b82f6 100%);
  padding: 1rem 0;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 100;
}

.header__container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header__logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  text-decoration: none;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.header__logo:hover {
  transform: scale(1.05);
}

.header__title {
  font-size: 1.5rem;
  font-weight: bold;
  color: white;
  margin: 0;
}

.header__nav {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
  justify-content: flex-end;
}

.header__link {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  font-weight: 500;
  transition: all 0.3s ease;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  white-space: nowrap;
}

.header__link:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-2px);
}

.header__link:active {
  background: rgba(255, 255, 255, 0.3);
}

/* Адаптивность для мобильных устройств */
@media (max-width: 768px) {
  .header__container {
    flex-direction: column;
    gap: 1rem;
  }

  .header__nav {
    gap: 1rem;
    justify-content: center;
    width: 100%;
  }

  .header__link {
    font-size: 0.9rem;
    padding: 0.4rem 0.8rem;
  }

  .header__title {
    font-size: 1.2rem;
  }
}

@media (max-width: 480px) {
  .header__container {
    padding: 0 1rem;
  }

  .header__nav {
    gap: 0.5rem;
  }

  .header__link {
    font-size: 0.85rem;
    padding: 0.3rem 0.6rem;
  }
}
</style>
