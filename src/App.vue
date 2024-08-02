<template>
  <ion-header>
    <ion-toolbar>
      <ion-buttons slot="start">
        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="20" height="20" viewBox="0 0 256 256" xml:space="preserve">
          <g style="stroke: none; stroke-width: 0; stroke-dasharray: none; stroke-linecap: butt; stroke-linejoin: miter; stroke-miterlimit: 10; fill: none; fill-rule: nonzero; opacity: 1;" transform="translate(1.4065934065934016 1.4065934065934016) scale(2.81 2.81)" >
            <path d="M 65.75 90 c 0.896 0 1.792 -0.342 2.475 -1.025 c 1.367 -1.366 1.367 -3.583 0 -4.949 L 29.2 45 L 68.225 5.975 c 1.367 -1.367 1.367 -3.583 0 -4.95 c -1.367 -1.366 -3.583 -1.366 -4.95 0 l -41.5 41.5 c -1.367 1.366 -1.367 3.583 0 4.949 l 41.5 41.5 C 63.958 89.658 64.854 90 65.75 90 z" style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-linejoin: miter; stroke-miterlimit: 10; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;" transform=" matrix(1 0 0 1 0 0) " stroke-linecap="round" />
          </g>
        </svg>
      </ion-buttons>
      <ion-title>Удостоверение личности</ion-title>
    </ion-toolbar>
  </ion-header>

  <div class="content">
    <ion-segment value="default" class="custom-segment">
      <ion-segment-button value="default">
        <ion-label>Документ</ion-label>
      </ion-segment-button>
      <ion-segment-button value="segment">
        <ion-label>Реквизиты</ion-label>
      </ion-segment-button>
    </ion-segment>

    <div class="image-container">
      <img src="../img/udos.jpg" alt="Фотография" />
    </div>
    <div class="divider"></div>
    <div class="button-container">
      <button id="show">
        Предъявить документ
      </button>
      <button id="send">
        Отправить документ
      </button>
    </div>
  </div>
</template>

<script lang="ts">
/*import { ref } from 'vue';
import { IonHeader, IonToolbar, IonButtons,  IonTitle, IonSegment, IonSegmentButton, IonButton, IonLabel } from '@ionic/vue';

const selectedSegment = ref('documents');*/
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  // Ваши компоненты, данные и методы
});
</script>

<style>
.icon{
  position: relative;
}

.button-container {
  display: flex;
  flex-direction: column;
  align-items: center; /* Центрирует кнопки по горизонтали */
  gap: 10px; /* Отступ между кнопками */
}

button {
  width: 92%;
  margin: 0 auto;
  color: white; /* Цвет текста кнопок */
  border-radius: 12px; /* Закругление углов кнопок */
  padding: 0;
  height: 50px;
  margin-bottom: -10px;
  font-size: 15px;
}

/* Закругление нижних углов у кнопок */
button#show {
  position: relative;
  border-radius: 12px;
  width: 96%;
  background-color: rgb(44, 91, 192);
  font-weight: bold;
  bottom: 6px;
}

button#send {
  border-radius: 12px;
  width: 96%;
  border-color: rgb(44, 91, 192);
  background-color: white;
  color: rgb(44, 91, 192);
  border-width: 2px;
  border-style: solid;
  font-weight: bold;
  height: 50px;
}

/* Стили для разделителя */
.divider {
  position: relative;
  bottom: 10px;
  width: 100%; /* Ширина на всю страницу */
  height: 1px; /* Высота разделителя */
  background-color: #ccc; /* Цвет разделителя */
  margin-bottom: 10px; /* Отступ снизу */
}

body {
  background-color: white !important;
}

ion-header {
  --background: white !important; /* Белый фон для заголовка */
  box-shadow: none !important;
  border: none;
}

ion-toolbar {
  --background: white !important; /* Белый фон для панели инструментов */
  box-shadow: none !important;
  --border-style: none;
}

ion-segment {
  margin: 3px auto;
  width: 96%;
  background-color: rgb(235, 235, 235);
  color: black;
}

/* Белый фон для ion-segment-button */
ion-segment-button {
  --indicator-color: white; /* Убираем цвет индикатора */
}

ion-segment-button ion-label {
  font-weight: 600;
}

ion-title {
  color: black !important; /* Черный цвет текста заголовка */
  text-align: center;
  font-size: 16px;
  font-weight: bold;
}

.content {
  background: white;
}

.image-container {
  width: 90%; /* Контейнер изображения занимает всю ширину */
  margin: 0 auto;
  padding: 65px 0 160px 0px;
}

.image-container img {
  width: 100%; /* Изображение занимает всю ширину контейнера */
  height: auto; /* Высота автоматически подстраивается в зависимости от ширины */
}

</style>
