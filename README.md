## About
#### App pulsemarket for Telegram Mini apps.
Dev link: https://fhntv06.github.io/telegram-mini-apps/

### Для включения тесовых данных нужно файле useGameSocket:
1) данные initialDataGameStatus добавить как default значение в хук setData
2) изменить значение переменной initTestData на true

## График
График построен с помощью библиотеки chart.js - https://www.chartjs.org/docs/latest/

**TODO**: переписать реализацию получения данных из контекста
согласно видео: https://www.youtube.com/watch?v=k2g_Og3CFKU

Работа со слоями (100 - эталон):  
<blockquote>
0 - Main (и другие страницы)<br>
2 - Modal и blur<br>
(Появляются на только на страницах, поэтому ModalProvider и AnimationProvider оборачивают только Main, чтобы было глобально можно добавить настройку, которая будет регулироваться z-index и position)<br>
1 - PanelMenu (тк нужно располагать на всех страницах)<br>
1 - AnimationBlock (тк анимация должна быть видна только на Main)<br>  
100 - OnboardingStats  
</blockquote>

## Переменные окружения
#### Dev mode
VITE_IS_DEV_MODE=false

#### HOST DEV SERVER
VITE_DOMAIN=nemitor.ru# - dev
#VITE_DOMAIN=pulsemarket.online
VITE_PORT=3000

#### API
VITE_API_PROTOCOL=https

#### SOCKET
VITE_SOCKET_PROTOCOL=wss
VITE_ADDRESS_TRANSACTION=EQB-bjIC4WX9Al-yKbmnHcRgy4wZBac4aXtRB4a1OrRnxbO7
VITE_UP_TRANSACTION=te6cckEBAQEABwAACUCvDQrA66ueng==
VITE_DOWN_TRANSACTION=te6cckEBAQEABwAACUCvDQpAk5BoHA==

#### Service posthog
VITE_PUBLIC_POSTHOG_KEY=phc_1vvr2JSubLcWvwZZP4rgQhSxMIz78KiIRUhw1ZXbT9Z
VITE_PUBLIC_POSTHOG_HOST=https://eu.i.posthog.com

#### Manifest url for mini apps
VITE_PUBLIC_MANIFEST_URL=https://raw.githubusercontent.com/tonpulse/CryptoMarketManifest/refs/heads/main/tonconect-manifest.json
VITE_PUBLIC_PATH_FOR_GITHUB_PAGES=/telegram-mini-apps
