<div align="center">

# 🤖 Local AI

**Мультимодальный ИИ-ассистент, работающий полностью в браузере.**

60+ языковых и мультимодальных моделей. Без серверов. Без API-ключей. Без регистрации.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![WebGPU](https://img.shields.io/badge/WebGPU-supported-green)](https://caniuse.com/webgpu)
[![Transformers.js](https://img.shields.io/badge/🤗_Transformers.js-ready-orange)](https://huggingface.co/docs/transformers.js)
[![WebLLM](https://img.shields.io/badge/⚡_WebLLM-powered-blue)](https://webllm.mlc.ai/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/SawerSwet/AI-local-/pulls)

</div>

---

## 📖 О проекте

**Local AI** — полноценный мультимодальный ИИ-ассистент, работающий **полностью в вашем браузере**. Никаких серверов, никаких API-ключей, никакой отправки данных в облако. Всё вычисляется локально на вашем устройстве через **WebGPU** и **WebAssembly**.

Один HTML-файл — и у вас в руках:

- 💬 **Чат** с 60+ языковыми моделями (Llama, Qwen, Gemma, Phi, Mistral, DeepSeek)
- 🖼 **Работа с изображениями**: OCR, описание, ответы на вопросы, детекция объектов
- 📄 **Чтение документов**: PDF, DOCX, TXT, MD, JSON, CSV, ZIP, исходный код
- 📤 **Экспорт результатов**: TXT, Markdown, HTML, JSON, CSV, PDF (с кириллицей), ZIP
- 🧠 **10 режимов рассуждения**: от простого диалога до Chain-of-Thought и Сократа
- 🎨 **Мобильный UI** с нижней навигацией
- 🔒 **Полная приватность**: данные не покидают устройство

---

## ✨ Возможности

### 💬 Чат

| Возможность | Описание |
|-------------|----------|
| Стриминг | Ответ приходит токен за токеном |
| История | До 120 сообщений, автосохранение |
| Системный промпт | Настраивается под задачу |
| Быстрые промпты | 12 шаблонов в один клик |
| Озвучка | Web Speech API |
| Стоп-генерация | Прервать на любом этапе |
| Регенерация | Перегенерировать последний ответ |
| Markdown-рендер | Код, списки, таблицы, формулы |

### 🧠 Режимы рассуждения

| Режим | Что делает |
|-------|-----------|
| 💬 Обычный | Прямой ответ |
| 🧠 Пошагово (CoT) | План → шаги → итог |
| ❓ Сократ | Наводящие вопросы |
| 💡 Брейншторм | Много идей, группировка |
| 🔍 Критика | Ответ + самокритика |
| 🎓 Эксперт | Точно, с принципами |
| 👶 Простыми словами | Как пятилетнему |
| 📌 Резюме | Кратко + детали |
| 🎨 Творческий | Метафоры, стиль |
| 🌐 Переводчик | Точный перевод |

### 🖼 Изображения

- **OCR** — распознавание текста (RU + EN) через Tesseract.js
- **Captioning** — описание содержимого (BLIP, ViT-GPT2)
- **VQA** — вопросы по картинке (BLIP VQA)
- **Детекция объектов** — DETR ResNet-50
- **Сегментация** — SegFormer B0
- **Глубина** — Depth Anything Small
- **Классификация** — ViT Base
- **Zero-shot** — CLIP ViT-B/32

### 📄 Документы

| Формат | Метод |
|--------|-------|
| PDF | pdf.js (до 30 страниц) |
| DOCX | JSZip + парсинг XML |
| ZIP | Чтение всех текстов внутри |
| TXT, MD, CSV, JSON | Прямое чтение |
| Код | JS, TS, PY, Java, C++, Go, Rust, PHP, SQL |
| Изображения | OCR |

### 📤 Экспорт

- **TXT** — простой текст
- **Markdown** — с форматированием
- **HTML** — автономный стилизованный файл
- **JSON** — структурированные данные
- **CSV** — для Excel
- **PDF** — с кириллицей через canvas
- **ZIP** — чат + вложения

### 🛠 Инструменты

- **Редактор документов** — TXT, MD, JSON, PDF
- **Таблица → CSV** — конвертер
- **Перевод** — RU↔EN через Opus-MT
- **ZIP-упаковщик**
- **Диагностика** — WebGPU, WebGL, WASM
- **Тест WebGPU**

---

## 🚀 Быстрый старт

### Способ 1: Локально

```bash
git clone https://github.com/SawerSwet/AI-local-.git
cd AI-local-
python -m http.server 8000
# Открой http://localhost:8000
```

> ⚠️ ES-модули не работают через `file://`. Нужен локальный сервер.

### Способ 2: Node.js

```bash
npx serve
```

### Способ 3: GitHub Pages

Открой готовую версию прямо сейчас:

**https://sawerswet.github.io/AI-local-/**

Если Pages ещё не включены:

1. **Settings → Pages**
2. **Source:** `Deploy from a branch`
3. **Branch:** `main` / `root`
4. Сохрани — через минуту сайт будет доступен

---

## 🌐 Требования

| Браузер | Минимум | Рекомендуется |
|---------|---------|---------------|
| Chrome | 113+ | 120+ |
| Edge | 113+ | 120+ |
| Opera | 99+ | 105+ |
| Safari | 17.4+ | 18+ |
| Firefox | ⚠️ Без WebGPU | Ограниченно |

**Что нужно:**

- ✅ **WebGPU** — для WebLLM-моделей
- ✅ **WebAssembly** — для Transformers.js
- ✅ **≥4 ГБ ОЗУ** — для моделей 1B
- ✅ **≥16 ГБ ОЗУ** — для моделей 7-8B
- ✅ **Интернет** — только при первой загрузке модели

> 💡 **Без WebGPU** работают WASM-модели до 1.5B (в 5-10 раз медленнее).

---

## 🧠 Каталог моделей (~60)

### ⚡ WebLLM (WebGPU)

| Модель | Размер | Языки | Особенности |
|--------|--------|-------|-------------|
| SmolLM2 360M | 230 МБ | EN | Самая лёгкая |
| Qwen2.5 0.5B | 350 МБ | RU, EN, ZH | Знает русский |
| TinyLlama 1.1B | 700 МБ | EN | Компактная |
| Llama 3.2 1B | 1.0 ГБ | RU, EN | Баланс |
| Qwen2.5 1.5B | 900 МБ | RU, EN, ZH | Хорош для RU |
| Qwen2.5 Coder 1.5B | 900 МБ | EN, Code | Программирование |
| Qwen2.5 Math 1.5B | 900 МБ | EN, Math | Математика |
| Gemma 2 2B | 1.4 ГБ | EN, RU | Google |
| Phi-3 mini 4K | 2.2 ГБ | RU, EN, Math | Microsoft |
| Phi-3.5 mini | 2.2 ГБ | RU, EN, Math, Code | Улучшенная |
| Llama 3.2 3B | 2.2 ГБ | RU, EN | Meta |
| Qwen2.5 3B | 1.8 ГБ | RU, EN, ZH, Code | Умеет код |
| DeepSeek R1 1.5B | 1.0 ГБ | EN, Math, Code | Рассуждения |
| Mistral 7B v0.3 | 4.2 ГБ | EN, RU, Code | Классика |
| Qwen2.5 7B | 4.2 ГБ | RU, EN, ZH, Code | **Топ для RU** |
| Qwen2.5 Coder 7B | 4.2 ГБ | EN, Code | **Топ для кода** |
| DeepSeek R1 7B | 4.4 ГБ | EN, Math, Code | Мощные рассуждения |
| Llama 3.1 8B | 4.5 ГБ | RU, EN | Meta |
| Hermes 2 Pro 8B | 4.5 ГБ | EN | Function calling |
| Gemma 2 9B | 5.4 ГБ | EN, RU | Google |
| OpenHermes 2.5 7B | 4.2 ГБ | EN | Инструкции |
| WizardLM 7B | 4.2 ГБ | EN | Диалоги |

### 🧪 Transformers.js

**Текст:**

- Qwen2.5 0.5B / 1.5B
- Llama 3.2 1B
- SmolLM2 360M
- Gemma 2 2B
- Phi 3.5 mini
- Flan-T5 Small / Base
- mT5 Small

**Перевод:**

- Opus MT RU→EN
- Opus MT EN→RU

**Vision / OCR:**

- TrOCR Small Printed
- TrOCR Base Handwritten
- Donut CORD-v2
- ViT Base
- CLIP ViT-B/32
- DETR ResNet-50
- SegFormer B0
- Depth Anything Small
- ViT-GPT2
- BLIP Caption Base
- BLIP VQA Base
- Florence-2 Base
- LayoutLMv3 Base
- Moondream2
- Whisper Tiny / Base / Small

**Embedding:**

- Nomic Embed v1.5
- All-MiniLM-L6-v2
- BGE Small EN v1.5

**Классификация:**

- DistilBERT SST-2

---

## 🛠 Технологии

| Слой | Технология |
|------|-----------|
| LLM (WebGPU) | WebLLM |
| ONNX-модели | Transformers.js |
| ML-фреймворк | TensorFlow.js |
| OCR | Tesseract.js |
| PDF-чтение | pdf.js |
| DOCX/ZIP | JSZip |
| PDF-экспорт | jsPDF |
| Markdown | marked |
| Формулы | KaTeX |
| UI | Vanilla JS + CSS |

---

## 📁 Структура

```
AI-local-/
├── index.html          # Всё приложение в одном файле
├── README.md           # Этот файл
├── LICENSE             # MIT
└── docs/
    ├── MODELS.md       # Каталог моделей
    ├── CONTRIBUTING.md # Гайд по контрибьютингу
    └── API.md          # Программный API
```

Весь код в одном HTML — осознанное решение:

- ✅ **Простота**: скопировал — работает
- ✅ **Портативность**: можно отправить в мессенджере
- ✅ **Хостинг**: GitHub Pages, Netlify, Vercel
- ✅ **Аудит**: никаких сборок и минификаций

---

## 🎯 Сценарии использования

### 🔒 Приватная работа с документами

Загрузите PDF-договор — модель найдёт нужное, резюмирует, объяснит. **Ни байта в облако.**

### 📱 Офлайн-ассистент

После первой загрузки модель кэшируется в браузере. Работает **без интернета**.

### 🎓 Обучение

Математика, код, физика. Режимы «Пошагово» и «Сократ» для разбора решений.

### 🖼 Работа с фото

Рукописный текст → OCR. Скриншот → VQA. Схема → описание.

### 📊 Конвертация

- PDF → TXT/MD
- DOCX → Markdown
- CSV → JSON
- Чат → PDF/ZIP

### 🌐 Переводчик

RU↔EN локально, без отправки текста на серверы.

---

## 🔐 Приватность

| Данные | Где хранятся | Кто видит |
|--------|--------------|-----------|
| История чата | localStorage | Только вы |
| Настройки | localStorage | Только вы |
| Модели | Cache API | Только вы |
| Вложения | Память вкладки | Только вы |
| Запросы | Локально | Только вы |
| Изображения | Локально | Только вы |

**Единственный сетевой запрос** — скачивание модели с HuggingFace CDN. После этого можно работать офлайн.

Никакой аналитики, трекеров, телеметрии.

---

## ⚡ Производительность

Llama 3.2 1B, WebGPU:

| Устройство | Скорость | Память |
|------------|----------|--------|
| MacBook Pro M3 | ~45 tok/s | 1.2 ГБ |
| MacBook Air M2 | ~35 tok/s | 1.2 ГБ |
| RTX 3060 | ~60 tok/s | 1.3 ГБ |
| RTX 4090 | ~120 tok/s | 1.5 ГБ |
| iPhone 15 Pro | ~25 tok/s | 1.4 ГБ |
| Pixel 8 | ~18 tok/s | 1.4 ГБ |
| Galaxy S23 | ~20 tok/s | 1.4 ГБ |

На WASM: **1-5 tok/s**.

---

## 🗺 Roadmap

- [x] Чат с 60+ моделями
- [x] WebGPU через WebLLM
- [x] Transformers.js
- [x] OCR (Tesseract.js)
- [x] PDF / DOCX / ZIP
- [x] Экспорт PDF / ZIP / CSV
- [x] 10 режимов рассуждения
- [x] Мобильный UI
- [ ] Многосессионный чат
- [ ] RAG по документам
- [ ] Голосовой ввод (Whisper)
- [ ] Mermaid-диаграммы
- [ ] Камера телефона → OCR
- [ ] PWA
- [ ] Anki-экспорт
- [ ] Браузерные плагины

---

## 🤝 Контрибьютинг

1. Форк
2. Ветка (`git checkout -b feature/amazing`)
3. Коммит (`git commit -m 'Add amazing'`)
4. Push (`git push origin feature/amazing`)
5. Pull Request

**Идеи для вклада:**

- Новые модели в массив `MODELS`
- UI/UX улучшения
- Новые режимы рассуждения
- Форматы ввода/вывода
- Переводы интерфейса
- Оптимизация памяти

Подробнее — [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md).

---

## 🐛 Известные ограничения

- **Firefox** — нет WebGPU
- **iOS Safari < 17.4** — частичная поддержка
- **PDF** — извлекается текст, не картинки
- **DOCX** — простой парсер (теряет таблицы/стили)
- **PDF-кириллица** — через canvas, файл больше
- **Модели 7B+** — нужен ПК с 16+ ГБ ОЗУ

---

## 📜 Лицензия

**MIT**. См. [LICENSE](LICENSE).

Свободно, включая коммерческое использование.

---

## 🙏 Благодарности

- [MLC AI](https://mlc.ai/) — WebLLM
- [HuggingFace](https://huggingface.co/) — Transformers.js и модели
- [Mozilla](https://mozilla.org/) — pdf.js
- [Tesseract.js](https://tesseract.projectnaptha.com/) — OCR
- [Stuk](https://stuk.github.io/jszip/) — JSZip
- [jsPDF](https://github.com/parallax/jsPDF) — экспорт PDF
- Все авторы моделей на HuggingFace

---

## 📊 Статистика

![Stars](https://img.shields.io/github/stars/SawerSwet/AI-local-?style=social)
![Forks](https://img.shields.io/github/forks/SawerSwet/AI-local-?style=social)
![Issues](https://img.shields.io/github/issues/SawerSwet/AI-local-)

---

## ⭐ Поддержать проект

- ⭐ Звезда на GitHub
- 🐛 Issue о баге
- 💡 Идея в Discussions
- 🔀 Pull Request
- 📢 Рассказать друзьям

---

## 📞 Контакты

- **Issues**: [github.com/SawerSwet/AI-local-/issues](https://github.com/SawerSwet/AI-local-/issues)
- **Discussions**: [github.com/SawerSwet/AI-local-/discussions](https://github.com/SawerSwet/AI-local-/discussions)
- **Live demo**: [sawerswet.github.io/AI-local-/](https://sawerswet.github.io/AI-local-/)

---

<div align="center">

**Сделано с ❤️ для тех, кто ценит приватность и локальные вычисления.**

_Ваш ИИ. Ваши данные. Ваше устройство._

</div>
