# APP-MMN

# FINANCEIRO

### EXTRATO  - GET
**GET|HEAD** - api/financeiro/extrato/{franqueado}
**Retorna:** `json`
```json
{
    "[]"
}
```

### SALDO  - GET
**GET|HEAD** -  api/financeiro/getSaldo
**Retorna:** `json`
```json
{
    "Error"
}
```
 
### SALDO/{franqueado}  - GET
**GET|HEAD** -  api/financeiro/getSaldo/{franqueado}
**Retorna:** `json`
```json
{
    "users_id": 1,
    "rfi_saldo_disponivel": "1000000.00",
    "rfi_debito": "0.00",
    "rfi_saldo_lideranca": "0.00",
    "rfi_debito_saldo_lideranca": "0.00",
    "rfi_teto_mfi": "0.00",
    "rfi_bonus": "0.00",
    "rfi_estorno": "0.00",
    "irf": "0.00000"
}
```

### STATUS SAQUE  - GET
**GET|HEAD** -  api/financeiro/getstatussaque
**Retorna:** `json`
```json
{
    "ERROR - Use of undefined constant MMN_STATUS_SAQUE_PENDENTE - assumed 'MMN_STATUS_SAQUE_PENDENTE'"
}
```

### PAGAMENTOS COM SALDO/{franqueado}  - GET
**GET|HEAD** -  api/financeiro/listpagamentocomsaldo/{franqueado}
**Retorna:** `json`
```json
{
    "[]"
}
```

### LISTA SOLICITAÇÃO/{franqueado}  - GET
**GET|HEAD** -  api/financeiro/listsolicitacao/{franqueado}
**Retorna:** `json`
```json
{
    "[]"
}
```

### PAGAMENTO COM SALDO{fatura}  - PUT
**PUT** -  api/financeiro/pagamentocomsaldo/{fatura}
Envia: `json`
```json
{
    "[]"
}
```

### PAGAMENTO COM SALDO{fatura}  - POST
**POST** -  api/financeiro/solicitacaosaque
Envia: `json`
```json
{
    "???"
}
```

# FRANCHISEE

### DOWNLINES/{franqueado}  - GET
**GET|HEAD** -  api/franchisee/downlines/{franqueado}
**Retorna:** `json`
```json
{
    "ERROR"
}
``` 

### FRANQUEADO/{franqueado} - GET
**GET|HEAD** -  api/franchisee/franqueado/{franqueado}
**Retorna:** `json`
```json
{
    "user": {
        "id": 1,
        "name": "einstein",
        "first_name": "Albert",
        "last_name": "Einstein",
        "email": "albert@mail.com",
        "status_atual": 1,
        "isFranqueado": 1,
        "created_at": "2018-03-15 16:26:00",
        "updated_at": "2018-03-15 16:26:00",
        "isIRF": 1
    },
    "hierarquia": {
        "users_id": 1,
        "hie_lado": 0,
        "hie_indicador": 0,
        "hie_lado_preferencial": 0,
        "hie_pai": null,
        "hie_filho_0": null,
        "hie_filho_1": null,
        "hie_binario": 0,
        "hie_nivel": 0,
        "hie_data_posicionamento": "2018-03-15 16:26:00"
    }
}
```   

### FRANQUEADO PATROCINADOR/{franqueado} - GET
**GET|HEAD** -  api/franchisee/franqueadopatrocinador/{franqueado}
**Retorna:** `json`
```json
{
    "franqueado": {
        "id": 1,
        "name": "einstein",
        "first_name": "Albert",
        "last_name": "Einstein",
        "email": "einstein@mail.com",
        "status_atual": 1,
        "isFranqueado": 1,
        "created_at": "2018-03-15 16:26:00",
        "updated_at": "2018-03-15 16:26:00",
        "isIRF": 1
    },
    "patrocinador": false
}
```

### isFRANQUEADO/{franqueado} - GET
**GET|HEAD** -  api/franchisee/isfranqueado/{franqueado}
**Retorna:** `json`
```json
{
    "isFranqueado": true
}
```

### PLANO DE CARREIRA/{franqueado} - GET
**GET|HEAD** -  api/franchisee/planodecarreira/{franqueado}
**Retorna:** `json`
```json
{
    "titulosID": 1,
    "tit_nome": "Iniciante",
    "tit_inicio_pontos": 0,
    "proxNome": "Silver",
    "tit_fim_pontos": 5000,
    "proxTituloID": 2,
    "tit_imagem": "naoqualificado.png",
    "prox_tit_imagem": "prata.png",
    "ebi_pontos_acumulados": "0.00"
}
```

### SHOW/{franqueado} - GET
**GET|HEAD** -  api/franchisee/show/{franqueado}
**Retorna:** `json`
```json
{
    "id": 1,
    "name": "einstein",
    "first_name": "ALbert",
    "last_name": "Eintein",
    "email": "einstein@mail.com",
    "status_atual": 1,
    "isFranqueado": 1,
    "created_at": "2018-03-15 16:26:00",
    "updated_at": "2018-03-15 16:26:00",
    "isIRF": 1
}
```

### STORE - POST
**POST** -  api/franchisee/store
Envia: `json`
```json
{
    "???"
}
```

# REDE

### SHOW/{franqueado} - GET
**GET|HEAD** -  api/hierarquia/{franqueado}
Envia: `json`
```json
{
    "users_id": 1,
    "hie_lado": 0,
    "hie_indicador": 0,
    "hie_lado_preferencial": 0,
    "hie_pai": null,
    "hie_filho_0": null,
    "hie_filho_1": null,
    "hie_binario": 0,
    "hie_nivel": 0,
    "hie_data_posicionamento": "2018-03-15 16:26:00"
}
```

### STATUS INDICADOR/{franqueado} - GET
**GET|HEAD** -  api/indicador/getStatusIndicacao/{id}
Envia: `json`
```json
{
    "response": "Patrocinador apto para indicar novos franqueados!",
    "id": 1,
    "name": "vagner",
    "status": true
}
```

### INDICADOR/{name} - GET
**GET|HEAD** -  api/indicador/{name}
Envia: `json`
```json
{
    "404"
}
```

# ORDER

**GET|HEAD** - api/order/cadpendente/{patrocinador}

### PEDIDO/{pedido} - GET
**GET|HEAD** - api/order/getpedido/{pedido}
```json
{
    "???"
}
```

### PEDIDO TIPO/{tipo} - GET
**GET|HEAD** - api/order/getpedidotipofranqueado/{tipo}
```json
{
    "404"
}
```

### PEDIDO TIPO/{tipo}/{franqueado} - GET
**GET|HEAD** - api/order/getpedidotipofranqueado/{tipo}/{franqueado}
```json
{
    "404"
}
```

### LISTA FRANQUEADO/{name} - GET
**GET|HEAD** - api/order/listfranqueado/{franqueado}
```json
{
    "Nenhum pedido encontrado!"
}
```

### INDICADOR/{franqueado} - GET
**GET|HEAD** - api/order/listvendasfranqueado/{franqueado}
```json
{
    "Nenhuma venda realizada!"
}
```

### INDICADOR/{pedido} - GET
**GET|HEAD** - api/order/showitens/{pedido}
```json
{
    "404"
}
```

### STORE - POST
**POST**     | api/order/store
```json
{
    itens_pedido: {
        {
            produto_id: INT,
            produto_qnt: INT
        },
        {
            produto_id: INT,
            produto_qnt: INT
        }
    }
}
```

### STORE - PUT
**PUT**     | api/order/update/{pedido_id}/{status}
```json
{
    "???"
}
```

# UNILEVEL

### UNILEVEL/{franqueado} - GET
**GET|HEAD** - api/pontuacao/unilevel/{franqueado}
```json
{
    "pontos": [],
    "resumo": {
        "users_id": 1,
        "ebi_ultimate": 0,
        "ebi_pontos_esquerda": "0.00",
        "ebi_pontos_direita": "0.00",
        "ebi_pontos_acumulados": "0.00",
        "ebi_porcentagem": "50.00",
        "ebi_status": 2
    },
    "status": [
        "Pendente de posicionamento",
        "Ativo",
        "Inativo",
        3,
        4,
        5
    ]
}
```
### LISTA PRODUTOS - GET
**GET|HEAD** - api/products/list
```json
{
    
{id: 1, produto__tipos_id: 1, nome: "DigiPartner", descricao: "Pacote de ativação", valor: "50.00",…}
1
:
{id: 2, produto__tipos_id: 2, nome: "DigiHash", descricao: "8 MH/s Poder de mineração",…}
2
:
{id: 3, produto__tipos_id: 2, nome: "DigiHash", descricao: "21 MH/s Poder de mineração",…}
3
:
{id: 4, produto__tipos_id: 2, nome: "DigiHash", descricao: "39 MH/s Poder de mineração",…}
4
:
{id: 5, produto__tipos_id: 2, nome: "DigiHash", descricao: "79 MH/s Poder de mineração",…}
5
:
{id: 6, produto__tipos_id: 2, nome: "DigiHash", descricao: "263 MH/s Poder de mineração",…}
}
```
### INDICADOR/{pedido} - GET
**GET|HEAD** - api/senhaFinanceira/{senha}
```json
{
 "???"
}
```

### STORE - PUT
**PUT**     | api/updatesenhafinanceira
```json
{
    "???"
}
