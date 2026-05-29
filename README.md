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

<img width="1459" height="510" alt="image" src="https://github.com/user-attachments/assets/2f774d0c-3bc1-42c8-80ff-2d0642b3a11c" />

🔴 Teste 2 — Pipeline com SQL Injection detectado pelo CodeQL
Aqui eu adicionei um código vulnerável de propósito.
O CodeQL identificou o problema e bloqueou a pipeline imediatamente.

<img width="1459" height="368" alt="image" src="https://github.com/user-attachments/assets/641e41b3-daec-4281-a768-4a2d3467df12" />


🟢 Teste 3 — Pipeline com erro e funcionando
Após corrigir a vulnerabilidade, a pipeline voltou a rodar com sucesso.
<img width="1459" height="481" alt="image" src="https://github.com/user-attachments/assets/f5a048b8-c061-4a3a-8813-e0576cfcfd70" />

<img width="1459" height="368" alt="image" src="https://github.com/user-attachments/assets/4a01782d-8bd0-4e6f-bff8-1ead07872432" />


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
