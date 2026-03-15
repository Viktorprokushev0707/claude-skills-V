# claude-skills

Коллекция кастомных скилов для [Claude Code](https://claude.ai/code).

## Что такое скил

Скил — это файл с инструкцией для Claude. Когда вызываешь `/название` в Claude Code, Claude читает эту инструкцию и следует ей пошагово. Удобно для повторяющихся задач.

## Скилы в этом репозитории

| Скил | Что делает |
|------|------------|
| [research-md](./research-md/) | Веб-исследование: ищет страницы, скачивает через markdown.new, сохраняет результат |

## Как установить любой скил

```bash
cp {название}/SKILL.md ~/.claude/commands/{название}.md
```

После этого скил появится как команда `/{название}` в Claude Code.

## Как установить всё сразу

```bash
for skill in */; do
  cp "${skill}SKILL.md" ~/.claude/commands/"${skill%/}.md"
done
```

## Автор

[Viktorprokushev0707](https://github.com/Viktorprokushev0707)
