---
name: ecrvsp_docs_emplacamento-mcp
description: Skill da REST API do ECRVSP Documentos: Primeiro Emplacamento na MCP.AI: 1 endpoint em /api/ecrvsp_docs_emplacamento. ECRVSP Documentos: Primeiro Emplacamento, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# ECRVSP Documentos: Primeiro Emplacamento — REST API skill

Você tem acesso à **ECRVSP Documentos: Primeiro Emplacamento** REST API na MCP.AI.

> ECRVSP Documentos: Primeiro Emplacamento, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/ecrvsp_docs_emplacamento
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
curl -X POST https://api.mcp.ai/api/ecrvsp_docs_emplacamento/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"a3":"...","a3_pin":"...","login_cpf":"...","login_senha":"...","chassi":"...","categoria":"...","tipo_restricao":"...","nfe_data_emissao":"...","nome":"...","nome_anterior":"...","endereco_cep":"...","endereco_numero":"...","veiculo_taxi":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/ecrvsp_docs_emplacamento/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `ecrvsp_docs_emplacamento_consultar`

ECRVSP Documentos: Primeiro Emplacamento, consulta em fonte oficial. _(POST /api/ecrvsp_docs_emplacamento/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `a3` | string | Sim | Parâmetro de consulta "a3". |
| `a3_pin` | string | Sim | Parâmetro de consulta "a3_pin". |
| `login_cpf` | string | Sim | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `placa_escolhida` | string | Não | Parâmetro de consulta "placa_escolhida". |
| `placa_final` | string | Não | Parâmetro de consulta "placa_final". |
| `file_pdf` | string | Não | Parâmetro de consulta "file_pdf". |
| `chassi` | string | Sim | Parâmetro de consulta "chassi". |
| `categoria` | string | Sim | Parâmetro de consulta "categoria". |
| `tipo_restricao` | string | Sim | Parâmetro de consulta "tipo_restricao". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `rg` | string | Não | Parâmetro de consulta "rg". |
| `rg_orgao_expedidor` | string | Não | Parâmetro de consulta "rg_orgao_expedidor". |
| `rg_uf` | string | Não | Parâmetro de consulta "rg_uf". |
| `nfe` | string | Não | Parâmetro de consulta "nfe". |
| `nfe_data_emissao` | string | Sim | Parâmetro de consulta "nfe_data_emissao". |
| `nfe_numero` | string | Não | Parâmetro de consulta "nfe_numero". |
| `nfe_valor` | string | Não | Parâmetro de consulta "nfe_valor". |
| `nome` | string | Sim | Parâmetro de consulta "nome". |
| `nome_anterior` | string | Sim | Parâmetro de consulta "nome_anterior". |
| `telefone` | string | Não | Parâmetro de consulta "telefone". |
| `endereco_cep` | string | Sim | Parâmetro de consulta "endereco_cep". |
| `endereco_numero` | string | Sim | Parâmetro de consulta "endereco_numero". |
| `endereco_complemento` | string | Não | Parâmetro de consulta "endereco_complemento". |
| `veiculo_pessoa_deficiencia` | string | Não | Parâmetro de consulta "veiculo_pessoa_deficiencia". |
| `veiculo_taxi` | string | Sim | Parâmetro de consulta "veiculo_taxi". |
| `veiculo_isencao_fiscal` | string | Não | Parâmetro de consulta "veiculo_isencao_fiscal". |
| `veiculo_venda_dispensada_renave` | string | Não | Parâmetro de consulta "veiculo_venda_dispensada_renave". |
| `veiculo_pessoa_deficiencia_venda_direta` | string | Não | Parâmetro de consulta "veiculo_pessoa_deficiencia_venda_direta". |
| `veiculo_empresa_salvados` | string | Não | Parâmetro de consulta "veiculo_empresa_salvados". |
| `tipo_placa_dianteira` | string | Não | Parâmetro de consulta "tipo_placa_dianteira". |
| `tipo_placa_traseira` | string | Não | Parâmetro de consulta "tipo_placa_traseira". |
| `tipo_placa_traseira_segunda` | string | Não | Parâmetro de consulta "tipo_placa_traseira_segunda". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_ecrvsp_docs_emplacamento` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
