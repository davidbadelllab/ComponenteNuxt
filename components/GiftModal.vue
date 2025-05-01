<template>
  <Teleport to="body">
    <div v-if="isOpen" class="modal-container">
      <div class="modal-backdrop" @click="closeModal"></div>
      <transition name="modal-slide">
        <div v-if="isOpen" class="modal-content">
          <div class="modal-header">
            <h2>Personaliza tu regalo</h2>
            <button class="close-button" @click="closeModal">
              <i class="fas fa-times"></i>
            </button>
          </div>
          
          <div class="modal-body">
            <div class="gift-options">
              <div class="gift-option">
                <i class="fas fa-calendar-check"></i>
                <span>Elige la estancia y la duración</span>
              </div>
              <div class="gift-option">
                <i class="fas fa-mobile-alt"></i>
                <span>Recíbelo en versión digital o física</span>
              </div>
              <div class="gift-option">
                <i class="far fa-calendar"></i>
                <span>Deja que el beneficiario elija las fechas</span>
              </div>
              <div class="gift-option">
                <i class="fas fa-gift"></i>
                <span>Regalo válido por 1 año, para 2 personas</span>
              </div>
              <div class="gift-option">
                <i class="fas fa-exchange-alt"></i>
                <span>Canjeable por otra estancia.*</span>
              </div>
            </div>
            
            <div class="duration-section">
              <h3>Duración de la estancia</h3>
              <div class="duration-options">
                <div 
                  class="duration-option" 
                  :class="{ selected: selectedDuration === 1 }"
                  @click="selectDuration(1)"
                >
                  <div class="option-content">
                    <span>1 noche</span>
                    <span class="price">75 €</span>
                  </div>
                </div>
                <div 
                  class="duration-option" 
                  :class="{ selected: selectedDuration === 2 }"
                  @click="selectDuration(2)"
                >
                  <div class="option-content">
                    <span>2 noches</span>
                    <span class="price">150 €</span>
                  </div>
                </div>
                <div 
                  class="duration-option" 
                  :class="{ selected: selectedDuration === 3 }"
                  @click="selectDuration(3)"
                >
                  <div class="option-content">
                    <span>3 noches</span>
                    <span class="price">225 €</span>
                  </div>
                </div>
              </div>
            </div>
            
            <div class="format-section">
              <h3>Elige el formato</h3>
              <div class="format-options">
                <div 
                  class="format-option" 
                  :class="{ selected: selectedFormat === 'digital' }"
                  @click="selectFormat('digital')"
                >
                  <div class="format-header">
                    <div class="format-icon">
                      <img src="/img/iconvoucher_optim.webp" alt="Digital" />
                    </div>
                    <div class="format-title">
                      <h4>Formato digital</h4>
                      <p>Recepción por e-mail inmediata</p>
                    </div>
                    <span class="eco-label">Ecológico</span>
                  </div>
                </div>
                <div 
                  class="format-option" 
                  :class="{ selected: selectedFormat === 'physical' }"
                  @click="selectFormat('physical')"
                >
                  <div class="format-header">
                    <div class="format-icon">
                      <img src="/img/icongiftbox_optim.webp" alt="Físico" />
                    </div>
                    <div class="format-title">
                      <h4>Formato físico</h4>
                      <p>Entrega en 2-3 días laborables</p>
                    </div>
                    <span class="extra-fee">+4,99 €</span>
                  </div>
                </div>
              </div>
            </div>
            
            <div class="recipient-section">
              <div class="input-row">
                <div class="input-group">
                  <label>De parte de (opcional)</label>
                  <input type="text" placeholder="Tu nombre" />
                </div>
                <div class="input-group">
                  <label>Para (opcional)</label>
                  <input type="text" placeholder="Nombre del destinatario" />
                </div>
              </div>
              <div class="input-group full">
                <label>Tu mensaje (opcional)</label>
                <textarea placeholder="Escribe un mensaje personalizado" rows="3"></textarea>
                <div class="char-count">Máx. 180 caracteres</div>
              </div>
            </div>
            
            <div class="price-summary">
              <div class="price-tag">
                <span class="discount">Hasta -43%</span>
              </div>
              
              <!-- Digital format display -->
              <div v-if="selectedFormat === 'digital'" class="total-section">
                <div class="total-label">Importe total</div>
                <div class="total-amount">
                  <div class="final-price">{{ basePrice }} €</div>
                  <div class="tax-note">IVA incl.</div>
                </div>
              </div>
              
              <!-- Physical format displa -->
              <div v-else class="physical-price-breakdown">
                <div class="price-row">
                  <div class="price-label">Precio Weekendesk</div>
                  <div class="price-value">{{ basePrice }} € IVA incl.</div>
                </div>
                <div class="price-row shipping">
                  <div class="price-label">Gastos de envío</div>
                  <div class="price-value">+4,99 €</div>
                </div>
                <div class="price-row final">
                  <div class="price-label">Precio final</div>
                  <div class="price-value final">{{ totalPrice }} €</div>
                </div>
              </div>
              
              <button class="gift-button">Regalar sin fechas</button>
            </div>
          </div>
        </div>
      </transition>
    </div>
  </Teleport>
</template>

<script setup>
import { ref, computed, defineProps, defineEmits } from 'vue';

const props = defineProps({
  isOpen: {
    type: Boolean,
    default: false
  }
});

const emit = defineEmits(['close']);

// Estado para duración y formato
const selectedDuration = ref(2); // Por defecto, 2 noches
const selectedFormat = ref('digital'); // Por defecto, formato digital

// Precios base según duración
const prices = {
  1: 75,
  2: 150,
  3: 225
};

// Precio base calculado según la duración seleccionada
const basePrice = computed(() => {
  return prices[selectedDuration.value];
});

// Precio total calculado (incluye gastos de envío si es formato físico)
const totalPrice = computed(() => {
  if (selectedFormat.value === 'physical') {
    return basePrice.value + 4.99;
  }
  return basePrice.value;
});

// Métodos para seleccionar duración y formato
const selectDuration = (duration) => {
  selectedDuration.value = duration;
};

const selectFormat = (format) => {
  selectedFormat.value = format;
};

const closeModal = () => {
  emit('close');
};
</script>

<style scoped>
.modal-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-start;
  justify-content: flex-end;
  z-index: 1000;
}

.modal-backdrop {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
  z-index: 1001;
  cursor: pointer;
  animation: fade-in 0.2s ease;
}

@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.modal-content {
  position: relative;
  background-color: white;
  width: 500px;
  height: 100vh; 
  z-index: 1002;
  box-shadow: -2px 0 10px rgba(0, 0, 0, 0.2);
  padding: 0;
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  border-bottom: 1px solid #eee;
}

.modal-header h2 {
  margin: 0;
  font-size: 20px;
  font-weight: 500;
  color: #333;
}

.close-button {
  background: none;
  border: none;
  font-size: 20px;
  cursor: pointer;
  color: #666;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 30px;
  height: 30px;
}

.modal-body {
  padding: 15px 30px;
  flex: 1;
  overflow-y: auto;
}

.gift-options {
  margin-bottom: 20px;
}

.gift-option {
  display: flex;
  align-items: center;
  gap: 15px;
  margin-bottom: 12px;
  font-size: 14px;
  color: #333;
}

.gift-option i {
  width: 24px;
  color: #666;
  font-size: 16px;
  text-align: center;
}

.duration-section, .format-section, .recipient-section {
  margin-bottom: 20px;
}

.duration-section h3, .format-section h3 {
  font-size: 15px;
  margin-bottom: 12px;
  font-weight: 500;
  color: #333;
}

.duration-options {
  display: flex;
  gap: 10px;
}

.duration-option {
  flex: 1;
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 12px 8px;
  cursor: pointer;
  text-align: center;
  background-color: #fff;
  transition: all 0.2s ease;
}

.duration-option.selected {
  border: 1px solid #00a698;
  background-color: #f0f7f6;
}

.option-content {
  display: flex;
  flex-direction: column;
  font-size: 14px;
}

.price {
  font-weight: bold;
  margin-top: 2px;
  font-size: 15px;
}

.format-options {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.format-option {
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 12px;
  cursor: pointer;
  transition: all 0.2s ease;
  background-color: #fff;
}

.format-option.selected {
  border: 1px solid #00a698;
  background-color: #f0f7f6;
}

.format-header {
  display: flex;
  align-items: center;
  gap: 12px;
}

.format-icon {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.format-icon img {
  width: 30px;
  height: 30px;
  object-fit: contain;
}

.format-title {
  flex: 1;
}

.format-title h4 {
  margin: 0 0 3px 0;
  font-size: 14px;
  font-weight: 500;
  color: #333;
}

.format-title p {
  margin: 0;
  font-size: 12px;
  color: #666;
}

.eco-label {
  color: #00a698;
  font-size: 12px;
  font-weight: 500;
  padding: 2px 5px;
}

.extra-fee {
  color: #333;
  font-size: 13px;
  font-weight: 500;
}

.input-row {
  display: flex;
  gap: 12px;
  margin-bottom: 15px;
}

.input-group {
  flex: 1;
}

.input-group.full {
  width: 100%;
}

.input-group label {
  display: block;
  margin-bottom: 6px;
  font-size: 14px;
  color: #444;
  font-weight: 400;
}

.input-group input, .input-group textarea {
  width: 100%;
  padding: 8px 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 14px;
  background-color: #fff;
}

.input-group textarea {
  resize: none;
  height: 80px;
}

.char-count {
  text-align: right;
  font-size: 12px;
  color: #888;
  margin-top: 4px;
}

.price-summary {
  margin: 15px 0;
}

.price-tag {
  text-align: right;
  margin-bottom: 10px;
}

.discount {
  display: inline-block;
  padding: 3px 8px;
  background-color: #f0f7f6;
  color: #00a698;
  font-weight: 500;
  font-size: 13px;
  border-radius: 4px;
}

.total-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 0;
  border-top: 1px solid #eee;
  border-bottom: 1px solid #eee;
}

.total-label {
  font-weight: bold;
  font-size: 16px;
  color: #333;
}

.total-amount {
  text-align: right;
}

.final-price {
  font-size: 20px;
  font-weight: bold;
  color: #333;
}

.tax-note {
  font-size: 12px;
  color: #888;
}

/* Physical price breakdown */
.physical-price-breakdown {
  margin: 10px 0;
}

.price-row {
  display: flex;
  justify-content: space-between;
  padding: 6px 0;
  font-size: 14px;
}

.price-row.shipping {
  border-bottom: 1px solid #eee;
  padding-bottom: 10px;
}

.price-row.final {
  padding-top: 10px;
}

.price-value {
  font-weight: 500;
}

.price-value.final {
  font-size: 18px;
  font-weight: bold;
}

.gift-button {
  background-color: #ff4b7d;
  color: white;
  border: none;
  border-radius: 4px;
  padding: 12px;
  width: 100%;
  font-weight: 600;
  cursor: pointer;
  font-size: 16px;
  margin-top: 15px;
  box-shadow: 0 2px 4px rgba(255, 75, 125, 0.2);
}


.modal-slide-enter-active,
.modal-slide-leave-active {
  transition: all 0.3s ease;
}

.modal-slide-enter-from {
  transform: translateX(100%);
  opacity: 0;
}

.modal-slide-leave-to {
  transform: translateX(100%);
  opacity: 0;
}
</style> 