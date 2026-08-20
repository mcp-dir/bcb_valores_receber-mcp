---
name: bcb_valores_receber-mcp
description: Skill da REST API do Banco Central do Brasil (BCB): Valores a Receber na MCP.AI: 1 endpoint em /api/bcb_valores_receber. Banco Central do Brasil (BCB): Valores a Receber, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Banco Central do Brasil (BCB): Valores a Receber — REST API skill

Você tem acesso à **Banco Central do Brasil (BCB): Valores a Receber** REST API na MCP.AI.

> Banco Central do Brasil (BCB): Valores a Receber, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/bcb_valores_receber
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/bcb_valores_receber/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/bcb_valores_receber/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `bcb_valores_receber_consultar`

Banco Central do Brasil (BCB): Valores a Receber, consulta em fonte oficial. _(POST /api/bcb_valores_receber/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `data_nascimento` | string | Não | Parâmetro de consulta "data_nascimento". |
| `data_abertura_empresa` | string | Não | Parâmetro de consulta "data_abertura_empresa". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_bcb_valores_receber` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
