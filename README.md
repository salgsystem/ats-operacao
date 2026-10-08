# ats-operacao

Plugin do Claude Code para a operação do ATS. Traz:

- **skills/**: `frontend-design`, `vercel-react-best-practices`, `webapp-testing`.
- **agents/**: 18 agentes (analyst, architect, executor, verifier...) do [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode).
- **.mcp.json**: registra o MCP remoto `salg-admin` (`https://www.salg.club/api/mcp`).

## Instalar

Os agentes dependem do oh-my-claudecode (ferramentas `lsp_*`/`ast_grep_*`, pastas `.omc/`, subagentes `oh-my-claudecode:*`). Adicione o marketplace dele primeiro:

```
/plugin marketplace add Yeachan-Heo/oh-my-claudecode
/plugin marketplace add salgsystem/ats-operacao
/plugin install ats-operacao@ats-operacao
```

O oh-my-claudecode é instalado automaticamente como dependência.

## MCP salg-admin

Na primeira conexão o Claude Code abre o login OAuth do Supabase. Só contas com `profiles.role = 'admin'` conseguem usar as ferramentas. Use `/mcp` para autorizar.

## Licenças

Agentes e skills de terceiros mantêm suas licenças originais. Veja [NOTICE](NOTICE).
