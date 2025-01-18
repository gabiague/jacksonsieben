# ESCOLA SUPERIOR POLITÉCNICO SETÚBAL
# Estudantes:
# Jackson Sieben
# Gaston Maio Biaguê,
# Projeto “Reparação de componentes eletrónicos”
# Relatório final 
# Qualidade de Software - Laboratório
# 21 de Janeiro de 21, Setúbal 
## Introdução 
O presente relatório documenta a análise detalhada de um projeto "Reparação de componentes eletrónicos". O trabalho foi conduzido no âmbito do laboratório de Qualidade de Software, com foco na identificação de melhorias na usabilidade, acessibilidade e qualidade geral do aplicativo. 

O objetivo principal do trabalho foi elaborar um relatório completo das tarefas realizadas, descrevendo cada etapa do processo de análise, bem como apresentar conclusões e recomendações baseadas nos resultados obtidos. A análise foi fundamentada em técnicas e conceitos estudados ao longo da unidade curricular, incluindo o desenvolvimento de casos de teste realizado, a aplicação de testes de sistema e aceitação, e a realização de um es tudo de usabilidade e acessibilidade. As tarefas realizadas incluíram familiarização com o projeto, a extração e análise de requisitos, a estruturação de casos de teste.

Com este trabalho, busca-se não apenas identificar os pontos fortes e fracos do projeto, mas também propor melhorias que possam aumentar seu valor para os usuários finais e sua competitividade no mercado. A abordagem adotada reforça a importância de práticas de qualidade de software na construção de soluções tecnológicas que atendam às expectativas dos usuários e das organizações. 

# Requisitos Funcionais – Loja de componentes eletrônicos 
**1. Realizar login com nome de usuário e senha.** 
Permite que os usuários acessem o sistema utilizando suas credenciais de autenticação. 

**2. Realizar login automático ao acessar o sistema.** 
Efetua o login automaticamente se o usuário já tiver uma sessão ativa. 

**3. Visualizar informações de serviços cadastrados.** 
Exibe uma lista detalhada de serviços registrados no sistema. 

**4. Criar usuários com os tipos "Operador" ou "Administrador".** 
Permite o cadastro de novos usuários com níveis de acesso específicos. 

**5. Visualizar a lista de usuários cadastrados.** 
Exibe uma lista completa dos usuários registrados no sistema. 

**6. Editar informações de usuários cadastrados.** 
Permite atualizar dados de usuários, como nome, e-mail e tipo de acesso. 

**7.Excluir usuários cadastrados.** 
Remove permanentemente usuários do sistema. 

**8. Validar a confirmação de senha durante o cadastro de usuários.** 
Garante que a senha informada seja igual à sua confirmação ao criar um usuário. 

**9. Cadastrar usuários com campos obrigatórios.** 
Exige nome, nome de usuário, e-mail, tipo de usuário e senha para registrar um novo usuário. 

**10. Cadastrar clientes com campos obrigatórios.** 
Exige nome, e-mail, morada, código postal e número de contribuinte para registrar um novo cliente. 

**11. Editar informações de clientes cadastrados.** 
Permite atualizar informações de clientes já registrados. 

**12. Visualizar a lista de clientes cadastrados.** 
Exibe uma lista completa de clientes registrados no sistema. 

**13. Excluir clientes cadastrados.** 
Remove permanentemente clientes do sistema. 

**14. Buscar clientes por qualquer parte dos campos cadastrados.** 
Permite pesquisar clientes utilizando qualquer informação relevante de seus registros. 

# Requisitos Não Funcionais 

**1. Desempenho:** 
O sistema deve responder às solicitações de visualização, edição e busca em até 2 segundos para bases de dados pequenas e médias. 
O sistema deve suportar múltiplos acessos simultâneos sem degradação perceptível no desempenho. 

**2. Usabilidade:** 
A interface deve ser intuitiva e de fácil navegação, permitindo que operadores e administradores executem tarefas com o mínimo de treinamento. 
O sistema deve fornecer mensagens de erro claras e orientações para corrigir entradas inválidas. 

**3. Compatibilidade:** 
O sistema deve ser compatível com navegadores modernos e dispositivos de diferentes tamanhos de tela. 
O banco de dados deve ser escalável para suportar um crescimento considerável de registros de usuários, clientes e serviços. 

# Etapas para a Crítica Usando a ISO/IEC 25010:2011 

## 1. Revisão das Características de Qualidade da Norma 

**A norma ISO/IEC 25010:2011 define oito características principais para avaliação de qualidade de software:** 

**1.1. Funcionalidade:**

a. Adequação funcional: O sistema atende aos requisitos funcionais? 

b. Exatidão: Os resultados fornecidos pelo sistema são precisos? 

c. Conformidade funcional: O sistema cumpre regulamentos e padrões aplicáveis? 

**1.2. Desempenho:** 
a. Eficiência em comportamento: Tempo de resposta e utilização de recursos são adequados? 
b. Capacidade: O sistema suporta a carga esperada de usuários e dados? 

**1.3. Compatibilidade:**
a. Coexistência: O sistema funciona bem com outros sistemas? 
b. Interoperabilidade: É capaz de trocar informações com outros sistemas? 

**1.4. Usabilidade:** 
a. Reconhecimento de usabilidade: A interface é intuitiva e fácil de aprender? 
b. Proteção contra erros do usuário: As mensagens de erro e validações ajudam o usuário? 

**1.5. Confiabilidade:**
a. Maturidade: O sistema é estável? 
b. Tolerância a falhas: É resiliente a falhas inesperadas? 
c. Recuperabilidade: Pode se recuperar de falhas sem perda de dados? 

**1.6. Segurança:** 
a. Confidencialidade: Os dados do usuário estão protegidos? 
b. Integridade: Os dados não podem ser alterados sem autorização? 
c. Autenticidade: Apenas usuários autorizados têm acesso ao sistema? 

**1.7. Manutenibilidade:**
a. Modularidade: O código é bem organizado e modular? 
b. Reusabilidade: Componentes podem ser reutilizados? 
c. Analisabilidade: É fácil identificar e corrigir defeitos? 

**1.8. Portabilidade:**
a. Adaptabilidade: O sistema pode ser usado em diferentes plataformas? 
b. Instalabilidade: É fácil de instalar e configurar? 

## 2. Aplicação dos Critérios ao Projeto ## 
Para cada característica relevante, avalie como o sistema se comporta atualmente. Com base nas funcionalidades e requisitos levantados, aqui estão alguns pontos iniciais: 

**2.1. Funcionalidade:** 
a. Adequação funcional: O sistema cobre autenticação, cadastro e gestão de usuários e clientes, e atende os requisitos funcionais básicos. 
b. Sugestão: Verificar se há validação rigorosa para prevenir inconsistências, como duplicidade de registros. 

**2.2. Desempenho:**
a. Eficiência: O requisito não funcional especifica resposta em até 2 segundos para bases pequenas e médias, mas a escalabilidade para grandes volumes não foi claramente mencionada. 
b. Sugestão: Realizar testes de carga e otimizar consultas de busca. 

**2.3. Compatibilidade:**
a. Interoperabilidade: Não há menção à integração com sistemas externos. 
b. Sugestão: Explorar APIs ou padrões de interoperabilidade, caso isso seja necessário. 

**2.4. Usabilidade:** 
a. Reconhecimento de usabilidade: O sistema parece básico, mas mensagens de erro claras são mencionadas. 
b. Sugestão: Realizar testes com usuários para garantir que a interface seja intuitiva. 

**2.5. Confiabilidade:** 
a. Recuperabilidade: Não há menção a backup ou mecanismos de recuperação. 
b. Sugestão: Implementar estratégias de recuperação para evitar perda de dados. 

**2.6. Segurança:**
a. Confidencialidade: A autenticação por senha existe, mas não menciona criptografia de dados. 
b. Sugestão: Implementar criptografia de senhas e reforçar a segurança de sessões. 

**2.7. Manutenibilidade:** 
a. Modularidade: O uso de ferramentas como ESLint sugere que o código está sendo padronizado. 
b. Sugestão: Revisar o código para garantir alta coesão e baixo acoplamento. 

**2.8. Portabilidade:** 
a. Adaptabilidade: O sistema é descrito como compatível com navegadores modernos. 
b. Sugestão: Realizar testes em diferentes dispositivos para garantir que a responsividade está adequada.

## 3. Crítica e Conclusão ##
Com base na análise: 
- Pontos Fortes: 
Funcionalidades básicas bem definidas e alinhadas aos objetivos do sistema. 
Uso de ferramentas para melhoria da qualidade do código. 
Foco em requisitos não funcionais como desempenho e usabilidade. 

- Pontos a Melhorar: 
Segurança: Implementar práticas robustas como criptografia e controle de sessão. 
Desempenho: Realizar testes de carga para escalabilidade. 
Manutenibilidade: Garantir uma arquitetura modular para facilitar futuras melhorias. 
Confiabilidade: Planejar estratégias de backup e recuperação. 
