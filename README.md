# Helpdesk Incident Lab

Учебный проект-портфолио по обработке инцидентов IT Support, Help Desk и NOC L1.

Проект показывает, как специалист первой линии принимает обращение, уточняет симптомы, выполняет безопасную диагностику, отделяет подтверждённые факты от гипотез, готовит эскалацию и документирует решение.

> Все сценарии, результаты команд и причины неисправностей являются лабораторными или моделируемыми. Проект не описывает коммерческий опыт и не заменяет реальные политики организации.

## Цель проекта

- отработать структуру ITSM-инцидента;
- научиться документировать диагностику Windows и сети;
- показать понимание DNS, шлюза, маршрутизации, VPN и RDP;
- потренироваться в пользовательских комментариях и технических записях;
- подготовить материалы для обсуждения на собеседовании IT Support, Help Desk, Junior System Administrator или NOC L1.

## Что использовалось

- Jira Service Management — учебное оформление заявок;
- Windows networking — `ipconfig`, `ping`, `tracert`, `route print`, `nslookup`;
- PowerShell — `Test-NetConnection`;
- DNS, DHCP, DNS proxy/forwarder, NAT и default route;
- RDP, VPN, Active Directory и Group Policy на уровне диагностики;
- Markdown и GitHub для технической документации.

## Jira-сценарии

Все три учебные заявки прошли в Jira путь от `To Do` через `In Progress` до `Resolved`.

- [INC-001 — нет доступа в интернет](incidents/INC-001-no-internet.md) — KAN-4. Проверка локального шлюза, внешнего IP, DNS, маршрутизации и условий эскалации.
- [INC-002 — сайты не открываются по DNS-именам](incidents/INC-002-dns-resolution.md) — KAN-5. Различие между внешним доступом, DNS proxy, DNS через DHCP и локальным кэшем Windows.
- [INC-003 — ошибка подключения по RDP](incidents/INC-003-remote-access.md) — KAN-6. Разделение сетевой доступности, TCP 3389, VPN, аутентификации, AD-групп и Group Policy.

## База знаний

- [Диагностика сети Windows](knowledge-base/windows-network-diagnostics.md)
- [Диагностика DNS](knowledge-base/dns-troubleshooting.md)
- [Проверка удалённого доступа](knowledge-base/remote-access-checklist.md)

Каждая инструкция объясняет назначение команды, ожидаемый результат, ограничения и следующий шаг при неудаче.

## Доказательства работы в Jira

В каталоге [screenshots](screenshots/) сохранены учебные скриншоты:

- создание заявок;
- описание и приоритет;
- диагностические записи;
- комментарии пользователю;
- переход в `Resolved`;
- общий обзор очереди Jira.

Ключевой пример — [обзор проекта Jira](screenshots/14-project-overview.png).

## Как изучать проект

1. Начните с [INC-001](incidents/INC-001-no-internet.md), чтобы увидеть базовую структуру инцидента.
2. Сравните подтверждённые факты и гипотезы в разделе диагностики.
3. Изучите соответствующую инструкцию из [knowledge-base](knowledge-base/).
4. Посмотрите скриншоты Jira и сопоставьте их с этапами заявки.
5. Обратите внимание на условия эскалации и границы ответственности первой линии.

## Навыки, которые демонстрирует проект

- структурированный сбор симптомов и уточняющих вопросов;
- базовая диагностика IPv4 и сетевого подключения;
- понимание различий между шлюзом, маршрутом, NAT и DNS;
- анализ DNS proxy/forwarder и DHCP-настроек;
- проверка TCP-доступности RDP;
- различие между сетевой ошибкой и отказом аутентификации;
- понимание роли VPN, Active Directory и Group Policy;
- классификация, приоритизация и документирование инцидентов;
- понятная коммуникация с пользователем;
- корректная эскалация на вторую линию или сетевого администратора.

## Ограничения учебной лаборатории

Выводы команд, причины неисправностей и восстановление доступа в заявках обозначены как моделируемые, если в проекте нет фактического вывода из реальной инфраструктуры. Публичные DNS-серверы используются только как диагностическое сравнение, если это разрешено политикой организации. Пароли, токены и реальные конфиденциальные данные в проект не включаются.

## English summary

Helpdesk Incident Lab is a practical learning portfolio for IT Support, Service Desk and NOC L1 workflows.

It documents three simulated Jira incidents: loss of Internet access, DNS name resolution failure and an RDP authentication issue. The repository includes Windows network diagnostics, DNS troubleshooting, remote access checks, escalation criteria and Jira screenshots.

All command outputs and root causes are explicitly marked as simulated where they were not collected from real infrastructure.

## Процессы Service Desk

- [Учебная SLA-матрица](reports/sla-matrix.md) — условные значения времени реакции и решения.
- [Пример эскалации](knowledge-base/escalation-example.md) — какие данные передавать второй линии.
- [Сводный отчёт по инцидентам](reports/incident-summary.md) — сравнение трёх сценариев и общий процесс обработки.

SLA в этом проекте используется только как учебная модель. Реальные сроки определяются политикой конкретной организации.
