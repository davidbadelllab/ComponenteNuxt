<template>
  <div class="hotel-booking">
    <!-- Top banner -->
    <div class="discount-banner">
      <p>🔴 Hasta 20 € de descuento en nuestra web* con el código <strong>HAPPY1ES</strong></p>
    </div>
    
    <!-- Header -->
    <header class="header">
      <div class="logo">
        <h1 class="brand-name">Weekendesk</h1>
      </div>
      <div class="header-icons">
        <button class="icon-button"><i class="fas fa-question-circle"></i></button>
        <button class="icon-button cart-icon"><span class="badge">1</span><i class="fas fa-shopping-cart"></i></button>
        <button class="icon-button"><i class="far fa-heart"></i></button>
        <button class="icon-button"><i class="far fa-user-circle"></i></button>
      </div>
    </header>

    <!-- Navigation -->
    <nav class="main-nav">
      <div class="nav-buttons">
        <button class="primary-button"><i class="fas fa-map-marker-alt"></i> Escapadas</button>
        <button class="nav-button"><i class="fas fa-gift"></i> Regalos</button>
        <button class="nav-button"><i class="fas fa-star"></i> Actividades</button>
      </div>
      <div class="nav-links">
        <a href="#" class="nav-link">Última hora</a>
        <a href="#" class="nav-link">Puente de mayo</a>
        <a href="#" class="nav-link">Verano 2025</a>
        <a href="#" class="nav-link">Nuevos hoteles</a>
        <a href="#" class="nav-link">Destino Mallorca o Cerdeña</a>
      </div>
      <div class="inspiration-dropdown">
        <button class="dropdown-button">Inspiración <i class="fas fa-chevron-down"></i></button>
      </div>
    </nav>

    <!-- Breadcrumbs -->
    <div class="breadcrumbs">
      <a href="#">Inicio</a> &gt;
      <a href="#">Escapadas fin de semana España</a> &gt;
      <a href="#">Escapadas fin de semana Región de Murcia</a> &gt;
      <a href="#">Escapadas fin de semana Murcia</a> &gt;
      <a href="#">Escapadas fin de semana Lorca</a> &gt;
      <span>Hotel Amaltea</span>
    </div>

    <!-- Hotel Header -->
    <div class="hotel-header">
      <div class="hotel-title">
        <h2>Hotel Amaltea ★★★★</h2>
        <p><i class="fas fa-map-marker-alt location-icon"></i> Lorca, Región de Murcia, España</p>
      </div>
      <div class="hotel-rating">
        <div class="rating-container">
          <span class="rating-label">Bueno</span>
          <span class="rating-score">7,9/10</span>
        </div>
        <a href="#" class="reviews-link">26 opiniones</a>
      </div>
    </div>

    <div class="page-content">
      <div class="main-content">
        <!-- Hotel Images -->
        <div class="hotel-images">
          <div class="image-grid">
            <div class="main-image-top">
              <img src="/img/hotel1.jpg" alt="Hotel pool view" />
              <button class="favorite-button"><i class="far fa-heart"></i></button>
            </div>
            <div class="main-image-top">
              <img src="/img/hotel2.jpg" alt="Hotel garden" />
            </div>
            <div class="main-image-bottom">
              <img src="/img/hotel3.jpg" alt="Hotel grounds" />
              <div class="image-badge">Último minuto</div>
            </div>
            <div class="main-image-bottom">
              <img src="/img/hotel4.jpg" alt="Hotel grounds" />
              <button class="photos-button"><i class="fas fa-camera"></i> Ver 23 fotos</button>
            </div>
          </div>
        </div>

        <!-- Hotel Offer -->
        <div class="hotel-offer">
          <h3 class="offer-title">Oferta 2025: desayuno, botella de cava y cena fría en este 4 estrellas de Lorca</h3>
          
          <div class="included-items">
            <h4 class="included-title">Tu escapada incluye</h4>
            <div class="amenities">
              <div class="amenity-item">
                <img src="/img/habitacion.jpg" alt="Habitación" />
                <p>Habitación doble estándar</p>
              </div>
              <div class="amenity-item">
                <img src="/img/breakfast.webp" alt="Desayuno" />
                <p>Desayuno bufé</p>
              </div>
              <div class="amenity-item">
                <img src="/img/botella.jpg" alt="Botella de cava" />
                <p>Botella de cava</p>
              </div>
              <div class="amenity-item">
                <img src="/img/cena.jpg" alt="Cena" />
                <p>Cena</p>
                <p class="amenity-details">Para 2 adultos<br/>Cada día</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="sidebar">
        <!-- Booking Summary -->
        <div class="booking-summary">
          <div class="price-details">
            <div class="price-top-row">
              <div class="price-left">
                <p class="nights-info">3 noches, para 2, desde</p>
                <p class="price-per-night"><span class="price">58 €</span> / noche</p>
              </div>
              <p class="discount-badge">48% de descuento</p>
            </div>
          </div>

          <div class="booking-dates">
            <div class="dates-section">
              <h4>Fechas de la estancia</h4>
              <div class="date-picker">
                <i class="far fa-calendar-alt"></i>
                <span>lun, 5 may - jue, 8 may</span>
              </div>
            </div>
            <div class="guests-section">
              <h4>Para</h4>
              <div class="guests-picker">
                <i class="fas fa-user-friends"></i>
                <span>2</span>
              </div>
            </div>
          </div>

          <div class="booking-conditions">
            <div class="condition-badge">
              <i class="fas fa-check-circle green-icon"></i>
              <span>Modificable sin gastos</span>
            </div>
            <p class="condition-details">o cancelable con reembolso parcial hasta el 2 de mayo.</p>
            <a href="#" class="more-info">Más información</a>
          </div>

          <div class="price-highlight">
            <p class="green-text"><i class="fas fa-award green-icon"></i> Mejor precio del mes</p>
          </div>

          <div class="savings">
            <div class="savings-text">Te ahorras 161 €</div>
            <span class="discount-percentage">-48%</span>
          </div>

          <hr class="divider-line">

          <div class="total-price">
            <div class="price-label">Importe total</div>
            <div class="price-value">
              <p class="original-price">335 €</p>
              <p class="final-price">174 €</p>
              <p class="tax-note">IVA incl.</p>
            </div>
          </div>

          <button class="book-button">Reservar</button>

          <div class="alternative-actions">
            <div class="divider-text">o</div>
            <button class="gift-button" @click="openModal">Regalar sin fechas</button>
          </div>
        </div>
        
        <div class="price-guarantee">
          <i class="fas fa-tag"></i>
          <p><strong>¡Este es el precio más barato</strong> para este hotel!</p>
        </div>
      </div>
    </div>

    <!-- Modal para regalar sin fechas -->
    <GiftModal :is-open="isModalOpen" @close="closeModal" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import GiftModal from './GiftModal.vue';

// Estado para controlar la apertura y cierre del modal
const isModalOpen = ref(false);

// Métodos para abrir y cerrar el modal
const openModal = () => {
  isModalOpen.value = true;
};

const closeModal = () => {
  isModalOpen.value = false;
};
</script>

<style scoped>
.hotel-booking {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
  max-width: 1200px;
  margin: 0 auto;
  color: #333;
}

/* Discount Banner */
.discount-banner {
  background-color: #f5f5f5;
  padding: 8px 0;
  text-align: center;
  font-size: 14px;
}

.discount-banner strong {
  font-weight: bold;
}

/* Header */
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
}

.brand-name {
  color: #ff4b7d;
  font-weight: bold;
  margin: 0;
  font-size: 24px;
}

.header-icons {
  display: flex;
  gap: 15px;
}

.icon-button {
  background: none;
  border: none;
  cursor: pointer;
  position: relative;
  font-size: 18px;
  color: #555;
}

.cart-icon {
  color: #ff4b7d;
}

.badge {
  position: absolute;
  top: -5px;
  right: -5px;
  background-color: #ff4b7d;
  color: white;
  border-radius: 50%;
  padding: 2px 6px;
  font-size: 10px;
}

/* Navigation */
.main-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  border-bottom: 1px solid #eee;
}

.nav-buttons {
  display: flex;
  gap: 10px;
}

.primary-button {
  background-color: #ff4b7d;
  color: white;
  border: none;
  border-radius: 20px;
  padding: 8px 16px;
  cursor: pointer;
}

.nav-button {
  background: none;
  border: none;
  padding: 8px 12px;
  cursor: pointer;
}

.nav-links {
  display: flex;
  gap: 15px;
}

.nav-link {
  color: #333;
  text-decoration: none;
  font-size: 14px;
}

.dropdown-button {
  background: none;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 5px;
}

/* Breadcrumbs */
.breadcrumbs {
  padding: 15px 20px;
  font-size: 12px;
  color: #666;
}

.breadcrumbs a {
  color: #666;
  text-decoration: none;
  margin: 0 5px;
}

.breadcrumbs a:first-child {
  margin-left: 0;
}

/* Hotel Header */
.hotel-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 15px;
  padding: 0 20px;
}

.hotel-title h2 {
  margin: 0 0 5px 0;
  font-size: 24px;
}

.location-icon {
  color: #666;
  font-size: 14px;
}

.hotel-title p {
  margin: 0;
  color: #666;
  font-size: 14px;
}

.hotel-rating {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.rating-container {
  display: flex;
  align-items: center;
}

.rating-label {
  font-weight: bold;
  margin-right: 5px;
}

.rating-score {
  font-size: 20px;
  font-weight: bold;
  color: #2ecc71;
}

.reviews-link {
  color: #0066cc;
  text-decoration: none;
  font-size: 14px;
  margin-top: 5px;
}

/* Page Layout */
.page-content {
  display: flex;
  padding: 0 20px;
}

.main-content {
  flex: 1;
  padding-right: 20px;
  max-width: 65%;
}

.sidebar {
  width: 35%;
  display: flex;
  flex-direction: column;
}

/* Hotel Images */
.hotel-images {
  margin-bottom: 20px;
}

.image-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 10px;
  position: relative;
  height: 450px;
}

.main-image-top, .main-image-bottom {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  height: 100%;
}

.main-image-top img, .main-image-bottom img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.favorite-button {
  position: absolute;
  top: 15px;
  right: 15px;
  background: white;
  border: none;
  border-radius: 50%;
  width: 30px;
  height: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.image-badge {
  position: absolute;
  bottom: 15px;
  left: 15px;
  background: rgba(255, 255, 255, 0.9);
  padding: 5px 10px;
  border-radius: 5px;
  font-size: 12px;
}

.photos-button {
  position: absolute;
  bottom: 15px;
  right: 15px;
  background: white;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 5px;
}

/* Hotel Offer */
.hotel-offer {
  margin-bottom: 20px;
}

.offer-title {
  font-size: 20px;
  font-weight: bold;
  margin-top: 0;
  margin-bottom: 20px;
}

.included-items {
  margin-top: 20px;
}

.included-title {
  font-size: 18px;
  margin-bottom: 15px;
}

.amenities {
  display: flex;
  gap: 20px;
  margin-top: 15px;
}

.amenity-item {
  flex: 1;
  text-align: center;
}

.amenity-item img {
  width: 100%;
  height: 120px;
  object-fit: cover;
  border-radius: 8px;
}

.amenity-details {
  font-size: 12px;
  color: #666;
}

/* Booking Summary */
.booking-summary {
  background-color: #ffffff;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
  border: 1px solid #eaeaea;
  margin-bottom: 15px;
}

.price-top-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 15px;
}

.price-left {
  display: flex;
  flex-direction: column;
}

.nights-info {
  font-size: 14px;
  margin: 0 0 2px 0;
  color: #333;
}

.price-per-night {
  margin: 0;
  font-size: 14px;
}

.price {
  font-weight: bold;
  color: #00a698;
  font-size: 18px;
}

.discount-badge {
  background-color: #00a698;
  color: white;
  display: inline-block;
  padding: 5px 10px;
  border-radius: 6px;
  font-weight: bold;
  font-size: 13px;
  margin: 0;
}

.booking-dates {
  display: flex;
  gap: 10px;
  margin: 20px 0;
}

.dates-section, .guests-section {
  flex: 1;
}

.dates-section h4, .guests-section h4 {
  font-size: 14px;
  margin-bottom: 8px;
  margin-top: 0;
  font-weight: normal;
  color: #555;
}

.date-picker, .guests-picker {
  border: 1px solid #ddd;
  padding: 12px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 14px;
  background-color: #fff;
  cursor: pointer;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
}

.date-picker i, .guests-picker i {
  color: #666;
  font-size: 16px;
}

.booking-conditions {
  margin: 20px 0;
  font-size: 14px;
  background-color: #f6fbf9;
  border-radius: 6px;
  padding: 15px;
}

.condition-badge {
  display: flex;
  align-items: center;
  gap: 8px;
  font-weight: 600;
  margin-bottom: 5px;
}

.condition-details {
  margin: 5px 0;
  padding-left: 25px;
  color: #555;
}

.more-info {
  color: #0066cc;
  text-decoration: none;
  display: block;
  margin-top: 5px;
  padding-left: 25px;
  font-weight: 500;
}

.green-icon {
  color: #00a698;
  font-size: 16px;
}

.green-text {
  color: #00a698;
  font-weight: bold;
  display: flex;
  align-items: center;
  gap: 8px;
}

.price-highlight {
  margin: 15px 0;
}

.price-highlight p {
  margin: 0;
}

.savings {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 15px 0;
  font-size: 14px;
}

.savings-text {
  color: #333;
}

.discount-percentage {
  color: #00a698;
  font-weight: bold;
  padding: 3px 8px;
  background-color: #e6f9ef;
  border-radius: 4px;
}

.divider-line {
  border: none;
  border-top: 1px solid #eee;
  margin: 20px 0;
}

.total-price {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 1px 0;
}

.price-label {
  font-size: 16px;
  font-weight: bold;
}

.price-value {
  text-align: right;
}

.original-price {
  text-decoration: line-through;
  color: #999;
  font-size: 14px;
  margin: 0;
}

.final-price {
  font-size: 22px;
  font-weight: bold;
  margin: 0;
  color: #333;
}

.tax-note {
  font-size: 12px;
  color: #999;
  margin: 0;
}

.book-button {
  background-color: #ff4b7d;
  color: white;
  border: none;
  border-radius: 6px;
  padding: 14px;
  width: 100%;
  font-weight: bold;
  cursor: pointer;
  margin: 20px 0 1px 0;
  font-size: 16px;
  box-shadow: 0 2px 4px rgba(255, 75, 125, 0.2);
}

.alternative-actions {
  text-align: center;
  margin: 15px 0 20px 0;
}

.divider-text {
  color: #999;
  margin: 0 0 15px 0;
  text-align: center;
  font-size: 14px;
}

.gift-button {
  background: #fff;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 12px;
  width: 100%;
  cursor: pointer;
  font-size: 14px;
  color: #333;
}

.price-guarantee {
  background-color: #eef8ff;
  border: 1px solid #d5e8ff;
  border-radius: 6px;
  padding: 12px;
  margin-top: 5px;
  font-size: 14px;
  display: flex;
  align-items: flex-start;
  gap: 10px;
}

.price-guarantee i {
  color: #0095ff;
  font-size: 16px;
  margin-top: 2px;
}

.price-guarantee p {
  margin: 0;
  line-height: 1.4;
}
</style> 