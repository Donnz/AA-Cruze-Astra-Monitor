AA Mazda Monitor 0.8.5

**Русский**

- **Экспорт и импорт журнала прожигов**: пункты «Экспорт журнала прожигов» и «Импорт журнала прожигов» в меню «⋮». Формат `L;время;сажа;пробег;состояние` и `I;интервал`, неверные строки пропускаются.
- **Настройки**: убраны лишние линии-разделители в конце разделов в release-сборке (фильтр по типу декорации, а не по имени класса).
- **Мост к данным**: переопределены все методы `ITorqueService.Default`, возвращавшие `null` — теперь отдаются пустые массивы и строки, внешний клиент не падает на `null`.
- **Проверка обновлений**: ошибки сети, ответа GitHub и неразборчивого тега пишутся в журнал (Timber.w).
- **Тесты**: 17 юнит-тестов — разбор ответов адаптера (ELM327), формулы датчиков Mazda, проверка версий/тегов.
- **Релиз**: к выпуску прикладывается только `usage.txt` (что R8 удалил); `mapping.txt` (37 МБ) хранится как артефакт workflow.
- **Версия**: 0.8.5, код версии 8005 — ставится поверх 0.8.4 без удаления.

**English**

- **Regeneration log export and import**: "Export regeneration log" and "Import regeneration log" items in the "⋮" menu. Format `L;time;soot;distance;state` and `I;interval`, invalid lines are skipped.
- **Settings**: stray divider lines at the end of sections in release builds are fixed (decoration filtered by type, not by class name).
- **Data bridge**: all `ITorqueService.Default` methods that returned `null` are now overridden — empty arrays and strings are returned, so external clients do not crash on `null`.
- **Update check**: network, GitHub response and unparseable tag errors are logged (Timber.w).
- **Tests**: 17 unit tests — adapter response parsing (ELM327), Mazda sensor formulas, version/tag checks.
- **Release**: only `usage.txt` is attached to the release (what R8 removed); `mapping.txt` (37 MB) is stored as a workflow artifact.
- **Version**: 0.8.5, version code 8005 — installs over 0.8.4 without uninstalling.