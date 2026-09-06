# Русский Тренажёр

A single-file Russian speaking trainer. Open `index.html` in any browser — no build, no server, no dependencies beyond Google Fonts.

Built for an A1-entry learner whose goal is **speaking with real people**, at 45–60 minutes a day.

## Modules

| # | Module | What it trains |
|---|--------|----------------|
| 01 | Сегодня | The 60-minute session plan, daily objective, persistent checklist |
| 02 | Декодер | Cyrillic reading reflex — timed cognate recognition, measures ms/word |
| 03 | Карточки | SM-2 spaced repetition over 112 sentence cards, three directions (RU→EN, EN→RU, audio→meaning) |
| 04 | Шаблоны | Twelve sentence frames that generate hundreds of sentences each |
| 05 | Глаголы | Typed conjugation drill, 22 verbs × 6 persons, with the full table |
| 06 | Падежи | Case production drill with a reason given for every answer |
| 07 | Диалоги | Five dialogues with per-line TTS, blurred translations, whole-dialogue playback for shadowing |
| 08 | Спринт | 60-second timed drills: translation, rapid response, recall |
| 09 | Ошибки | Error log derived from your own misses — weakest topics, leech cards |
| 10 | Курс | A0→C1 roadmap with exit tests and immersion ratios |

## Design notes

- **Cards are sentences, never isolated words.** You never need `время` alone; you need `У меня́ нет вре́мени`.
- **Stress marks everywhere** (`молоко́`) — stress is the loudest accent marker in Russian.
- **Answer checking is forgiving of stress marks and ё/е**, strict on letters. Near-misses (Levenshtein ≤ ~12% of length) are marked "почти" rather than wrong.
- **Audio** uses the browser's `speechSynthesis` with a `ru-RU` voice. If none is installed the app says so and stays text-only.
- **All progress is in `localStorage`**, keyed `ru-trainer-v1`, wrapped in try/catch so private windows degrade instead of breaking.

## Keyboard

- `Space` — reveal card
- `1` `2` `3` `4` — grade Again / Hard / Good / Easy
- `Enter` — submit a typed answer
