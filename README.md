# psce Claude Code Plugin

Starter Claude Code plugin organized by company departments.

## Structure

```text
.
+-- .claude-plugin/
|   `-- plugin.json
+-- skills/
|   +-- finance-accounting/
|   +-- facilities/
|   +-- general-affairs/
|   +-- hello/
|   +-- hr/
|   +-- production/
|   +-- project-brief/
|   +-- purchasing/
|   +-- safety-management/
|   `-- trade/
`-- README.md
```

## Local Test

From this directory:

```bash
claude --plugin-dir .
```

Then run one of the namespaced skills inside Claude Code:

```text
/psce:hr 신규 입사자 온보딩 체크리스트
/psce:general-affairs 사무실 비품 구매 요청 양식
/psce:facilities 프레스 설비 예방보전 계획
/psce:safety-management 지게차 작업 위험성 평가
/psce:production 주간 생산계획과 불량률 보고
/psce:purchasing 협력사 견적 비교표
/psce:trade 수출 선적서류 체크리스트
/psce:finance-accounting 월마감 체크리스트
```

After editing plugin files in an open Claude Code session, reload them:

```text
/reload-plugins
```

## Marketplace Test

Add this marketplace from GitHub:

```text
/plugin marketplace add RDavid32/psce
```

If a previous failed marketplace entry is cached, remove it first:

```text
/plugin marketplace remove psce-marketplace
/plugin marketplace add RDavid32/psce
```

Then install the plugin:

```text
/plugin install psce@psce-marketplace
```

## Notes

- `.claude-plugin/plugin.json` contains plugin metadata.
- `.claude-plugin/marketplace.json` contains the marketplace catalog.
- `skills/<skill-name>/SKILL.md` defines each skill.
- Skills are namespaced by the plugin name, so `skills/hello` becomes `/psce:hello`.
