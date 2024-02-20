# HW-06-BarberShop

для оптимізації - https://compressjpeg.com/uk/
сайт для перевірки який тег в який можна вкладувати https://caninclude.glitch.me/
Макет https://www.figma.com/file/ihQm575H6pMX77FeD4F7ZD/Barbershop_v1-(Copy)?node-id=1%3A2
Макет українською https://www.figma.com/file/9pLSj3RwLdkVRShYgfUzPv/Barbershop_v1-(Ukrainian)?node-id=0%3A1
https://github.com/riko1212/fe-56-on/tree/mod-1 нагадую, що за кодом треба йти на гілку mod-1
Посилання YouTube: https://youtu.be/8AM-AbdEKe8 (запис YouTube в режимі обробки)

flaexbox - 3

Відкриття/закриття модального вікна
Модальне вікно з формою заявки відкривається по натисканню на кнопку "Замовити послугу". Для того щоб скрипт спрацював, необхідно додати до розмітки спеціальні атрибути, за якими скрипт шукає елементи:

data-modal-open - на кнопку відкриття модального вікна.
data-modal-close - на кнопку закриття модального вікна.
data-modal - на бекдроп модального вікна.

Після чого, перед закриваючим тегом body додати тег script з посиланням на файл скрипту для модально вікна. Можна подивитися відео-інструкцію.

<body>
  <!-- Вся твоя розмітка, включно з розміткою модалки -->

  <!-- Ставимо перед закриваючим тегом body -->
  <script src="./js/modal.js"></script>
</body>

Скрипт, який необхідно скопіювати і вставити у файл modal.js.

(() => {
const refs = {
openModalBtn: document.querySelector("[data-modal-open]"),
closeModalBtn: document.querySelector("[data-modal-close]"),
modal: document.querySelector("[data-modal]"),
};

refs.openModalBtn.addEventListener("click", toggleModal);
refs.closeModalBtn.addEventListener("click", toggleModal);

function toggleModal() {
refs.modal.classList.toggle("is-hidden");
}
})();
