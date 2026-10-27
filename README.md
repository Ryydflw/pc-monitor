# PC Monitor

**[Русский](#русский) · [English](#english)**

---

## Русский

Мониторинг ПК в реальном времени для Windows: графики CPU, GPU, ОЗУ, потребления, пинга и FPS игр, оверлей поверх игры, очистка памяти и защита от перегрева.

### Скачать

Раздел **Releases**, один файл — больше ничего ставить и скачивать не нужно:

| Система | Файл |
|---|---|
| Windows 10 / 11 (64-бит) | `PcMonitor-1.2.1.exe` |
| Windows 7 / 8 / 8.1 (64-бит) | `PcMonitor-1.2.1-win7.exe` |

При первом запуске Windows может показать «Windows защитила ваш компьютер» — так бывает со всеми новыми программами без платной цифровой подписи. Нажмите **Подробнее → Выполнить в любом случае**.

### Возможности

- **Экран загрузки:** видно, как запускаются датчики, счётчик FPS, пинг и очистка памяти.
- **Процессор:** загрузка, температура, частота (как в Диспетчере задач), мощность.
- **Видеокарта:** загрузка, температура, частота, мощность, видеопамять.
- **ОЗУ** и **очистка памяти** как в Mem Reduct: кнопка, **Ctrl+Shift+M** и автоочистка при заполнении на 90%. Во время игры память самой игры не трогается.
- **Пинг** с джиттером и потерями (адрес выбирается в настройках).
- **Потребление системы:** реальное, если у блока питания есть датчик (Corsair HXi/AXi/RMi, ASUS Thor), иначе — оценка с разбивкой CPU + GPU + прочее.
- **FPS и время кадра** игры; резкие просадки отмечаются красным. Игру можно выбрать вручную.
- **Панель «Статистика»** у левого края и **оверлей** поверх игры (**Ctrl+Shift+O**).
- **Защита от перегрева:** при 80 °C и выше игра сворачивается (или закрывается — по выбору).
- **Обновления:** при запуске программа сама проверяет GitHub и предлагает «Обновиться / Не сейчас»; новая версия скачивается и ставится сама. В версии для Windows 7 файл скачивается через браузер.
- **Автозапуск** с Windows, **языки** русский и английский.

### Конфиденциальность

**Мы ничего о вас не собираем.** Нет аккаунтов, рекламы и телеметрии.
- Датчики читаются у LibreHardwareMonitor на этом же компьютере (127.0.0.1).
- Пинг: раз в секунду на выбранный адрес уходит обычный ICMP-пакет без данных о вас. Можно выключить.
- Обновления: при запуске и по кнопке программа спрашивает у GitHub номер последней версии. Если вышла новая — появится окно «Обновиться / Не сейчас».
- Настройки хранятся только у вас в реестре (`HKCU\Software\PcMonitor`).

### Требования

64-битная Windows, права администратора (нужны для датчиков, FPS и очистки памяти), .NET Framework 4.7.2+ (в Windows 10/11 уже есть; на Windows 7 SP1 ставится отдельно).

### Ограничения

- Встроенная графика Intel отдаёт только частоту; полные данные — на дискретных AMD и NVIDIA.
- Без «умного» блока питания потребление системы — оценка.
- В эксклюзивном полноэкранном режиме игра может перекрыть оверлей — используйте «оконный без рамки».
- Версия для Windows 7 не проверялась на настоящей Windows 7.

---

## English

Real-time PC monitoring for Windows: CPU, GPU, RAM, power, ping and game FPS charts, an in-game overlay, a memory cleaner and overheat protection.

### Download

**Releases**, a single file — nothing else to install:

| System | File |
|---|---|
| Windows 10 / 11 (64-bit) | `PcMonitor-1.2.1.exe` |
| Windows 7 / 8 / 8.1 (64-bit) | `PcMonitor-1.2.1-win7.exe` |

On first run Windows may show "Windows protected your PC" — this happens to every new program without a paid code-signing certificate. Click **More info → Run anyway**.

### Features

- **Loading screen** showing sensors, FPS counter, ping and memory cleaner starting up.
- **Processor:** load, temperature, clock (as in Task Manager), power.
- **Graphics card:** load, temperature, clock, power, video memory.
- **RAM** and a **memory cleaner** like Mem Reduct: button, **Ctrl+Shift+M** and auto-clean at 90% usage. During a game the game's own memory is left alone.
- **Ping** with jitter and packet loss (address set in Settings).
- **System power:** measured if your PSU has a sensor (Corsair HXi/AXi/RMi, ASUS Thor), otherwise an estimate with a CPU + GPU + other breakdown.
- **FPS and frame time**, sharp drops marked red; the tracked game can be chosen manually.
- **Statistics panel** on the left edge and an in-game **overlay** (**Ctrl+Shift+O**).
- **Overheat protection:** at 80 °C or more the game is minimized (or closed — your choice).
- **Updates:** at startup the program checks GitHub and offers "Update / Not now"; the new version downloads and installs itself. In the Windows 7 edition the file is downloaded via the browser.
- **Autostart** with Windows, **languages** Russian and English.

### Privacy

**We collect nothing about you.** No accounts, ads or telemetry.
- Sensors are read from LibreHardwareMonitor on the same computer (127.0.0.1).
- Ping: once a second a plain ICMP packet with no data about you goes to the chosen address. Can be turned off.
- Updates: at startup and on the button the program asks GitHub for the latest version number. If a new one is out, you get an "Update / Not now" prompt.
- Settings stay on your PC in the registry (`HKCU\Software\PcMonitor`).

### Requirements

64-bit Windows, administrator rights (for sensors, FPS and memory cleaning), .NET Framework 4.7.2+ (built into Windows 10/11; install separately on Windows 7 SP1).

### Limitations

- Intel integrated graphics report only the clock; full data on discrete AMD and NVIDIA cards.
- Without a smart PSU, system power is an estimate.
- In exclusive fullscreen a game may cover the overlay — use borderless windowed mode.
- The Windows 7 edition has not been tested on a real Windows 7 machine.

---

### Благодарности / Credits

- **Mem Reduct** — автор **Henry++** ([github.com/henrypp/memreduct](https://github.com/henrypp/memreduct)). Очистка памяти в PC Monitor сделана по идее Mem Reduct; код Mem Reduct не используется — программа сама вызывает те же функции Windows. / The memory cleaner follows the idea of Mem Reduct by Henry++; no Mem Reduct code is used.
- **LibreHardwareMonitor** (MPL 2.0) — датчики / sensors.
- **Intel PresentMon** (MIT) — FPS.
- **Qt** (LGPL v3) — интерфейс / UI.

See `THIRD-PARTY-NOTICES.txt` inside the program.
