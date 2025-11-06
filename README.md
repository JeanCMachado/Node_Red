#Consulta com Node-RED

Este projeto implementa um serviço simples de consulta de Corretoras e CEP utilizando **Node-RED**.  
A aplicação permite buscar CEPs de duas maneiras:

1. **Via formulário HTML**  
2. **Via URL direta** usando parâmetros de rota

As consultas são realizadas através da **BrasilAPI**, que retorna dados como logradouro, bairro, cidade e estado.

---

## Estrutura do Projeto

## Corretoras

### **1. `/brokers` - lista com todos as corretoras**
Exibe uma lista com Nome, local e CNPJ das corretoras
http://localhost::1880/brokers

##CEP

### **1. `/cep` – Página inicial**
Exibe um formulário HTML onde o usuário digita um CEP e realiza a busca.
http://localhost:1880/cep

### **2. `/cep/search?cep=xxxxxxx` – Busca via Query String**
Recebe a busca enviada pelo formulário.  
Exemplo: http://localhost:1880/cep/search?cep=30140071

### **3. `/cep/:cep` - Busca diretoo pela URL**
Permite consultar diretamente um CEP pela rota.  
Exemplo: http://localhost:1880/cep/30140071


---

## Tecnologias Utilizadas

- **Node-RED**
- **BrasilAPI** (https://brasilapi.com.br/)
- Templates Mustache (para renderização HTML)
- HTTP In / HTTP Response Nodes
- Function Nodes (JavaScript)

---

## Importando o Fluxo

1. Abra o Node-RED  
2. Clique no menu superior direito  
3. Vá em **Import → Upload file**  
4. Selecione o arquivo: flows.json
5. Clique em **Import**/**Importar** 
6. Clique em **Deploy**/**Implementar**


