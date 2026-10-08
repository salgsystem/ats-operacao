# ats-operacao

Plugin do Claude Code para a operação do ATS. Traz:

- **skills/**: `frontend-design`, `vercel-react-best-practices`, `webapp-testing`.
- **agents/**: 18 agentes (analyst, architect, executor, verifier...) do [oh-my-claudecode](https://github.com/Yeachan-Heo/oh-my-claudecode).
- **.mcp.json**: registra o MCP remoto `salg-admin` (`https://www.salg.club/api/mcp`).

## Instalar

```
/plugin marketplace add salgsystem/ats-operacao
/plugin install ats-operacao@ats-operacao
```

O oh-my-claudecode (v5.6.2, fixada) é instalado automaticamente como dependência: os agentes usam as ferramentas `lsp_*`/`ast_grep_*`, as pastas `.omc/` e as skills `/oh-my-claudecode:*` dele.

Se você já tem o oh-my-claudecode instalado por outro marketplace, desinstale-o antes (`/plugin uninstall oh-my-claudecode@omc`). Duas cópias ativas duplicam os hooks.

## MCP salg-admin

Na primeira conexão o Claude Code abre o login OAuth do Supabase. Só contas com `profiles.role = 'admin'` conseguem usar as ferramentas. Use `/mcp` para autorizar.

## Licenças

Agentes e skills de terceiros mantêm suas licenças originais. Veja [NOTICE](NOTICE).
