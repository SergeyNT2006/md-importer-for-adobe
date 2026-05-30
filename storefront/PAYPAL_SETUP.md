# PayPal — настройка кнопки $25

Страница продаж: `storefront/index.html` → GitHub Pages  
URL: **https://sergeynt2006.github.io/md-importer-for-adobe/**

Репозиторий: [github.com/SergeyNT2006/md-importer-for-adobe](https://github.com/SergeyNT2006/md-importer-for-adobe)

---

## 1. PayPal Business

1. Войдите в [PayPal Business](https://www.paypal.com/business).
2. Убедитесь, что аккаунт принимает платежи в **USD**.
3. Запомните **email**, привязанный к бизнес-аккаунту (не обязательно совпадает с личной почтой).

---

## 2. Подставить email в форму

В файле `storefront/index.html` найдите:

```html
<input type="hidden" name="business" value="PAYPAL_BUSINESS_EMAIL">
```

Замените `PAYPAL_BUSINESS_EMAIL` на ваш PayPal business email (в проекте: **lgphonemar24@gmail.com**).

```html
<input type="hidden" name="business" value="lgphonemar24@gmail.com">
```

Сохраните, закоммитьте и запушьте — Pages обновится через 1–2 минуты.

---

## 3. Альтернатива: Hosted Button (надёжнее)

1. PayPal → **Pay & Get Paid** → **Create Buttons** → **Buy Now**.
2. Название: `MD Importer Full License`, цена **25.00 USD**.
3. Скопируйте HTML-код кнопки.
4. Вставьте вместо блока `<form class="paypal-form">...</form>` в `docs/index.html`.

---

## 4. PayPal.me (простой вариант)

Если не нужна форма на сайте, добавьте ссылку:

```text
https://www.paypal.me/YOUR_USERNAME/25USD
```

В `docs/index.html` рядом с кнопкой:

```html
<p><a href="https://www.paypal.me/YOUR_USERNAME/25USD">Pay $25 via PayPal.me</a></p>
```

---

## 5. После оплаты (выдача полной версии)

Рекомендуемый процесс:

1. Покупатель платит $25.
2. PayPal присылает вам уведомление на email.
3. Вы отправляете на email покупателя:
   - `MD-Importer-Full-1.6.0.zxp` (или ссылку на приватный Google Drive / Dropbox)
   - краткую инструкцию по установке из `manual.md`
4. Страница `docs/thanks.html` — «спасибо, проверьте почту».

Опционально позже: **IPN / Webhooks** PayPal для автоматической отправки ссылки (отдельная задача).

---

## 6. Return URL

В форме уже указано:

- **return** → `thanks.html` (страница «спасибо»)
- **cancel_return** → главная страница

Проверьте в настройках PayPal, что разрешены return URL для вашего домена `sergeynt2006.github.io`.
