Pipeline CI/CD com CodeQL – Trabalho Final FATEC
Este repositório faz parte do Trabalho Final da disciplina Desenvolvimento de Sistemas / Segurança da Informação, orientado pelo professor Idirley Soares.
Aqui eu construí uma pipeline CI/CD completa, com foco em segurança, testes e deploy automatizado — tudo rodando dentro do GitHub Actions.

A ideia é garantir que cada mudança no código seja analisada, testada e validada automaticamente, evitando que vulnerabilidades ou erros cheguem ao ambiente de deploy.

📁 Estrutura do Projeto
Código
SEU-REPOSITORIO/
├── .github/
│ ├── workflows/
│ │ └── ci-cd-pipeline.yml
│ └── codeql-config.yml
├── main.py
├── requirements.txt
├── tests/
│ └── test_main.py
└── README.md
🛠️ Tecnologias Utilizadas
Python 3.11

GitHub Actions

CodeQL (GitHub Advanced Security)

Pytest

Flake8

Essas ferramentas juntas permitem automatizar segurança, qualidade e deploy — tudo sem precisar clicar em nada.

🔄 Como a Pipeline Funciona
A pipeline é dividida em 3 etapas, que sempre rodam na mesma ordem:

🔒 Análise de Segurança (CodeQL)
Verifica o código em busca de vulnerabilidades, como SQL Injection, uso inseguro de funções, etc.

🧪 Testes Automatizados (pytest + flake8)
Garante que o código funciona e segue boas práticas.

🚀 Deploy para Stage
Simula o deploy da aplicação em um ambiente controlado.

Se qualquer etapa falhar, as próximas não executam — exatamente como uma pipeline profissional deve funcionar.

🧪 Evidências da Pipeline
Abaixo estão os prints que comprovam o funcionamento da pipeline nos três cenários exigidos pelo professor.

🟢 Teste 1 — Pipeline com código seguro
Pipeline rodando normalmente, sem vulnerabilidades e com todos os testes passando.

<img width="795" height="227" alt="image" src="https://github.com/user-attachments/assets/b4762477-2e74-40a0-9309-13b2f8e06f07" />

<img width="802" height="272" alt="image" src="https://github.com/user-attachments/assets/1f9481bb-56c7-476f-b728-49fc54286ba1" />




🔴 Teste 2 — Pipeline com SQL Injection detectado pelo CodeQL
Aqui eu adicionei um código vulnerável de propósito.
O CodeQL identificou o problema e bloqueou a pipeline imediatamente.
<img width="1287" height="370" alt="image" src="https://github.com/user-attachments/assets/024ecdf7-72b8-42df-b4c2-85dc9c7498e7" />


🟢 Teste 3 — Pipeline corrigida e funcionando
Após corrigir a vulnerabilidade, a pipeline voltou a rodar com sucesso.

<img width="944" height="238" alt="1 tela com pipeline funcionando pos erro" src="https://github.com/user-attachments/assets/a6df25e8-1543-4a68-bcaa-41a654a535c8" />

📦 Como rodar o projeto localmente
Se quiser testar tudo no seu computador:

bash
pip install -r requirements.txt
pytest -v
flake8 .
📬 Entrega
Repositório público enviado conforme solicitado pelo professor.

🎉 Conclusão
Este projeto demonstra:

Automação completa com CI/CD

Análise de segurança com CodeQL

Testes automatizados funcionando

Deploy controlado por ambiente

Carolina Cancio Silveira Kolle Fatec Santana de Parnaiba
