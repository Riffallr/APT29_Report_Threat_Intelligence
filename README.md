# APT29 Threat Profile and ATT&CK Mapping / Профиль угрозы APT29 и маппинг ATT&CK

## 🇬🇧 English Version

### Overview
This repository contains an independent Threat Intelligence research project focused on the **APT29** threat group (also known as Cozy Bear, Midnight Blizzard, NOBELIUM). 

The project was completed for educational purposes to demonstrate practical skills in:
*   Analyzing Advanced Persistent Threat (APT) behavior.
*   Mapping Tactics, Techniques, and Procedures (TTPs) to the **MITRE ATT&CK** framework.
*   Using **MITRE ATT&CK Navigator** to visualize threat actor profiles.
*   Formulating threat forecasts and actionable defense recommendations.

### Repository Contents
*   **`APT29_Report_EN.pdf`** — English version of the analytical report.
*   **`APT29_Report_RU.pdf`** — Russian version of the analytical report.
*   **`APT29_Heatmap.svg`** — Visualized ATT&CK Navigator layer showing the techniques used by APT29.
*   **`APT29_G0016_layer.json`** — The raw Navigator layer file (can be imported directly into the MITRE ATT&CK Navigator).

### Key Findings
Based on the official MITRE ATT&CK database (Group G0016), the research highlights APT29's shift towards **identity-based attacks** and exploitation of cloud environments:
*   **T1098 (Account Manipulation):** Active use of Azure AD, OAuth apps, and Service Principals for persistence and privilege escalation.
*   **T1059 (Command and Scripting Interpreter):** Heavy reliance on built-in tools like PowerShell and Cloud API (Microsoft Graph) to operate in the "grey zone" of logs.
*   **T1546 (Event Triggered Execution):** Using WMI event subscriptions for stealthy persistence.

### Recommendations
The report provides actionable defense strategies, including:
*   Auditing Azure AD and M365 logs for unauthorized Service Principals and Device Registrations.
*   Detecting anomalous PowerShell usage (e.g., `-EncodedCommand`) and suspicious WMI subscriptions.
*   Implementing robust protection against Password Spraying and enforcing unconditional MFA.

---

## 🇷🇺 Русская версия

### Описание проекта
Данный репозиторий содержит независимое исследование в области Threat Intelligence, посвященное анализу группировки **APT29** (также известной как Cozy Bear, Midnight Blizzard, NOBELIUM).

Проект выполнен в учебных целях для демонстрации практических навыков:
*   Анализа поведения Advanced Persistent Threat (APT) группировок.
*   Маппинга Тактик, Техник и Процедур (TTP) на фреймворк **MITRE ATT&CK**.
*   Использования **MITRE ATT&CK Navigator** для визуализации профилей угроз.
*   Формулирования прогнозов и практических рекомендаций по защите.

### Содержимое репозитория
*   **`APT29_Report_RU.pdf`** — Основной аналитический отчет на русском языке.
*   **`APT29_Report_EN.pdf`** — Англоязычная версия отчета.
*   **`APT29_Heatmap.svg`** — Визуализация техник APT29 в матрице ATT&CK Navigator.
*   **`APT29_G0016_layer.json`** — Исходный файл слоя Navigator (можно импортировать напрямую в MITRE ATT&CK Navigator).

### Ключевые выводы
На основе официальной базы MITRE ATT&CK (Group G0016) в исследовании highlighted сдвиг APT29 в сторону **атак на инфраструктуру идентификации (identity-based attacks)** и эксплуатации облачных сред:
*   **T1098 (Account Manipulation):** Активное использование Azure AD, OAuth-приложений и Service Principals для закрепления и повышения привилегий.
*   **T1059 (Command and Scripting Interpreter):** Опора на встроенные легитимные утилиты (PowerShell, Cloud API / Microsoft Graph) для работы в «серой зоне» логов.
*   **T1546 (Event Triggered Execution):** Использование подписок на события WMI для скрытого закрепления в системе.

### Рекомендации
В отчете предложены практические стратегии защиты, включая:
*   Аудит логов Azure AD и M365 на предмет создания несанкционированных Service Principals и Device Registrations.
*   Детектирование аномального использования PowerShell (например, флаг `-EncodedCommand`) и подозрительных подписок WMI.
*   Внедрение надежной защиты от Password Spraying и обязательное использование MFA для привилегированных аккаунтов.

---
*Disclaimer / Отказ от ответственности: This project is for educational and portfolio purposes. All TTP data is sourced from the publicly available MITRE ATT&CK knowledge base. / Данный проект создан в учебных и портфолио-целях. Все данные по TTP взяты из общедоступной базы знаний MITRE ATT&CK.*
