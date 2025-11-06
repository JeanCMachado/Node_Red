#Consulta com Node-RED

Este projeto implementa um serviço simples de consulta de Consultorias e CEP utilizando **Node-RED**.  
A aplicação permite buscar CEPs de duas maneiras:

1. **Via formulário HTML**  
2. **Via URL direta** usando parâmetros de rota

As consultas são realizadas através da **BrasilAPI**, que retorna dados como logradouro, bairro, cidade e estado.

---

## Estrutura do Projeto

O fluxo contém três rotas principais:

### **1. `/cep` – Página inicial**
Exibe um formulário HTML onde o usuário digita um CEP e realiza a busca.

### **2. `/cep/search?cep=xxxxxxx` – Busca via Query String**
Recebe a busca enviada pelo formulário.  
Exemplo:

