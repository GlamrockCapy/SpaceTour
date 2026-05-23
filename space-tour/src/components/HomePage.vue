<template>
  <div class="home-page">
    <!-- Home Section -->
    <section id="home" class="section section--hero">
      <div class="hero__content">
        <h1 class="hero__title">Добро пожаловать в SpaceTour</h1>
        <p class="hero__subtitle">Исследуй космос с нами</p>
        <button class="hero__button">Начать приключение</button>
      </div>
    </section>

    <!-- Popular Travels Section -->
    <section id="popular" class="section section--popular">
      <div class="container">
        <h2 class="section__title">Популярные путешествия</h2>
        <p class="section__description">Выбери одно из наших популярных маршрутов</p>
        <div class="tours__grid">
          <div class="tour-card">
            <div class="tour-card__image">🌙</div>
            <h3 class="tour-card__title">На Луну</h3>
            <p class="tour-card__description">3 дня на поверхности Луны</p>
          </div>
          <div class="tour-card">
            <div class="tour-card__image">🔴</div>
            <h3 class="tour-card__title">На Марс</h3>
            <p class="tour-card__description">Месячное путешествие на красную планету</p>
          </div>
          <div class="tour-card">
            <div class="tour-card__image">🪐</div>
            <h3 class="tour-card__title">Тур по планетам</h3>
            <p class="tour-card__description">Галактическое путешествие по всей системе</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Tour Constructor Section -->
    <section id="constructor" class="section section--constructor">
      <div class="container">
        <h2 class="section__title">Конструктор путешествия</h2>
        <p class="section__description">Создай своё уникальное путешествие по космосу</p>
        <button class="constructor__button">Создать путешествие</button>
      </div>
    </section>

    <!-- Physical Test Section -->
    <section id="test" class="section section--test">
      <div class="container">
        <h2 class="section__title">Тест физических способностей</h2>
        <p class="section__description">Проверь, готов ли ты к космическому путешествию</p>
        <button class="test__button">Пройти тест</button>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style scoped>
.home-page {
  width: 100%;
}

.section {
  padding: 4rem 2rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section__title {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
  color: #1e40af;
  text-align: center;
}

.section__description {
  font-size: 1.1rem;
  color: #666;
  text-align: center;
  margin-bottom: 2rem;
}

/* Hero Section */
.section--hero {
  background: linear-gradient(135deg, #1e40af 0%, #3b82f6 100%);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 500px;
}

.hero__content {
  text-align: center;
}

.hero__title {
  font-size: 3rem;
  margin-bottom: 1rem;
  font-weight: bold;
}

.hero__subtitle {
  font-size: 1.5rem;
  margin-bottom: 2rem;
  opacity: 0.9;
}

.hero__button,
.constructor__button,
.test__button {
  background: white;
  color: #1e40af;
  border: none;
  padding: 1rem 2rem;
  font-size: 1.1rem;
  border-radius: 8px;
  cursor: pointer;
  font-weight: bold;
  transition: all 0.3s ease;
}

.hero__button:hover,
.constructor__button:hover,
.test__button:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

/* Popular Tours Section */
.section--popular {
  background: #f8f9fa;
}

.tours__grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.tour-card {
  background: white;
  border-radius: 8px;
  padding: 2rem;
  text-align: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.tour-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.tour-card__image {
  font-size: 4rem;
  margin-bottom: 1rem;
}

.tour-card__title {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  color: #1e40af;
}

.tour-card__description {
  color: #666;
  font-size: 1rem;
}

/* Constructor Section */
.section--constructor {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.section--constructor .section__title,
.section--constructor .section__description {
  color: white;
}

/* Test Section */
.section--test {
  background: #f8f9fa;
}

/* Адаптивность */
@media (max-width: 768px) {
  .section {
    padding: 2rem 1rem;
  }

  .section__title {
    font-size: 2rem;
  }

  .hero__title {
    font-size: 2rem;
  }

  .hero__subtitle {
    font-size: 1.2rem;
  }

  .tours__grid {
    grid-template-columns: 1fr;
  }
}
</style>
