# **Desafio da DIO -Construindo esquema conceitual de uma Oficina mecanica**
### **Nome: Sistema de Controle e Gerenciamento de Ordens de Serviço – Oficina Mecânica**  

## **Descrição do Projeto**  
Este projeto apresenta um **Modelo Entidade-Relacionamento Aprimorado (MER)** para um sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica. O objetivo é estruturar um banco de dados eficiente, garantindo o registro adequado das interações entre clientes, veículos, equipes de mecânicos, ordens de serviço e serviços realizados.  

O diagrama foi desenvolvido com base em uma **narrativa fornecida pela instrutora juliana da Digital inovatio one(DIO)**, para o conprimento do **desafio de projeto "Construindo um esquema conceitual para banco de dados"** que faz parte do **bootcamp Heineken - Inteligência Artificial Aplicada a Dados com Copilot** ofertado pela DIO.

---

## **Contextualização do Modelo**  

O sistema gerencia as atividades da oficina mecânica, permitindo que os clientes levem seus veículos para **consertos ou revisões periódicas**. A oficina organiza o fluxo de trabalho da seguinte maneira:  

1. **Cadastro de Clientes e Veículos**  
   - Cada cliente pode possuir vários veículos, mas um veículo pertence a apenas um cliente.  

2. **Atribuição de Equipes de Mecânicos**  
   - Quando um veículo chega à oficina, ele é **designado a uma equipe de mecânicos**, que será responsável por avaliar o problema, preencher a ordem de serviço (OS) e executar o reparo.  

3. **Registro de Ordens de Serviço (OS)**  
   - A OS contém informações como número, data de emissão, status, data prevista de conclusão e valor total.  

4. **Serviços e Mão de Obra**  
   - Os serviços executados na OS são baseados em uma tabela de referência de mão de obra, garantindo que o valor de cada serviço seja calculado corretamente.  

5. **Peças Utilizados**  
   - Se necessário, peças utilizadas no serviço são registradas para compor o valor final da OS.  

---

## **Estrutura do Modelo**  

### **Entidades e Relacionamentos**  
O modelo foi estruturado com as seguintes entidades:  

- **Cliente** → Possui dados cadastrais e pode ter vários veículos.  
- **Veículo** → Vinculado a um único cliente e pode passar por várias OS ao longo do tempo.  
- **Equipe** → Responsável por avaliar e consertar os veículos.  
- **Mecânico** → Cada mecânico pertence a uma equipe específica.  
- **Ordem de Serviço (OS)** → Registro principal dos serviços executados, vinculado ao veículo e à equipe responsável.  
- **Serviço** → Contém a descrição e o preço da mão de obra aplicada na OS.  
- **Peça** → Caso a oficina registre peças individualmente, elas são vinculadas à OS.  

---

## **Entrega**  

### **Arquivos no Repositório**  
1. **Diagrama (PNG/PDF)** → Contém o modelo final do MER.  
2. **README.md** (este arquivo) → Explicação do contexto, estrutura e funcionamento do modelo.  
