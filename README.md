# 🚀 Инструмент для сброса пробного периода Cursor

<div align="center">

[![Релиз](https://img.shields.io/github/v/release/yuaotian/go-cursor-help?style=flat-square&logo=github&color=blue)](https://github.com/yuaotian/go-cursor-help/releases/latest)
[![Лицензия](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square&logo=bookstack)](https://github.com/yuaotian/go-cursor-help/blob/master/LICENSE)
[![Звезды](https://img.shields.io/github/stars/yuaotian/go-cursor-help?style=flat-square&logo=github)](https://github.com/yuaotian/go-cursor-help/stargazers)

[🌟 English](README.md) | [🌏 中文](README_CN.md) | [🌏 日本語](README_JP.md)

<img src="https://ai-cursor.com/wp-content/uploads/2024/09/logo-cursor-ai-png.webp" alt="Логотип Cursor" width="120"/>

</div>

> ⚠️ **ВАЖНОЕ УВЕДОМЛЕНИЕ**
> 
> Этот инструмент поддерживает:
> - ✅ Windows: Последние версии 0.49.x (поддерживаются)
> - ✅ Mac/Linux: Последние версии 0.49.x (поддерживаются, приветствуется обратная связь)
>
> Перед использованием убедитесь, что ваша версия Cursor совместима с инструментом.

<details open>
<summary><b>📦 История версий и загрузки</b></summary>

<div class="version-card" style="background: linear-gradient(135deg, #6e8efb, #a777e3); border-radius: 8px; padding: 15px; margin: 10px 0; color: white;">

### 🌟 Последние версии

[Посмотреть полную историю версий](https://github.com/oslook/cursor-ai-downloads?tab=readme-ov-file)

</div>

</details>

⚠️ **Общие решения для Cursor**
> 1.  Закройте Cursor, выйдите из учетной записи и удалите её на официальном сайте (обновите IP-адрес: Япония, Сингапур, США, Гонконг, приоритет низкой задержке - не обязательно, но рекомендуется; для пользователей Windows рекомендуется очистить кэш DNS: `ipconfig /flushdns`)
> Перейдите на официальный сайт Cursor, чтобы удалить текущую учетную запись
> Шаги: Аватар пользователя -> Настройки -> Дополнительно▼ внизу слева -> Удалить учетную запись
>
> 2.  Запустите скрипт обновления кода машины, см. адрес скрипта ниже, доступен в Китае
> 
> 3.  Зарегистрируйте новую учетную запись, войдите в систему и откройте Cursor для продолжения использования.
>
> 4.  Альтернативное решение: Если после шага [**3**] Cursor все еще не работает, или если вы столкнулись с проблемами, такими как невозможность регистрации учетной записи или удаления учетной записи, это обычно означает, что ваш браузер был идентифицирован или ограничен целевым сайтом (контроль риска). В этом случае попробуйте сменить браузер, например: Edge, Google Chrome, Firefox. (Или рассмотрите возможность использования браузера, который может изменять или рандомизировать информацию о браузере).


---

⚠️ **Предупреждение о модификации MAC-адреса**
> 
> Для пользователей Mac: Этот скрипт включает функцию модификации MAC-адреса, которая:
> - Изменит MAC-адрес вашего сетевого интерфейса
> - Создаст резервную копию оригинальных MAC-адресов перед изменением
> - Это изменение может временно повлиять на сетевое подключение
> - Вы можете пропустить этот шаг при выполнении скрипта
>

<details >
<summary><b>🔒 Отключение функции автоматического обновления</b></summary>

> Чтобы предотвратить автоматическое обновление Cursor до неподдерживаемых новых версий, вы можете отключить функцию автоматического обновления.

#### Метод 1: Использование встроенного скрипта (рекомендуется)

При запуске инструмента сброса скрипт спросит, хотите ли вы отключить автоматическое обновление:
```text
[Вопрос] Хотите отключить функцию автоматического обновления Cursor?
0) Нет - Оставить настройки по умолчанию (нажмите Enter)
1) Да - Отключить автоматическое обновление
```

Выберите `1`, чтобы автоматически завершить операцию отключения.

#### Метод 2: Ручное отключение

**Windows:**
1. Закройте все процессы Cursor
2. Удалите каталог: `%LOCALAPPDATA%\cursor-updater`
3. Создайте файл с тем же именем (без расширения) в том же месте

**macOS:**
```bash
# ПРИМЕЧАНИЕ: По результатам тестирования, этот метод работает только для версии 0.45.11 и ниже.
# Закройте Cursor
pkill -f "Cursor"
# Замените app-update.yml пустым/только для чтения файлом
cd /Applications/Cursor.app/Contents/Resources
mv app-update.yml app-update.yml.bak
touch app-update.yml
chmod 444 app-update.yml

# Перейдите в Настройки -> Приложение -> Обновление, установите Режим в none.
# Это необходимо сделать, чтобы предотвратить проверку обновлений Cursor.

# ПРИМЕЧАНИЕ: Метод модификации cursor-updater может больше не быть эффективным
# В любом случае, удалите каталог обновлений и создайте блокирующий файл
rm -rf ~/Library/Application\ Support/Caches/cursor-updater
touch ~/Library/Application\ Support/Caches/cursor-updater
```

**Linux:**
```bash
# Закройте Cursor
pkill -f "Cursor"
# Удалите каталог обновлений и создайте блокирующий файл
rm -rf ~/.config/cursor-updater
touch ~/.config/cursor-updater
```

> ⚠️ **Примечание:** После отключения автоматических обновлений вам нужно будет вручную загружать и устанавливать новые версии. Рекомендуется обновляться только после подтверждения совместимости новой версии.


</details>

---

### 📝 Описание

> Когда вы сталкиваетесь с любым из этих сообщений:

#### Проблема 1: Лимит пробной учетной записи <p align="right"><a href="#issue1"><img src="https://img.shields.io/badge/Move%20to%20Solution-Blue?style=plastic" alt="Back To Top"></a></p>

```text
Слишком много использованных пробных учетных записей на этом устройстве.
Пожалуйста, обновитесь до Pro. Мы установили этот лимит
для предотвращения злоупотреблений. Пожалуйста, дайте нам знать, если вы считаете,
что это ошибка.
```

#### Проблема 2: Ограничение API-ключа <p align="right"><a href="#issue2"><img src="https://img.shields.io/badge/Move%20to%20Solution-green?style=plastic" alt="Back To Top"></a></p>

```text
[Новая проблема]

Composer полагается на пользовательские модели, которые не могут быть оплачены с помощью API-ключа.
Пожалуйста, отключите API-ключи и используйте подписку Pro или Business.
ID запроса: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

#### Проблема 3: Лимит запросов пробного периода

> Это указывает на то, что вы достигли лимита использования в течение VIP пробного периода:

```text
Вы достигли лимита запросов пробного периода.
```

#### Проблема 4: Высокая нагрузка Claude 3.7 <p align="right"><a href="#issue4"><img src="https://img.shields.io/badge/Move%20to%20Solution-purple?style=plastic" alt="Back To Top"></a></p>

```text
Высокая нагрузка 
В настоящее время мы испытываем высокий спрос на Claude 3.7 Sonnet. Пожалуйста, обновитесь до Pro или переключитесь на
'стандартную' модель, Claude 3.5 sonnet, другую модель или попробуйте снова через несколько минут.
```

<br>

<p id="issue2"></p>

#### Решение: Полное удаление Cursor и переустановка (проблема с API-ключом)

1. Загрузите [Geek.exe Uninstaller[Free]](https://geekuninstaller.com/download)
2. Полностью удалите приложение Cursor
3. Переустановите приложение Cursor
4. Продолжите к Решению 1

<br>

<p id="issue1"></p>

> Временное решение:

#### Решение 1: Быстрый сброс (рекомендуется)

1. Закройте приложение Cursor
2. Запустите скрипт сброса кода машины (см. инструкции по установке ниже)
3. Откройте Cursor снова для продолжения использования

#### Решение 2: Смена учетной записи

1. Файл -> Настройки Cursor -> Выйти
2. Закройте Cursor
3. Запустите скрипт сброса кода машины
4. Войдите с новой учетной записью

#### Решение 3: Оптимизация сети

Если вышеуказанные решения не работают, попробуйте:

- Переключитесь на узлы с низкой задержкой (рекомендуемые регионы: Япония, Сингапур, США, Гонконг)
- Обеспечьте стабильность сети
- Очистите кэш браузера и повторите попытку

#### Решение 4: Проблема доступа к Claude 3.7 (высокая нагрузка)

Если вы видите сообщение "Высокая нагрузка" для Claude 3.7 Sonnet, это указывает на то, что Cursor ограничивает использование модели 3.7 для пробных учетных записей в определенные часы дня. Попробуйте:

1. Переключитесь на новую учетную запись, созданную с помощью Gmail, возможно, подключившись через другой IP-адрес
2. Попробуйте получить доступ в непиковые часы (обычно с 5 до 10 утра или с 3 до 7 вечера, когда ограничения часто менее строгие)
3. Рассмотрите возможность обновления до Pro для гарантированного доступа
4. Используйте Claude 3.5 Sonnet в качестве резервного варианта

> Примечание: Эти шаблоны доступа могут изменяться по мере того, как Cursor корректирует свою политику распределения ресурсов.

### 💻 Поддержка систем

<table>
<tr>
<td>

**Windows** ✅

- x64 (64-бит)
- x86 (32-бит)

</td>
<td>

**macOS** ✅

- Intel (x64)
- Apple Silicon (M1/M2)

</td>
<td>

**Linux** ✅

- x64 (64-бит)
- x86 (32-бит)
- ARM64

</td>
</tr>
</table>

### 🚀 Решение в один клик

<details open>
<summary><b>Глобальные пользователи</b></summary>

**macOS**

```bash
# Метод два
curl -fsSL https://aizaozao.com/accelerate.php/https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_mac_id_modifier.sh -o ./cursor_mac_id_modifier.sh && sudo bash ./cursor_mac_id_modifier.sh && rm ./cursor_mac_id_modifier.sh
```

**Linux**

```bash
curl -fsSL https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_linux_id_modifier.sh | sudo bash 
```

> **Примечание для пользователей Linux:** Скрипт пытается найти вашу установку Cursor, проверяя общие пути (`/usr/bin`, `/usr/local/bin`, `$HOME/.local/bin`, `/opt/cursor`, `/snap/bin`), используя команду `which cursor` и выполняя поиск в `/usr`, `/opt` и `$HOME/.local`. Если Cursor установлен в другом месте или не найден этими методами, скрипт может завершиться неудачей. Убедитесь, что Cursor доступен через одно из этих стандартных мест или методов.

**Windows**

```powershell
irm https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_win_id_modifier.ps1 | iex
```

<div align="center">
<img src="img/run_success.png" alt="Run Success" width="600"/>
</div>

</details>

<details open>
<summary><b>Пользователи из Китая (рекомендуется)</b></summary>

**macOS**

```bash
curl -fsSL https://aizaozao.com/accelerate.php/https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_mac_id_modifier.sh -o ./cursor_mac_id_modifier.sh && sudo bash ./cursor_mac_id_modifier.sh && rm ./cursor_mac_id_modifier.sh
```

**Linux**

```bash
curl -fsSL https://aizaozao.com/accelerate.php/https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_linux_id_modifier.sh | sudo bash
```

**Windows**

```powershell
irm https://aizaozao.com/accelerate.php/https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_win_id_modifier.ps1 | iex
```

</details>

<details open>
<summary><b>Запуск и настройка Windows Terminal</b></summary>

#### Как открыть терминал администратора в Windows:

##### Метод 1: Использование сочетания клавиш Win + X
```md
1. Нажмите сочетание клавиш Win + X
2. Выберите один из следующих вариантов в меню:
   - "Windows PowerShell (Администратор)"
   - "Windows Terminal (Администратор)"
   - "Terminal (Администратор)"
   (Варианты могут отличаться в зависимости от версии Windows)
```

##### Метод 2: Использование команды Win + R Run
```md
1. Нажмите сочетание клавиш Win + R
2. Введите powershell или pwsh в диалоговом окне Run
3. Нажмите Ctrl + Shift + Enter для запуска от имени администратора
   или введите в открывшемся окне: Start-Process pwsh -Verb RunAs
4. Введите скрипт сброса в терминале администратора:

irm https://aizaozao.com/accelerate.php/https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_win_id_modifier.ps1 | iex
```

##### Метод 3: Использование поиска
>![Search PowerShell](img/pwsh_1.png)
>
>Введите pwsh в поисковую строку, щелкните правой кнопкой мыши и выберите "Запуск от имени администратора"
>![Run as Administrator](img/pwsh_2.png)

Введите скрипт сброса в терминале администратора:
```powershell
irm https://aizaozao.com/accelerate.php/https://raw.githubusercontent.com/yuaotian/go-cursor-help/refs/heads/master/scripts/run/cursor_win_id_modifier.ps1 | iex
```

### 🔧 Руководство по установке PowerShell 

Если PowerShell не установлен на вашей системе, вы можете установить его одним из следующих способов:

#### Метод 1: Установка через Winget (рекомендуется)

1. Откройте командную строку или PowerShell
2. Выполните следующую команду:
```powershell
winget install --id Microsoft.PowerShell --source winget
```

#### Метод 2: Ручная установка

1. Загрузите установочный файл для вашей системы:
   - [PowerShell-7.4.6-win-x64.msi](https://github.com/PowerShell/PowerShell/releases/download/v7.4.6/PowerShell-7.4.6-win-x64.msi) (64-битные системы)
   - [PowerShell-7.4.6-win-x86.msi](https://github.com/PowerShell/PowerShell/releases/download/v7.4.6/PowerShell-7.4.6-win-x86.msi) (32-битные системы)
   - [PowerShell-7.4.6-win-arm64.msi](https://github.com/PowerShell/PowerShell/releases/download/v7.4.6/PowerShell-7.4.6-win-arm64.msi) (ARM64 системы)

2. Дважды щелкните загруженный установочный файл и следуйте инструкциям по установке

> 💡 Если у вас возникли проблемы, обратитесь к [официальному руководству по установке Microsoft](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows)

</details>

#### Windows Установка:

- 🔍 Автоматически обнаруживает и использует PowerShell 7, если он доступен
- 🛡️ Запрашивает права администратора через UAC
- 📝 Переходит на Windows PowerShell, если PS7 не найден
- 💡 Предоставляет ручные инструкции, если повышение прав не удалось

Вот и все! Скрипт выполнит:

1. ✨ Автоматическую установку инструмента
2. 🔄 Немедленный сброс пробного периода Cursor

### 📦 Ручная установка

> Загрузите соответствующий файл для вашей системы из [релизов](https://github.com/yuaotian/go-cursor-help/releases/latest)

<details>
<summary>Пакеты для Windows</summary>

- 64-бит: `cursor-id-modifier_windows_x64.exe`
- 32-бит: `cursor-id-modifier_windows_x86.exe`
</details>

<details>
<summary>Пакеты для macOS</summary>

- Intel: `cursor-id-modifier_darwin_x64_intel`
- M1/M2: `cursor-id-modifier_darwin_arm64_apple_silicon`
</details>

<details>
<summary>Пакеты для Linux</summary>

- 64-бит: `cursor-id-modifier_linux_x64`
- 32-бит: `cursor-id-modifier_linux_x86`
- ARM64: `cursor-id-modifier_linux_arm64`
</details>

### 🔧 Технические детали

<details>
<summary><b>Конфигурационные файлы</b></summary>

Программа изменяет конфигурационный файл `storage.json` Cursor, расположенный по адресу:

- Windows: `%APPDATA%\Cursor\User\globalStorage\storage.json`
- macOS: `~/Library/Application Support/Cursor/User/globalStorage/storage.json`
- Linux: `~/.config/Cursor/User/globalStorage/storage.json`
</details>

<details>
<summary><b>Измененные поля</b></summary>

Инструмент генерирует новые уникальные идентификаторы для:

- `telemetry.machineId`
- `telemetry.macMachineId`
- `telemetry.devDeviceId`
- `telemetry.sqmId`
</details>

<details>
<summary><b>Ручное отключение автоматического обновления</b></summary>

Пользователи Windows могут вручную отключить функцию автоматического обновления:

1. Закройте все процессы Cursor
2. Удалите каталог: `C:\Users\username\AppData\Local\cursor-updater`
3. Создайте файл с тем же именем: `cursor-updater` (без расширения)

Пользователи macOS/Linux могут попытаться найти аналогичный каталог `cursor-updater` в своей системе и выполнить ту же операцию.

</details>

<details>
<summary><b>Функции безопасности</b></summary>

- ✅ Безопасное завершение процессов
- ✅ Атомарные файловые операции
- ✅ Обработка ошибок и восстановление
</details>

<details>
<summary><b>Уведомление о модификации реестра</b></summary>

> ⚠️ **Важно: Этот инструмент изменяет реестр Windows**

#### Измененный реестр
- Путь: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography`
- Ключ: `MachineGuid`

#### Потенциальное воздействие
Изменение этого ключа реестра может повлиять на:
- Уникальную идентификацию устройства в системе Windows
- Статус распознавания и авторизации устройства для определенного программного обеспечения
- Функции системы, основанные на идентификации оборудования

#### Меры безопасности
1. Автоматическое резервное копирование
   - Оригинальное значение автоматически сохраняется перед изменением
   - Место резервного копирования: `%APPDATA%\Cursor\User\globalStorage\backups`
   - Формат файла резервного копирования: `MachineGuid.backup_YYYYMMDD_HHMMSS`

2. Шаги ручного восстановления
   - Откройте редактор реестра (regedit)
   - Перейдите к: `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography`
   - Щелкните правой кнопкой мыши на `MachineGuid`
   - Выберите "Изменить"
   - Вставьте значение из файла резервного копирования

#### Важные примечания
- Убедитесь в наличии файла резервного копирования перед изменением
- Используйте файл резервного копирования для восстановления оригинального значения при необходимости
- Требуются права администратора для изменения реестра
</details>

---

### 📚 Рекомендуемое чтение

- [Сборник проблем и решений Cursor](https://mp.weixin.qq.com/s/pnJrH7Ifx4WZvseeP1fcEA)
- [Руководство по универсальному помощнику разработчика AI](https://mp.weixin.qq.com/s/PRPz-qVkFJSgkuEKkTdzwg)

---

##  Поддержка

<div align="center">
<b>Если вы считаете это полезным, рассмотрите возможность покупки мне острого глютенового перекуса (Latiao) в знак признательности~ 💁☕️</b>
<table>
<tr>

<td align="center">
<b>微信赞赏</b><br>
<img src="img/wx_zsm2.png" width="500" alt="微信赞赏码"><br>
<small>要到饭咧？啊咧？啊咧？不给也没事~ 请随意打赏</small>
</td>
<td align="center">
<b>支付宝赞赏</b><br>
<img src="img/alipay.png" width="500" alt="支付宝赞赏码"><br>
<small>如果觉得有帮助,来包辣条犒劳一下吧~</small>
</td>
<td align="center">
<b>Alipay</b><br>
<img src="img/alipay_scan_pay.jpg" width="500" alt="Alipay"><br>
<em>1 Latiao = 1 AI thought cycle</em>
</td>
<td align="center">
<b>WeChat</b><br>
<img src="img/qun13.png" width="500" alt="WeChat"><br>
<em>二维码7天内(5月30日前)有效，过期请加微信</em>
</td>
<!-- <td align="center">
<b>ETC</b><br>
<img src="img/etc.png" width="100" alt="ETC Address"><br>
ETC: 0xa2745f4CD5d32310AC01694ABDB28bA32D125a6b
</td>
<td align="center"> -->
</td>
</tr>
</table>
</div>

---

## ⭐ Статистика проекта

<div align="center">

[![Star History Chart](https://api.star-history.com/svg?repos=yuaotian/go-cursor-help&type=Date)](https://star-history.com/#yuaotian/go-cursor-help&Date)

![Repobeats analytics image](https://repobeats.axiom.co/api/embed/ddaa9df9a94b0029ec3fad399e1c1c4e75755477.svg "Repobeats analytics image")

</div>

## 📄 Лицензия

<details>
<summary><b>MIT License</b></summary>

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

</details>




---
для запуска из выбранной директории

iex (Get-Content -Path "./cursor_win_id_modifier.ps1" -Raw)