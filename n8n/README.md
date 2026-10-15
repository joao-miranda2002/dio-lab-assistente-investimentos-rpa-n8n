# 🏦 Assistente de Investimentos Inteligente com RPA, N8N e Google Gemini

> Projeto final do curso de N8N da **DIO (Digital Innovation One)**, focado na orquestração de fluxos automatizados combinando Web Scraping (RPA), automação no N8N e Inteligência Artificial Generativa.

---

## 📌 Sobre o Projeto

Este projeto implementa uma automação completa de ponta a ponta para o setor financeiro:
1. **RPA em Python:** Coleta dados de clientes em uma página web simulada usando BeautifulSoup.
2. **Orquestração com N8N:** Recebe os dados via Webhook, lê uma base de investimentos (`data.csv`) e cruza o perfil do investidor com as opções disponíveis.
3. **IA Generativa (Google Gemini):** Gera recomendações financeiras humanizadas, contextualizadas com o saldo e perfil de cada cliente.

---

## 🛠️ Decisões Técnicas

- Extração com Web Scraping (RPA):
A página de clientes simula um sistema legado sem API pública disponível. Optou-se pelo uso de Python + BeautifulSoup para emular a ação humana de ler a tabela de clientes e formatar as informações em JSON estruturado.

- Comunicação Desacoplada via Webhook:
A integração entre o script Python e o N8N ocorre via requisição HTTP POST. Isso garante que a extração dos dados e a orquestração do fluxo funcionem de maneira independente e escalável.

- Cruzamento de Dados no N8N:
O workflow lê a base de opções de investimento (data.csv) e mapeia as oportunidades adequadas de acordo com a classificação do cliente:

  - Conservador: Renda Fixa e segurança de capital.
  - Moderado: Equilíbrio entre estabilidade e fundos multimercado.
  - Arrojado: Ênfase em Renda Variável e Ações.

- IA Generativa com Google Gemini:
Para cumprir o Desafio Completo, foi integrado o modelo Google Gemini diretamente no N8N.

- Engenharia de Prompt: O prompt foi desenhado para atuar como um consultor financeiro profissional, considerando o nome, saldo e perfil do cliente, garantindo que as recomendações fiquem estritamente restritas aos produtos reais da base do banco.

## 📸 Demonstração e Evidências
- Workflow no N8N
<img width="1635" height="457" alt="image" src="https://github.com/user-attachments/assets/b759769f-f7d0-4f92-a1cd-dc24e3841aee" />


2. Execução do Script Python

<img width="1472" height="226" alt="image" src="https://github.com/user-attachments/assets/efca31eb-e8ee-4b45-9bff-1db47284d181" />


3. Mensagem Gerada pela IA

<img width="688" height="675" alt="image" src="https://github.com/user-attachments/assets/f2809c7b-0ec7-4d5a-93d5-4d30df702ef2" />
