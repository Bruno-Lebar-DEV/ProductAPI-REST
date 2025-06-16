# ProductAPI-REST

**API RESTful desenvolvida em ADVPL para integração com o ERP TOTVS Protheus, focada na gestão de produtos.**

## 📋 Descrição

O **ProductAPI-REST** é um projeto voltado para a criação de uma API moderna e segura em ADVPL, permitindo o cadastro, edição, listagem e exclusão de produtos e seus atributos diretamente no ambiente do Protheus. O projeto segue o estilo RESTful e inclui autenticação via token JWT, retornos padronizados em JSON e logs para rastreabilidade das requisições.

## 🚀 Funcionalidades

- 📦 CRUD completo de produtos  
- 🗂️ Gerenciamento de tipo e complemento de produto  
- 🔐 Autenticação segura via JWT  
- 📄 Retorno estruturado em JSON  
- 📝 Registro detalhado de logs de requisições  
- 🌐 Design orientado para fácil integração com sistemas externos  

## 🔧 Tecnologias e Estrutura

- **ADVPL**  
- **Protheus (Appserver)**  
- **JSON Parser nativo e customizado**  
- **JWT com criptografia customizada (ADVPL puro)**  
- **Organização modular para versionamento e manutenção**

## 📦 Instalação

> Requisitos mínimos:

- Protheus 12.1.33+ com REST habilitado  
- Ambiente com licenciamento para execução de WebServices  
- Tabelas customizadas importadas via SX2/SX3  

**Passos:**

1. Clone este repositório  
2. Copie os fontes `.PRW` para a pasta do Appserver  
3. Compile com TDS ou Appserver diretamente  
4. Registre os endpoints no módulo REST do Protheus  
5. Teste via Postman ou navegador REST Client  

## 🔐 Autenticação

A autenticação é baseada em JWT, enviado via header:

```
Authorization: Bearer <seu_token>
```

Tokens válidos garantem acesso a rotas privadas de criação e atualização de produtos.

## 🧪 Exemplo de Requisição

```http
GET /api/products
Authorization: Bearer abcdefg12345

Response:
{
  "success": true,
  "products": [
    { "codigo": "0001", "descricao": "Produto A" },
    { "codigo": "0002", "descricao": "Produto B" }
  ]
}
```

## 📸 Demonstrações

*(adicione prints das respostas JSON, logs e configuração da API no Protheus)*

## 📑 Licença

Distribuído sob a [Apache License 2.0](./LICENSE).

## 🤝 Contribuições

Contribuições são muito bem-vindas! Relate problemas, envie sugestões ou abra PRs com melhorias.

## 👨‍💻 Autor

Desenvolvido por [Bruno Lebar](https://github.com/Bruno-Lebar-DEV)
