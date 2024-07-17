# bradesco-case
Repositório para disponibilizar arquivos do case apresentado em entrevista para o Bradesco.

## Questões

### 1. Desenho da arquitetura está na imagem "Case - Bradesco.drawio.png"
### 2. Componentes
   1. API Gateway - Gateway para exposição dos endpoints.
   2. Checkout Service - Serviço para controle dos pagamentos (checkouts)
   3. Sistema PIX - Sistema externo de onde iremos buscar o QRCode
   4. DB - SGBD utilizado para armazenar as informações
### 3. Descrição da implemtação
   1. Checkout Service seria desenvolvido com a linguagem Java + Spring Boot;
   2. Spring Data para acesso ao SGBD;
   3. Checkout Service seria divido entre Controlador (PaymentController), Serviço (PaymentService) e Repositório (PaymentRepository)
   4. Pagamento (Payment) é uma entidade (Model) a ser armazenada no banco de dados (Spring Data)
   5. Testes unitários para garantir pleno funcionamento da classe de Serviço, bem como de possíveis classes utilitárias (jUnit); 
   6. Testes de Integração para garantir que os endpoints estão em pleno funcionamento (Spring Test)
   7. Endpoints disponiveis seriam um POST (para checkout via pix) e outro POST (para atualização do status do pagamento)
   8. Autenticação seria feita no Gateway.