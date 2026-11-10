[![Telegram](https://img.shields.io/badge/Telegram-@fan__world__me-2CA5E0?style=flat-square&logo=telegram)](https://t.me/fan_world_me)   [![Discord](https://img.shields.io/badge/Discord-fan__world__me-5865F2?style=flat-square&logo=discord)](https://discord.com/users/1040301536036786248)   [![GitHub](https://img.shields.io/badge/GitHub-fan--world--me-181717?style=flat-square&logo=github)](https://github.com/fan-world-me)   [![Portfolio](https://img.shields.io/badge/Portfolio-fan--world--me.github.io-00e5ff?style=flat-square&logo=githubpages&logoColor=white)](https://fan-world-me.github.io/)

# AES-256-GCM

Веб-интерфейс для просмотра зашифрованных заметок.  
Шифрование: **AES-256-GCM** + деривация ключа **Argon2id**.

---

### 🧰 Tech Stack

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![AES-256-GCM](https://img.shields.io/badge/AES--256--GCM-encryption-00e5ff?style=flat-square)
![Argon2id](https://img.shields.io/badge/Argon2id-KDF-6B21A8?style=flat-square)

---

### 🔐 Параметры шифрования

> Нужны параметры Argon2id (`time_cost` / `memory_cost` / `parallelism`) + структура блоба:
> `salt (16)` + `IV (12)` + `ciphertext` + `tag (16)` для AES-256-GCM

**Argon2id (деривация ключа)**

| Параметр | Описание |
|---|---|
| `time_cost` | Число итераций (рекомендуется ≥ 3) |
| `memory_cost` | Объём памяти в KiB (рекомендуется ≥ 65536) |
| `parallelism` | Число параллельных потоков (рекомендуется ≥ 1) |

**Структура блоба (бинарный формат)**

```
[ salt (16 байт) ][ IV (12 байт) ][ ciphertext ][ tag (16 байт) ]
```

| Поле | Размер | Описание |
|---|---|---|
| `salt` | 16 байт | Случайная соль для Argon2id |
| `IV` (nonce) | 12 байт | Случайный IV для AES-256-GCM |
| `ciphertext` | переменный | Зашифрованные данные |
| `tag` | 16 байт | Тег аутентификации GCM |

> Весь блоб кодируется в **Base64** перед сохранением.

---

### 🚀 Использование

Открыть `index.html` в браузере — никаких зависимостей, чистый HTML/CSS/JS.

---

### 📄 Лицензия

[GPL-3.0](./LICENSE) © [fan-world-me](https://github.com/fan-world-me)

---

Made with 🩵 in Ukraine 🇺🇦

[![Telegram](https://img.shields.io/badge/Telegram-@fan__world__me-2CA5E0?style=flat-square&logo=telegram)](https://t.me/fan_world_me)   [![Discord](https://img.shields.io/badge/Discord-fan__world__me-5865F2?style=flat-square&logo=discord)](https://discord.com/users/1040301536036786248)   [![Portfolio](https://img.shields.io/badge/Portfolio-fan--world--me.github.io-00e5ff?style=flat-square&logo=githubpages&logoColor=white)](https://fan-world-me.github.io/)
