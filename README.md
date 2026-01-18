# Dictum Releases

**Dictum** — умный ввод текста с ИИ для macOS.

Голосовая диктовка (Deepgram/локальная модель), AI-обработка текста (Gemini), сниппеты, скриншоты.

## 📥 Скачать

[![Последняя версия](https://img.shields.io/github/v/release/wellwon/dictum-releases?label=Версия&color=1AAF87)](https://github.com/wellwon/dictum-releases/releases/latest)

**[⬇️ Скачать последнюю версию](https://github.com/wellwon/dictum-releases/releases/latest)**

### Системные требования

- macOS 14.0 (Sonoma) или новее
- Apple Silicon или Intel Mac

## 🔄 Автоматические обновления

Dictum поддерживает автоматическую проверку обновлений. При запуске приложение проверяет наличие новых версий и предлагает обновиться.

### Feed URL для Sparkle-совместимых клиентов

```
https://raw.githubusercontent.com/wellwon/dictum-releases/main/appcast.xml
```

## 📋 История версий

См. [CHANGELOG.md](CHANGELOG.md) для полной истории изменений.

## 🔐 Проверка подписи

Dictum подписан самоподписанным сертификатом "Dictum Development". При первом запуске macOS может запросить подтверждение.

```bash
# Проверить подпись
codesign -dv --verbose=4 /Applications/Dictum.app
```

## 📞 Поддержка

Если у вас возникли проблемы:
1. Проверьте [известные проблемы](https://github.com/wellwon/dictum-releases/issues)
2. Создайте [новый issue](https://github.com/wellwon/dictum-releases/issues/new)

---

© 2024-2026 Dictum. Умный ввод с ИИ.
