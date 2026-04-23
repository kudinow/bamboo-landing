# Yumisa — Legal Review Report

**Дата:** 21 апреля 2026
**Reviewer:** Claude (юридическое ревью)
**Объём:** 4 документа — Privacy Policy, Terms of Use, COPPA Policy, GDPR Compliance
**Бенчмарки:** Cal AI, MyFitnessPal, Bitepal (Reface Lithuania UAB), Lifesum AB, YAZIO GmbH
**Регуляторика:** GDPR, EU AI Act, COPPA Update 2025, CCPA/CPRA 2026, Washington MHMDA, FTC Click-to-Cancel/ROSCA, LGPD Brazil, App Store/Google Play 2026

**Status: 2026-04-24 — ALL PLACEHOLDERS RESOLVED ✅**

Юр. лицо `"Sunction" Limited Liability Partnership` подставлено во все 4 документа (BIN 250740000603, 133/1 Gagarin Avenue, Office 104, Bostandyk District, Almaty 050060, Republic of Kazakhstan). Editor-note `{IS / IS NOT}` в COPPA §10 Safe Harbor зарезолвен как **"is not currently a member"**. Документы publish-ready pending final lawyer review.

**Open items для Nick (не блокеры):**
1. **Sunction LLP vs Bureau613 — подтвердить структуру.** В документах юр. лицо Sunction LLP, бренд Yumisa, support-email @bureau613.com. Если Bureau613 — это отдельное юр. лицо (не альтер-эго Sunction), нужен intragroup data-sharing agreement между ними, иначе передача персональных данных между Sunction и Bureau613 формально не покрыта. Если @bureau613.com — просто домен для email (мейлбокс принадлежит Sunction), вопросов нет.
2. **OKED mismatch.** В Казахстанском реестре у Sunction LLP основной вид деятельности — "Оптика" (47.78.2 или близкий). Для мобильного приложения нужно добавить **62.01 "Деятельность в области компьютерного программирования"** или **63.12 "Деятельность web-порталов"**, иначе tax authorities могут квалифицировать доходы от App Store/Play как non-core и применить другой режим. Делается через e-license.kz за 1-2 дня.
3. **DUNS 302120631** — сохранить, нужен для Apple Developer Program enrollment как юр. лицо (не individual).
4. **Юрисдикция (AIFC vs ТОО).** Сейчас governing law в Terms §13 = Delaware + AAA arbitration (US-friendly default для SaaS). Для ТОО это работает, но при росте бизнеса и реальных спорах на территории РК казахстанский суд может отказать в признании foreign arbitration clause. Если переедете в AIFC (английское право + AIFC Court + IAC arbitration) — это fix-all, но надо будет обновить §13. Пока оставляем Delaware.

---

**Updates 2026-04-21 to 2026-04-24 (session summary):**

✅ **Analytics stack:** Appmetrica (Yandex / RU) заменена на **Adjust GmbH** (Berlin, EU) — см. Risk #1 (RESOLVED). Adjust = attribution + fraud detection + pseudonymous analytics. Caveat: полноценный product analytics (funnels, retention cohorts, session replay) Adjust не закрывает — если добавится Mixpanel/PostHog/Firebase, нужно обновить §4 Privacy Policy.

✅ **Единый контакт-email:** `support@bureau613.com` подставлен вместо 7 email-placeholders (PRIVACY / SUPPORT / DPO / LEGAL / EU_REP / UK_REP / DPO_BRAZIL).

✅ **Website URL:** `https://www.yumisa.app` подставлен везде.

✅ **Effective date:** May 1, 2026.

✅ **Pricing:** специфические цены убраны из Terms §4.2; формулировка "as displayed in App Store / Google Play at the time of purchase" — поддерживает региональные pricing tiers без правок документов.

✅ **Defaults подставлены:** retention (30 дней фото + diary как текст; 30 дней grace + 90 дней бэкапы), hosting (AWS Frankfurt eu-central-1), AI (OpenAI + Anthropic, оба DPF-certified + SCCs), Adapty (USA + DPF), support (Intercom), App Store rating 12+, Play Teen, US governing law Delaware, dispute resolution AAA arbitration + 30-day opt-out.

✅ **DPO:** не назначен формально (не требуется под Art. 37(1) GDPR для размера Yumisa); Yumisa Privacy Team = контакт. Brazil Encarregado = та же Privacy Team (LGPD Art. 41).

⚠️ **Art. 27 EU/UK Representatives — пользователь решил НЕ оформлять** (риск принят, см. раздел "Accepted Risks" ниже). Секция §2 в GDPR doc заменена на нейтральный "Contact for EU and UK Data Subjects". Строки EU_REP и UK_REP удалены из Privacy Policy §16.

✅ **CCPA phone — удалён** (пользователь принял риск по §1798.130(a)(1)(A)). Осталось только email-контактирование.

✅ **Kazakhstan carve-out:** добавлен в Terms §1.1 и Privacy Policy §13.1 — "Service is not directed at residents of the Republic of Kazakhstan" + ссылка на закон РК №94-V.

✅ **Реквизиты юр. лица подставлены (2026-04-24):** `"Sunction" Limited Liability Partnership`, BIN 250740000603, 133/1 Gagarin Avenue, Office 104, Bostandyk District, Almaty 050060, Republic of Kazakhstan — во всех 4 документах. Editor-note `{IS / IS NOT}` в COPPA §10 зарезолвен как "is not currently a member". **ZERO placeholders в 4 живых документах.**

⚠️ **Осталось только:** выбор юрисдикции AIFC vs ТОО для Terms §13. Сейчас default = Delaware + AAA arbitration (работает для ТОО). Опционально — если переходите в AIFC, §13 пересматривается на English law + AIFC Court.

---

## Accepted Risks (решения пользователя, принятые осознанно)

1. **No Art. 27 EU Representative** — GDPR §27 формально требует назначить representative в EU. Риск: жалоба EU-пользователя → расследование DPA → штраф до €10M или 2% global revenue (Art. 83(4), lower tier); на практике для small apps — €5-50K + order to appoint в 30 дней или EU service ban. Mitigation: secция §2 GDPR doc переделана в нейтральную "Contact for EU and UK Data Subjects" — документ не рекламирует гэп; EU-пользователи могут обращаться напрямую на support@bureau613.com. Рекомендация: если в первые 6-12 месяцев будут EU-пользователи > 500-1K, пересмотреть и оформить через Prighter (€175/год).

2. **No UK Representative** — зеркально Art. 27 UK GDPR. Те же рисковые параметры (ICO штрафует до £8.7M или 2% global revenue).

3. **No phone in Privacy Policy** — CCPA §1798.130(a)(1)(A) требует телефон для US-резидентов. Риск: жалоба California AG → civil penalty до $2,500 за violation (или $7,500 за intentional). Mitigation: указан email, который покрывает большинство CCPA requests де-факто. Рекомендация: при росте US-базы > 5K завести виртуальный номер ($1/мес через Twilio / Google Voice).

---

## TL;DR — ТРИ КРИТИЧЕСКИХ РИСКА

### ✅ Risk #1 — RESOLVED: Appmetrica → Adjust GmbH
**Было:** Во всех 4 документах упоминалась `Appmetrica` (Yandex / RU) как processor продуктовой аналитики. Для глобального запуска это несовместимо с GDPR (нет adequacy decision для России, нет SCCs, нет DPF), нарушает sanctions-driven политику Apple/Google и создавало репутационный риск.

**Стало (2026-04-21):** Заменена на **Adjust GmbH** (Saarbrücker Str. 37a, 10405 Berlin, Germany). Adjust — один из топ-3 MMP (Mobile Measurement Partner) в EU, GDPR-native (сертифицирован), SOC 2 Type II, Privacy Shield преемник через SCCs, работает с MyFitnessPal, Lifesum, YAZIO. Юрисдикция — Германия (BDSG + GDPR), processor status, DPA доступен напрямую.

**⚠️ Важный caveat:** Adjust — это **attribution / MMP**, а не **product analytics**. Он закрывает:
- UA attribution (откуда пришёл установщик)
- Fraud detection
- Cohort analysis (basic)
- SKAdNetwork (iOS)

Но **НЕ закрывает**: funnel analytics, retention cohorts, event-based product analytics, session replay, feature flags. Если они нужны — потребуется доп. tool (Mixpanel EU / PostHog Cloud EU / Firebase Analytics). В текущих документах указан только Adjust — если добавляется product analytics tool, нужно обновить §4 Privacy Policy (Third-Party Processors table).

### 🔴 Risk #2 — Возрастные пороги несогласованы между документами
- **Terms (§1):** 16 лет, под 18 — parental consent
- **COPPA Policy (§2):** не для детей **под 13**, "designed for users 16+"
- **GDPR Compliance (§9):** "not directed at children under 16 in the EU"
- **Privacy Policy:** не указано

Это **прямое противоречие** между документами + не учитывает национальные пороги GDPR (UK 13, IT 14, ES 14, FR 15, DE 16). При regulator audit или App Store review это flag.

**Что делать:** установить единый policy: "16+ globally" + age gate с проверкой по стране пользователя для младшей юрисдикции. Зеркалить во всех 4 документах.

### 🔴 Risk #3 — Отсутствие Washington My Health My Data Act (MHMDA), CCPA-block для США
Документы не содержат **отдельного раздела про consumer health data** (требование MHMDA с 31 марта 2024) и не покрывают права жителей California, Virginia, Colorado, Connecticut, Texas, Maryland и др. Калории + фото еды + вес = consumer health data в Washington и sensitive personal information в California. Без этого — private right of action в WA ($25K/violation), enforcement от CA AG, PRA для пользователей.

**Что делать:** добавить секцию "US State Privacy Rights" в Privacy Policy + отдельную "Washington Health Data Privacy Notice" (как у MyFitnessPal).

---

## КАК ЧИТАТЬ ОТЧЁТ

Каждый из 4 разделов ниже — это разбор одного документа. Внутри:
- **Что сейчас написано** (резюме)
- **Сильные места** — что не трогать
- **Критические правки** (🔴 — must-fix до запуска)
- **Серьёзные правки** (🟡 — нужно до запуска, не критично)
- **Косметика и улучшения** (🟢 — желательно)
- **Сравнение с конкурентами** — как у них и почему лучше/хуже

В конце отчёта — финальный чек-лист и приоритеты.

---

# 1. PRIVACY POLICY — РЕВЬЮ

**Файл:** `privacy-policy.md` (143 строки, 12 секций)

## Что есть сейчас
Базовый шаблон GDPR-style privacy policy. Есть: типы данных, цели обработки, data sharing table, retention, rights, cookies, contact. Структура понятная, юридический язык приемлемый.

## ✅ Сильные места
1. **Чёткая таблица "Recipient → Purpose → Data Shared"** (§4) — лучше, чем сплошной prose у MyFitnessPal. Похвалю.
2. **Health data** явно выделен как категория (§1.1). Хорошо.
3. **"We do not sell your personal data"** в начале §4 — правильный сигнал.
4. **Раздел про international transfers** (§7) с упоминанием SCC — базово ок.

## 🔴 Критические правки (must-fix)

### CR-PP-1. Удалить Appmetrica из таблицы (§4)
> | Appmetrica | Product analytics | Usage events, device info |

**Проблема:** Yandex (Russia) processor. См. Risk #1 выше.
**Правка:** Заменить на "Mixpanel" или "Firebase Analytics" (или другой EU/US-based provider). Перед публикацией решить, кого реально интегрируете технически. То же — в COPPA и GDPR.

### CR-PP-2. Добавить секцию "US State Privacy Rights"
**Что добавить (новая секция перед "Cookies and Tracking"):**
- California (CCPA/CPRA): право на access, delete, correct, opt-out of sale/sharing, opt-out of automated decision-making (ADMT), limit use of sensitive PI
- Virginia (VCDPA), Colorado (CPA), Connecticut (CTDPA), Texas (TDPSA), Utah (UCPA), Oregon (OCPA), Delaware, New Hampshire, Maryland (MODPA), Iowa, Indiana, Tennessee, Montana, New Jersey
- Универсальные права + ссылка на форму запроса
- Прямое заявление: "We do **not** sell or share your sensitive personal information (including health data) for cross-context behavioral advertising"
- Notice at Collection (CCPA Reg § 7012)

**Бенчмарк:** MyFitnessPal делает это через "Privacy Request Center" с per-state breakdown — это лучшая практика. Cal AI этого не имеет — гэп.

### CR-PP-3. Добавить отдельный блок для Washington Consumer Health Data
**Почему:** MHMDA требует отдельный, доступный с homepage документ. Это критично, если есть US users.
**Решение:** либо отдельный документ (как у MyFitnessPal — `washington-health-data-privacy-policy`), либо чёткий раздел в Privacy Policy с собственным URL (`/privacy-policy#washington-health-data`).
**Содержание:**
- Категории "consumer health data" (food logs, calorie estimates, weight, height, dietary patterns, body composition)
- Правовые основания
- Right to confirm, access, delete, withdraw consent (45-day SLA)
- Запрет геофенсинга вокруг health-related locations
- Отдельная контактная форма

### CR-PP-4. Добавить LGPD Brazil
**Что добавить:**
- Раздел "Brazil (LGPD)" с правами субъекта (ст. 18 LGPD): confirmation of processing, access, correction, anonymization/blocking/deletion, portability, deletion of data processed with consent, information about sharing
- Контакт DPO/encarregado (если revenue в BR > BRL 16M)
- Lawful basis на ст. 7/11 LGPD (особенно ст. 11 для sensitive data)
**Локализация:** документы в обязательном порядке должны быть в **PT-BR** для бразильского рынка (если запускаемся в Бразилии).

### CR-PP-5. Раскрыть конкретных AI-провайдеров (§3.2)
Сейчас плейсхолдеры `{AI_PROVIDER_1}`, `{AI_PROVIDER_2}`. **GDPR Art. 13/14 transparency** требует раскрытия категорий получателей или конкретных processors.
**Что сделать:** если используется OpenAI / Google Vision / Anthropic / Gemini / собственная модель — назвать их по имени и регион обработки. Минимум: "Our food recognition uses [Provider X]'s vision API hosted in EU/US."
**Бенчмарк:** Cal AI прячет провайдеров — это слабость, повторять не стоит. Lifesum называет интеграции прямо.

### CR-PP-6. Указать конкретный retention для food photos (§5)
Сейчас: `{PHOTO_RETENTION_PERIOD}`. Это нельзя оставить — GDPR storage limitation требует определённости.
**Рекомендация:**
- "Food photos used for personal diary: retained for the lifetime of your account"
- "Food photos used for AI model improvement: anonymised within 24 hours of upload, retained for up to 12 months in anonymised form, then deleted"
- Дать механизм opt-out из training (см. CR-PP-7).

### CR-PP-7. Добавить opt-out из AI model training
**Почему:** EDPB Opinion 28/2024 требует, чтобы legitimate interest для AI training был сбалансирован с правами субъекта. Без opt-out этот баланс трудно защитить.
**Где:** новая под-секция в §3 ("AI Model Improvement — Opt-Out"). Также упомянуть в §8 (Your Rights).
**Текст-заготовка:**
> "By default, we may use anonymised photos to improve our food recognition AI. You can opt out at any time in Settings → Privacy → AI Improvement. Opting out does not affect your access to the Service."

### CR-PP-8. Обновить раздел про international transfers (§7)
Сейчас упомянуты только SCC. На 2025-2026 нужно:
- **EU → US:** EU-US Data Privacy Framework (DPF) с supplementary measures + SCC fallback
- **UK:** UK IDTA или UK Addendum к SCC
- **Brazil:** ANPD-approved SCCs (с 23 августа 2025)
- Указать конкретные страны хостинга
- Дать пользователю возможность запросить копию SCC (как делает MyFitnessPal)

### CR-PP-9. Добавить раздел "Automated Decision-Making and AI"
**Почему:** EU AI Act (transparency obligations effective Aug 2026) + CCPA ADMT regulations требуют explicit disclosure: "this app uses AI to estimate nutritional values." Без этого риск нарушения transparency duty.
**Содержание:**
- Описание системы AI (food recognition по photo/text/audio)
- Что AI **не делает** (medical diagnosis, treatment, decisions with legal effects)
- Право пользователя на human review при оспаривании результата
- Точность модели и допустимая погрешность ("estimates may vary by ±15-25%")

### CR-PP-10. Health Breach Notification Rule (HBNR)
**Почему:** FTC HBNR (обновлён 2024) применяется к health apps вне HIPAA. Обязательное breach notification в 60 дней.
**Где:** упомянуть в §6 (Data Security) или новой подсекции.

## 🟡 Серьёзные правки

### SR-PP-1. Уточнить §1.1 "Account information"
"name, age, gender (if provided during registration)" — лучше написать "date of birth (used to verify age, see Eligibility) и optional gender". Age как просто число ослабляет COPPA-compliance.

### SR-PP-2. §1.3 — добавить marketing/social opt-in providers
Если есть Meta SDK, TikTok Pixel, App Tracking Transparency, Branch — все они должны быть упомянуты. Не упоминать = under-disclosure.

### SR-PP-3. §2 "Improve AI accuracy" — переписать
Сейчас: "use anonymized and aggregated food photo data to improve our recognition models". Слово "anonymized" в EU GDPR имеет узкое значение (полная необратимость). Лучше: "We may process pseudonymised food photo data (with personal identifiers removed) to improve our AI models. See Section 3 for details and your opt-out right."

### SR-PP-4. §6 (Security) — добавить конкретику
- "Encryption at rest: AES-256"
- "Encryption in transit: TLS 1.3"
- "Authentication: bcrypt for passwords, OAuth 2.0 for sign-in providers"
- "Annual penetration testing by [vendor]"
- "SOC 2 Type II / ISO 27001 in progress / certified" (если применимо)

### SR-PP-5. §8 (Your Rights) — уточнить timelines
- GDPR: 1 month (extension до 3 months возможна)
- COPPA / MHMDA / CCPA: специфические SLAs
- Указать: "We will respond within 30 days (45 days under MHMDA / CCPA)"

### SR-PP-6. §9 — конфликт "App does not use cookies" vs SDK identifiers
Если у вас есть website (а почти у всех есть лендинг), там cookies используются. Раздел нужно переписать с фокусом на **mobile SDK identifiers + website cookies** отдельно.

### SR-PP-7. §11 (Changes) — добавить материальные изменения
"Material changes" — определить, что это (изменения покрытия данных, появление новых categories, новые processors). Дать opt-out при substantive material change.

## 🟢 Улучшения

- **§12 Contact:** добавить отдельные emails: privacy@yumisa.app, dpo@yumisa.app, support@yumisa.app — лучше один общий placeholder.
- **In-line ссылки** на сторонние politики (Apple App Store, Google Play, AI providers) — повышает transparency score у App Store/Play review.
- **TOC (Table of Contents)** в начале документа — улучшает UX и формально соответствует "easy to read" требованию ICO/CNIL.
- **Дата последнего обновления + история изменений** (changelog) внизу.

## Сравнение с конкурентами

| Аспект | Yumisa (текущий) | Cal AI | MyFitnessPal | Lifesum | Yazio |
|---|---|---|---|---|---|
| US state-level rights | ❌ | ⚠️ (CA only) | ✅ (per-state) | ⚠️ basic | ⚠️ basic |
| Washington MHMDA | ❌ | ❌ | ✅ (отдельный документ) | ❌ | ❌ |
| LGPD Brazil | ❌ | ❌ | ⚠️ упомянут | ❌ | ❌ |
| AI providers named | ❌ (placeholders) | ❌ | ⚠️ generic | ✅ конкретные | ⚠️ |
| Photo retention specifics | ❌ | ❌ vague | ❌ vague | ⚠️ | ✅ конкретно |
| AI training opt-out | ❌ | ❌ | ❌ | ❌ | ❌ |
| Art. 9 health data explicit consent | ⚠️ implied | ❌ | ⚠️ | ✅ explicit | ⚠️ |

**Вывод:** мы можем стать leaders на нашем рынке, если закроем перечисленные гэпы. У всех конкурентов одни и те же дыры — это возможность для дифференциации ("trust as a feature").

---

# 2. TERMS OF USE — РЕВЬЮ

**Файл:** `terms-of-use.md` (131 строка, 15 секций)

## Что есть сейчас
Стандартный SaaS Terms with consumer-app слой: subscription auto-renewal, IP, disclaimers, limitation of liability, termination, governing law (placeholder).

## ✅ Сильные места
1. **§2 Disclaimer "App provides estimates"** + "not a medical device" — правильная защита от health-claim liability.
2. **§4.4 Billing** — корректно ссылается на App Store / Google Play.
3. **§4.3 Free Trial** с auto-conversion — explicit notice (требуется по ROSCA).
4. **§7 Data Export Feature** — выделение этой части в отдельную секцию это правильно.

## 🔴 Критические правки

### CR-TOS-1. Возрастной порог — несогласован с COPPA Policy
**§1 Eligibility:** "at least 16 years old. If you are under the age of 18, you represent that your parent or legal guardian has reviewed and agreed". COPPA Policy говорит "13+". GDPR §9 говорит "16 in EU". **Три источника — три разных порога.**
**Решение:**
- Утвердить **единую цифру: 16+ globally** (соответствует Германии — самой строгой EU юрисдикции, и упрощает COPPA: 13-15 не разрешено, 16-17 — parental consent, 18+ — full)
- Или: **13+ globally с национальным age-gate** (сложнее в реализации, но даёт TAM шире)
- Зеркалировать выбор во всех 4 документах + UI age-gate

### CR-TOS-2. FTC Click-to-Cancel / ROSCA compliance в §4
Сейчас: "manage and cancel your subscription through your App Store or Google Play account settings". Этого недостаточно даже после vacation FTC click-to-cancel rule в июле 2025 — ROSCA, FTC Act §5 и state laws (особенно CA AB-390, NY UDP) продолжают требовать:
- **Same-medium cancellation:** если signup в app — cancel должен быть в app (не только delegated to App Store)
- **Pre-charge clear disclosure:** все material terms BEFORE charging (price, frequency, что происходит после trial)
- **Простая отмена:** ≤2 клика
- **Cancellation confirmation** (email/in-app)
**Правка:** добавить секцию "How to Cancel" с явным шагов-by-шагов в Yumisa app + in App Store/Play. Прямой текст: "You can cancel anytime in Settings → Subscription → Cancel without speaking to anyone or filling forms."

### CR-TOS-3. User content license — слишком широкая, нет training data clause
**§5.1:** "non-exclusive, worldwide, royalty-free license to use, process, and analyze such content solely for the purpose of providing the Service."
**Проблема:** "providing the Service" не покрывает AI model training. Если будете тренировать модель на user photos — без отдельного клауза это challengeable.
**Правка:** разделить:
- License A — для предоставления сервиса (обработка, анализ, хранение)
- License B (opt-in!) — для AI model improvement, с правом отзыва (ср. с CR-PP-7)

### CR-TOS-4. AI accuracy disclaimer слаб
Сейчас (§2): "may contain inaccuracies". Это формально, но недостаточно для FTC Section 5 + EU UCPD (Unfair Commercial Practices Directive). Нужно конкретнее.
**Бенчмарк MyFitnessPal:** "AI content may contain errors or misleading information... bears no liability".
**Правка:**
> "Yumisa's AI-powered nutritional analysis provides **estimates** with typical accuracy of ±15-25% relative to laboratory analysis. Results depend on photo quality, food complexity, portion size estimation, and visibility of ingredients. Yumisa does not guarantee accuracy and is **not a substitute for professional dietary, medical, or clinical advice**. If you have allergies, dietary restrictions, diabetes, eating disorders, or any medical condition, consult a licensed healthcare provider."

### CR-TOS-5. Отсутствует EU consumer carve-out для §9 Limitation of Liability
**§9 Limitation of Liability:** US-style cap. Это **не работает для EU consumers** — UCPD + national consumer laws (German BGB, French Code de la consommation) запрещают broad disclaimers liability for personal injury / gross negligence / wilful misconduct.
**Правка:** добавить секцию "EU/EEA Consumers" с явным исключением:
> "Nothing in these Terms limits or excludes our liability for: (a) death or personal injury caused by negligence; (b) fraud or fraudulent misrepresentation; (c) any liability that cannot be limited under applicable consumer protection laws of your country of residence."

### CR-TOS-6. §13 Governing Law / Disputes — placeholder + критическая структура
Сейчас: `{GOVERNING_LAW_JURISDICTION}` + `{DISPUTE_RESOLUTION_METHOD}`. Нужны **отдельные правила для US и EU**.
**Структура:**
- **US users:** Delaware law + binding individual arbitration (AAA Consumer Rules) + class action waiver + 30-day opt-out из arbitration. (Это работает в US, защищает от class actions.)
- **EU/UK users:** law of consumer's country of residence + court of consumer's domicile (mandatory under Reg. 1215/2012). Никакой mandatory arbitration.
- **Brazil:** ст. 17/22 CDC — court в месте жительства потребителя.
- Choice of law clause не должна лишать consumer non-derogable protections home jurisdiction.

### CR-TOS-7. §7 Data Export — добавить HIPAA / health professional disclaimer
Сейчас вы пишете: "export your nutritional data for sharing with health professionals." **Риск:** если nutritionist/trainer использует это для лечения, может triggered HIPAA или государственные правила (Washington MHMDA, CA Health Data). Нужно явно:
> "Exported data is for personal informational use. If you choose to share with a healthcare professional, you do so at your own discretion. Yumisa does not establish a HIPAA Business Associate relationship by enabling this export. Healthcare providers receiving this data must comply with their own legal obligations."

## 🟡 Серьёзные правки

### SR-TOS-1. §4.5 Price Changes
Добавить SLA для notice: "at least 30 days' advance notice via email and in-app". App Store / Google Play требуют explicit re-consent для price increase.

### SR-TOS-2. §6 Intellectual Property — добавить trademark notice
"Yumisa™ and the Yumisa logo are trademarks of {LEGAL_ENTITY_NAME}. All rights reserved."

### SR-TOS-3. §11 Termination — детализировать data retention после termination
Сейчас: `{DATA_RETENTION_PERIOD_AFTER_TERMINATION}`. Замените конкретикой: 30/60/90 дней. Учесть legal holds (tax records — 7 лет в большинстве юрисдикций).

### SR-TOS-4. Добавить §15a "Beta Features"
Если планируете A/B тесты, новые AI-модели в beta — стандартная beta clause: "as-is, no warranty, no SLA, may be removed at any time".

### SR-TOS-5. §3 Account Registration — добавить запрет на multiple accounts / sharing
Important для prevent free-trial abuse. "You may create only one account per person. Sharing accounts is prohibited."

## 🟢 Улучшения

- TOC в начале документа.
- "Plain English Summary" в начале каждой секции (тренд с 2024-2025 для transparency).
- Glossary терминов (App, Service, User, Content, Subscription).
- Версия "Last Updated" + summary of changes.

## Сравнение с конкурентами

| Аспект | Yumisa | Cal AI | MyFitnessPal | Lifesum |
|---|---|---|---|---|
| FTC Click-to-Cancel language | ❌ | ❌ | ✅ | ⚠️ |
| AI accuracy quantified (±%) | ❌ | ❌ | ⚠️ generic | ❌ |
| EU consumer carve-out | ❌ | ❌ | ❌ | ✅ (шведский регулятор) |
| Arbitration + opt-out | ❌ | ✅ 30-day | ✅ 30-day | ❌ |
| Health professional/HIPAA carve-out | ⚠️ слабо | ❌ | ⚠️ | ❌ |
| Multiple accounts ban | ❌ | ✅ | ✅ | ✅ |

---

# 3. COPPA POLICY — РЕВЬЮ

**Файл:** `coppa-policy.md` (90 строк, 10 секций)

## Что есть сейчас
Базовая COPPA compliance декларация: app не для детей <13, age gate, не сохраняем DOB underage users, удаление данных при обнаружении, parental rights, third-party SDKs disclosure.

## ✅ Сильные места
1. **§3 явный age gate** с конкретным сообщением — лучше, чем "we don't target children" без mechanism.
2. **§4 immediate deletion + termination + parent notification** — корректная COPPA процедура.
3. **§7 explicit App Store / Google Play declarations** — это сигналит на review.

## 🔴 Критические правки

### CR-COPPA-1. **COPPA Final Rule 2025 не учтён**
FTC финализировала обновления **в январе 2025**, в силу с **23 июня 2025**, full compliance к **22 апреля 2026 (это уже сегодня!)**. Что добавлено:
- **Personal information** теперь включает biometric identifiers (фото, голос — у нас обе) и government identifiers
- **Separate verifiable parental consent** для каждого из:
  - Sharing data с third parties (для рекламы)
  - Disclosing для targeted advertising
  - Internal AI/ML training
- **Data retention limits:** не дольше, чем "reasonably necessary"
- **Written information security program** для children's data
- Новые approved methods для verifiable parental consent: knowledge-based authentication, government ID + selfie verification
**Правка:** переписать §4-§5 с учётом этих требований. Если планируете users 13+, нужен flow для получения parental consent для users 13-17 (если возрастной порог в Yumisa = 13). Если порог 16+, COPPA в основном про **отрицание** — но требования по biometric data всё равно нужно зеркалить.

### CR-COPPA-2. Согласовать возрастной порог
См. CR-TOS-1. Сейчас COPPA говорит "users aged 16 and older" в §2 — но §3 при этом подразумевает age gate для "под 13". Если решение = 16+ globally, переформулировать §2-§3:
> "Yumisa is designed for users aged 16 and older worldwide. Users under 16 cannot create accounts. We do not knowingly collect personal information from children under 16."

### CR-COPPA-3. Удалить Appmetrica (§6)
См. Risk #1.

### CR-COPPA-4. §6 — Третьи стороны: добавить biometric-aware language
**Особенно для Adjust** (attribution): даже device IDs могут быть PI under COPPA Final Rule. Apple's IDFA и GAID — теперь чувствительны. Добавить конкретно:
> "All third-party SDKs are configured to disable advertising identifiers and behavioural tracking for users under our minimum age. We require contractual COPPA-Safe Harbor commitments from all SDK providers."

### CR-COPPA-5. §8 Safe Harbor — заполнить или удалить
Сейчас: `{IS/IS NOT} a member`. До запуска — определиться. **Рекомендация:** kidSAFE Seal Program (популярный для US-targeted apps) или PRIVO (более premium). Дороже, но даёт actual защиту в случае FTC enquiry. Если **не** членствуете — оставьте секцию, но сформулируйте: "Yumisa is not currently a member of an FTC-approved COPPA Safe Harbor program. We voluntarily comply with COPPA requirements through our internal Privacy Program."

## 🟡 Серьёзные правки

### SR-COPPA-1. §3 Age Gate — добавить anti-circumvention
Если ребёнок ввёл false DOB и прошёл age gate — должен быть mechanism для re-verification (например, через payment method, attestation на milestone events).

### SR-COPPA-2. §5 Parental Rights — детализировать процесс
Сейчас: "contact us at email". Нужно:
- Ясный response SLA (10 рабочих дней)
- Список того, что нужно от родителя (доказательство identity, child's account email/username)
- Mechanism для verified parental ID (challenge questions, government ID upload)

### SR-COPPA-3. §7 App Store declarations — конкретизировать
- Apple: "Age rating: 12+" (приемлемо для health & fitness без medical claims) или "17+" (если есть фото weight/body)
- Google Play: "Content rating: Everyone 10+" (соответствует Health & Fitness category)
- Заполнить плейсхолдеры конкретными значениями.

## 🟢 Улучшения

- Добавить §11 — Process for handling complaints от родителей и регуляторов.
- Краткое FAQ для родителей в простом языке (обязательно по best practice).

---

# 4. GDPR COMPLIANCE — РЕВЬЮ

**Файл:** `gdpr-compliance.md` (133 строки, 12 секций)

## Что есть сейчас
Структурный GDPR-document: data controller, EU rep, lawful bases table, DPAs, data subject rights, security, transfers, children, DPIA, ROPA. Хорошее покрытие, но местами поверхностно.

## ✅ Сильные места
1. **§3 lawful bases table** — отличное прозрачное оформление.
2. **§3 Special Category Data** — правильное использование Art. 9(2)(a) explicit consent.
3. **§5.7 Automated Decision-Making** — пытается обсуждать Art. 22.
4. **§10 DPIA** с risk register — это уровень, до которого многие конкуренты не дошли.
5. **§7 Breach Notification** с 72-часовым SLA — корректно.

## 🔴 Критические правки

### CR-GDPR-1. **Не упомянут EU AI Act**
EU AI Act с transparency obligations effective 2 августа 2026. Yumisa = AI system → попадает в Limited Risk (минимум). Обязательно:
- Раздел "EU AI Act Compliance"
- Категория risk (Limited Risk for food recognition without health diagnoses)
- Обязательства: transparency to users, AI-generated content disclosure, technical documentation
- Если в roadmap появится "AI dietary recommendation" с прямыми health-claims — может triggered High Risk и существенно более жёсткий compliance burden

### CR-GDPR-2. Удалить Appmetrica (§4)
См. Risk #1. Кроме того — **`Germany (Berlin, EU)` placeholder** говорит сам за себя: реальная локация — Россия. Не публиковать.

### CR-GDPR-3. §8 International Transfers — обновить под 2025-2026
Сейчас упомянуты только SCC. На 2025-2026 нужно:
- **EU-US Data Privacy Framework (DPF)** — primary mechanism (validated by EU court Sep 2025, под appeal)
- SCC + supplementary measures как fallback
- Указать конкретные TIA (Transfer Impact Assessments) для US transfers
- UK separately: UK IDTA или Addendum

### CR-GDPR-4. §9 Children's Data — национальные пороги GDPR
Сейчас: "not directed at children under 16 in the EU". Это упрощение. Реальность:
- UK: 13
- Sweden, Denmark, Estonia, Finland, Latvia, Lithuania, Malta, Poland, Portugal, Spain, France: 13-15
- Italy: 14
- Germany, Netherlands: 16
**Правка:** "If your country sets a higher minimum digital age, that age applies. Currently the minimum age to use Yumisa is 16 globally; users under their country's digital age threshold need verifiable parental consent."

### CR-GDPR-5. §5.7 Automated Decision-Making — нужно усилить, не отказываться
Сейчас: "This is not 'automated decision-making' with legal or similarly significant effects". Это **рискованная** позиция:
- EDPB Guidelines (2024 update): "similarly significant effect" интерпретируется широко (включает health-related inferences)
- CCPA ADMT regulations 2026: AI processing health-relevant data = automated decision-making technology
**Правка:** изменить с "не является" на "transparent disclosure":
> "Yumisa uses automated processing (AI) to estimate the nutritional content of food. This processing supports your personal dietary tracking. While we do not believe this constitutes 'automated decision-making producing legal or similarly significant effects' under Art. 22 GDPR, you have the right to (a) request a human review of any specific result, (b) object to the processing, and (c) receive an explanation of how the AI works in plain language."

### CR-GDPR-6. §6 Data Protection by Design — расширить
Сейчас 4 пункта. Добавить:
- **Privacy-by-Default settings:** конкретные defaults (analytics off, marketing off, data sharing minimal, AI training opt-in)
- **Data minimisation:** explicit list какие данные мы НЕ собираем (precise location, contacts, photos beyond food, etc.)
- **Pseudonymisation:** конкретно — как делается для AI training data

## 🟡 Серьёзные правки

### SR-GDPR-1. §1 Data Controller — заполнить placeholders
До запуска. Нужно: legal entity name, address, registration number, DPO name + email. Если стартап мал — DPO может быть external (как у Yazio через lexTM GmbH Frankfurt).

### SR-GDPR-2. §2 EU Representative — обязателен по Art. 27
Если legal entity не в ЕС/ЕЭЗ. Стандартный вариант — назначить external EU rep service (например, EDPO, Prighter, EU-GDPR-Rep). Стоит €500-1500/year. **Не оставлять placeholder.**

### SR-GDPR-3. §10 DPIA — внести конкретику
Сейчас 4 строки в таблице. Real DPIA должен:
- Описывать nature, scope, context, purposes processing
- Necessity & proportionality assessment
- Risks к rights and freedoms (real categorical assessment)
- Mitigation measures + residual risk
**Это внутренний документ, не для public publication, но в GDPR Compliance можно упомянуть, что full DPIA доступна по запросу регулятора.**

### SR-GDPR-4. §3 Marketing emails — fix consent flow
"Explicit opt-in required" — хорошо. Но добавить: "Granular consent (we ask separately for product updates vs. promotional offers)" + double opt-in для EU.

### SR-GDPR-5. UK GDPR — отдельная подсекция
Сейчас всё про EU GDPR. После Brexit UK имеет UK GDPR + DPA 2018 + ICO. Добавить подсекцию: ICO как complaint authority для UK users; UK Representative (требуется по Art. 27 UK GDPR если controller вне UK); UK IDTA для transfers.

## 🟢 Улучшения

- §11 ROPA — добавить, что ROPA структурирована по Art. 30(1) categories.
- §12 Контакты — добавить German DPO contact format (как Yazio: external lawyer via law firm).

## Сравнение с конкурентами

| Аспект | Yumisa | Cal AI | MyFitnessPal | Lifesum | Yazio |
|---|---|---|---|---|---|
| EU AI Act mention | ❌ | ❌ | ❌ | ❌ | ❌ |
| EU Representative named | ❌ placeholder | ❌ | ⚠️ DPA contact | n/a (in EU) | n/a |
| DPF mentioned | ❌ | ❌ | ❌ | ⚠️ | ❌ |
| Art. 9 explicit consent flow | ✅ упоминает | ⚠️ | ⚠️ | ✅ best | ⚠️ |
| Art. 22 ADM honest disclosure | ⚠️ deflects | ⚠️ | ⚠️ | ❌ | ❌ |
| National age threshold awareness | ❌ "16 in EU" | ❌ | ❌ | ✅ "13 or country's age" | ❌ |
| DPIA section | ✅ | ❌ | ❌ | ❌ | ❌ |

---

# СВОДНЫЙ ЧЕК-ЛИСТ "ДО ПУБЛИКАЦИИ"

## Блокирующие (🔴 — нельзя публиковать без этого)
1. ☐ Заменить Appmetrica на EU/US-based product analytics (Mixpanel / Amplitude / Firebase / PostHog)
2. ☐ Утвердить единый возрастной порог (рекомендую 16+ globally) и зеркалировать в 4 документах + UI age-gate
3. ☐ Добавить US State Privacy Rights секцию в Privacy Policy (минимум CA + WA, желательно 14 штатов)
4. ☐ Добавить Washington Health Data Privacy notice (либо отдельным документом, либо явной секцией)
5. ☐ Добавить EU AI Act compliance в GDPR doc (хотя бы short paragraph про Limited Risk + transparency)
6. ☐ Заполнить все critical placeholders: `{LEGAL_ENTITY_NAME}`, `{REGISTERED_ADDRESS}`, `{DPO_*}`, `{EU_REPRESENTATIVE_*}`, `{COUNTRY_OF_INCORPORATION}`, `{GOVERNING_LAW_JURISDICTION}`
7. ☐ Раскрыть конкретных AI-providers (или хотя бы категории + регионы)
8. ☐ Добавить opt-out из AI model training
9. ☐ Усилить AI accuracy disclaimer (±% accuracy claim)
10. ☐ FTC Click-to-Cancel / ROSCA-friendly формулировки в Terms §4

## Важные (🟡 — желательно до публикации, можно через 30-60 дней patch)
11. ☐ Назначить EU Representative (external service ~€500-1500/year)
12. ☐ Подготовить локализацию ключевых документов в DE, FR, ES, IT, PT-BR (соответствует языкам приложения)
13. ☐ DPIA — внутренний документ + ROPA
14. ☐ Кейс EU consumer carve-out в §9 Limitation of Liability
15. ☐ User content license — separate AI training opt-in clause
16. ☐ Configure App Store Privacy Nutrition Label + Google Play Data Safety Form
17. ☐ Решить про Safe Harbor membership (kidSAFE / PRIVO)

## Желательные (🟢 — улучшения для UX/trust)
18. ☐ TOC во всех документах
19. ☐ "Plain English Summary" в начале каждой секции
20. ☐ Public sub-processors page (e.g. yumisa.app/sub-processors с changelog)
21. ☐ Trust Center page (security, certifications, audits)
22. ☐ Отдельный Cookie Policy для website

---

# ПРИОРИТЕТЫ И TIMELINE

**Эта неделя (до 28 апреля):**
- Решить про Appmetrica и replacement
- Утвердить возрастной порог
- Заполнить критические placeholders с командой
- Получить контакт EU Rep service

**Следующие 2 недели (до 12 мая):**
- Финализировать обновлённые версии 4 документов с учётом всех 🔴 правок
- Добавить Washington MHMDA notice + US State Rights
- Локализовать в 5-6 языков (если запуск multi-geo)
- Согласовать с разработкой реализацию opt-out flows (AI training, marketing, ADMT)

**До запуска:**
- App Store Privacy Nutrition Label + Google Play Data Safety
- Подготовить ROPA + DPIA
- Назначить EU Rep
- Sub-processors page

---

# ФИНАЛЬНАЯ ЗАМЕТКА

Эти документы — **не компетенция growth-менеджера в одиночку**. Перед публикацией финальных версий **обязательна** проверка квалифицированным юристом по data protection / consumer law (EU + US минимум). Стоит €1500-5000 за пакет review для seed-stage стартапа. Это не overkill, а must-have для health/wellness app с глобальным запуском.

Альтернатива — privacy-tech платформы (Termly, iubenda, Didomi) генерируют compliance документы с учётом jurisdictions. Качество разное, но дешевле, чем ad-hoc lawyer. Для Yumisa с ограниченным бюджетом ($1K/mo) рекомендую: iubenda Pro (~€150/year) для Privacy + Terms + Cookies + DPA, плюс single legal review (€2-3K) перед запуском.

Сравнение бенчмарков показало: **Cal AI слаб** (потому AI и был куплен MFP — наводит на мысли про due diligence). MyFitnessPal — current standard. Yumisa может стать лучше, если закроет описанные выше гэпы.
