# API para integração dos imóveis da imobiliária

API destinada à consulta de imóveis disponíveis para locação.
Solicitar à Sami as seguintes credenciais de acesso ( *USERNAME, *KEY, *AUTHENTICATION_KEY ).


### **Utilizar**
##### **Header**
```json
Content-Type: application/json
```

##### **Authorization**
```json
Type: Basic Auth
Username: *USERNAME
```

### **Consultar cidades**

URL: https://wapi.samierp.com.br/AUTHENTICATION_KEY/locacao/cidades/

### Exemplo:

```php
{
    "sigla": "KEY",
    "chamadaInterna": true
}
```

### **Consultar bairros**

URL: https://wapi.samierp.com.br/AUTHENTICATION_KEY/locacao/bairros/

### Exemplo:

```php
{
    "sigla": "KEY",
    "chamadaInterna": true,
    "city": "Porto Alegre"
}
```

### **Consultar tipos de imóveis**

URL: https://wapi.samierp.com.br/AUTHENTICATION_KEY/locacao/tiposimovel/

### Exemplo:

```php
{
    "sigla": "KEY",
    "chamadaInterna": true
}
```

### **Consultar fotos do imóvel**

URL: https://wapi.samierp.com.br/AUTHENTICATION_KEY/locacao/fotos/{id_imovel}

### Exemplo:

```php
{
    "sigla": "KEY",
    "chamadaInterna": true
}
```

### **Consultar caracteristicas do imóvel**

URL: https://wapi.samierp.com.br/AUTHENTICATION_KEY/locacao/caracteristicas/{id_imovel}

### Exemplo:

```php
{
    "sigla": "KEY",
    "chamadaInterna": true
}
```


### **Consultar imóvel/imóveis**

##### Todos Imóveis => URL: https://wapi.samierp.com.br/AUTHENTICATION_KEY/locacao/imovel/
##### Único imóvel => URL: https://wapi.samierp.com.br/AUTHENTICATION_KEY/locacao/imovel/{id_imovel}

### Exemplo:

```php
{
    "sigla": "KEY",
    "chamadaInterna": true,
    "properties_per_page": 50, #Imóveis por página
    "current_page": 1, #Pagina atual
    "city": 'Porto Alegre', #Cidade
    "district": ['AUXILIADORA', 'CENTRO'], #Bairros
    "types": ['Apto', 'Casa'], #Tipos de Imóvel
    "bedrooms": 1, #Dormitórios
    "garages": 1, #Garagens
    "bathrooms": 1 #Banheiros
    "suites": 1, #Suítes
    "minimum_value": 50000, #Valor minímo
    "maximum_value": 150000, #Valor máximo
    "minimum_area": 30, #Área miníma
    "maximum_area": 100, #Área máxima
}
```
