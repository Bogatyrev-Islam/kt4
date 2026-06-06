<script setup>
const topSellingProducts = [
  { id: 1, name: 'Calathea Orbifolia', price: 'Rs. 359/-', img: '/rose-gold-image.png', desc: 'Famous for its beautiful oversized striped leaves.' },
  { id: 2, name: 'Fiddle Leaf Fig', price: 'Rs. 420/-', img: '/plant2.png', desc: 'The ultimate statement plant with lush, glossy foliage.' },
  { id: 3, name: 'Snake Plant', price: 'Rs. 299/-', img: '/plant4.png', desc: 'An indestructible air purifier that thrives anywhere.' },
  { id: 4, name: 'Boston Fern', price: 'Rs. 310/-', img: '/plant5.png', desc: 'Adds a vibrant splash of emerald green to your room.' },
  { id: 5, name: 'Monstera Deliciosa', price: 'Rs. 450/-', img: '/plant6.png', desc: 'Iconic split leaves that bring instant jungle vibes.' },
  { id: 6, name: 'Peace Lily', price: 'Rs. 380/-', img: '/plant3.png', desc: 'Elegant white blooms that filter indoor air beautifully.' }
]
</script>

<template>
  <main class="catalog-page">
    <section class="hero-section">
      <h1 class="hero-title">Breathe Natural</h1>
      <p class="section-description">
        Transform your living space into a refreshing green oasis. Discover our handpicked collection of indoor plants
        that purify the air and bring peace to your mind.
      </p>
      <div class="hero-actions">
        <button class="btn btn-outline">Explore</button>
        <button class="btn btn-link">▶ Live Demo</button>
      </div>
    </section>

    <div class="glass-card plant-accent-card">
      <img src="/rose-gold-image.png" alt="Trendy House Plant" class="card-image">
      <div class="card-body">
        <p class="section-description">Trendy House Plant</p>
        <h2 class="card-title">Calathea Plant</h2>
        <button class="btn btn-outline">Buy Now</button>
      </div>
    </div>

    <div class="glass-card client-review-card">
      <div class="client-profile">
        <img src="/client-avatar.jpg" alt="Alena Patel" class="avatar">
        <div class="profile-info">
          <h3 class="client-name">Alena Patel</h3>
          <p class="rating-stars">★★★★★</p>
        </div>
      </div>
      <p class="review-text">
        «Absolutely love my new Calathea! It arrived in perfect condition and completely changed the vibe of my home
        office. Highly recommend this shop!»
      </p>
    </div>

    <section class="catalog-section">
      <h2 class="section-title">Our Trendy Plants</h2>

      <div class="glass-card alternative-card">
        <img src="/plant2.png" alt="For Small Decs Ai Plant" class="alt-card-image">
        <div class="alt-card-body">
          <h3 class="card-title">Stylish Desktop Companion</h3>
          <p class="section-description">
            Perfectly sized for compact workspaces, shelves, or nightstands. This low-maintenance plant adds an instant
            touch of aesthetic modern style to any corner.
          </p>
          <span class="price-tag">Rs. 599/-</span>
          <div class="alt-card-actions">
            <button class="btn btn-outline">Explore</button>
            <button class="btn btn-outline">Buy Now</button>
          </div>
        </div>
      </div>

      <div class="glass-card alternative-card img-right">
        <div class="alt-card-body">
          <h3 class="card-title">Minimalist Living Room Decor</h3>
          <p class="section-description">
            Bring life to your empty corners. Features rich, deep green foliage that effortlessly blends with
            Scandinavian, mid-century, or industrial interiors.
          </p>
          <span class="price-tag">Rs. 579/-</span>
          <div class="alt-card-actions">
            <button class="btn btn-outline">Explore</button>
            <button class="btn btn-outline">Buy Now</button>
          </div>
        </div>
        <img src="/plant3.png" alt="For Small Decs Ai Plant" class="alt-card-image">
      </div>
    </section>

    <section class="catalog-section">
      <h2 class="section-title">Our Top Selling</h2>
      <div class="products-grid">
        <div v-for="product in topSellingProducts" :key="product.id" class="glass-card product-card">
          <img :src="product.img" :alt="product.name" class="card-image">
          <div class="card-body">
            <h3 class="card-title">{{ product.name }}</h3>
            <p class="section-description">{{ product.desc }}</p>
            <div class="product-footer">
              <span class="price-tag">{{ product.price }}</span>
              <button class="btn btn-inline-buy">Buy Now</button>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped>
.catalog-page {
  padding: 90px 60px;
}

.catalog-section {
  margin-top: 100px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 130px;
}

.section-title {
  font-size: 50px;
}

.section-description {
  font-size: 23px;
  color: rgba(255, 255, 255, 0.75);
}

.glass-card {
  background-color: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(25px);
  border-right: 2px solid rgba(255, 255, 255, 0.2);
  border-bottom: 2px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0px 0px 9px rgba(0, 0, 0, 0.25);
}

.btn {
  background: none;
  border: none;
  cursor: pointer;
  font-size: 28px;
}

.btn-outline {
  padding: 15px 60px;
  border: 2px solid #FFFFFF;
  border-radius: 12px;
}

.btn-link {
  font-size: 20px;
}

.hero-section {
  width: 800px;
}

.hero-title {
  font-size: 110px;
}

.hero-actions {
  display: flex;
  gap: 35px;
  margin-top: 20px;
}

.plant-accent-card {
  position: absolute;
  top: 250px;
  right: 60px;
  padding: 0 20px 60px;
  width: 425px;
  height: 525px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  gap: 30px;
  border-radius: 77px;
}

.card-image {
  margin: auto;
  width: 375px;
  height: 375px;
}

.card-body {
  padding: 0 40px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 15px;
}

.card-title {
  font-size: 38px;
}

.client-review-card {
  margin-top: 200px;
  padding: 15px 40px 50px;
  width: 400px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  gap: 30px;
  border-radius: 45px;
}

.client-profile {
  display: flex;
  align-items: center;
  gap: 30px;
}

.avatar {
  width: 65px;
  height: 65px;
  border-radius: 50%;
}

.client-name,
.rating-stars {
  font-size: 23px;
}

.rating-stars {
  color: #FFF84E;
}

.review-text {
  font-size: 20px;
  color: rgba(255, 255, 255, 0.75);
  font-style: italic;
}

.alternative-card {
  padding: 0 35px;
  width: 100%;
  height: 500px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-end;
  gap: 200px;
  border-radius: 77px;
}

.alt-card-image {
  height: 700px;
}

.alt-card-body {
  margin: auto;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.alternative-card .card-title {
  font-size: 38px;
}

.alternative-card .section-description {
  font-size: 20px;
}

.price-tag {
  font-size: 28px;
}

.alt-card-actions {
  display: flex;
  gap: 20px;
}

.img-right {
  flex-direction: row;
}

.products-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 35px;
}

.product-card {
  margin-bottom: 100px;
  padding: 0 20px 60px;
  width: 400px;
  height: 475px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  gap: 30px;
  border-radius: 77px;
}

.product-card .card-body {
  gap: 15px;
}

.product-footer {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn-inline-buy {
  padding: 15px;
  border: 2px solid #FFFFFF;
  border-radius: 12px;
}
</style>