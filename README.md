# 🌍 TurismoAI

Um assistente de viagens inteligente powered by IA que fornece informações personalizadas sobre destinos, cultura, culinária e muito mais.

## 📋 Sobre o Projeto

TurismoAI é um chatbot especializado em turismo que utiliza o poder da Inteligência Artificial para classificar automaticamente a intenção do usuário e fornecer respostas contextualizadas através de diferentes "personas" especializadas, como guia turístico, chef gastronômico, meteorologista, historiador e poliglota.

O sistema funciona em duas etapas:
1. **Classificação de Intenção**: Identifica o que o usuário realmente precisa
2. **Resposta Personalizada**: Gera uma resposta especializada baseada na intenção detectada

## ✨ Funcionalidades

O sistema reconhece e responde a 7 tipos diferentes de intenções:

| Intenção | Descrição | Exemplo de Pergunta |
|----------|-----------|---------------------|
| 🗺️ **Guia de Viagem** | Cria roteiros detalhados dia a dia com logística, horários e custos estimados | "Crie um roteiro de 5 dias para Paris" |
| 🎯 **Ideia de Local** | Sugere 3 destinos personalizados baseados no perfil do usuário | "Onde posso viajar em julho com orçamento de R$ 5000?" |
| 💡 **Dicas de Viagem** | Fornece dicas práticas de segurança, economia e etiqueta local | "Dicas para viajar sozinho pela primeira vez" |
| 🍽️ **Culinária** | Descreve pratos típicos, ingredientes e onde encontrar comida autêntica | "Quais os pratos típicos do Japão?" |
| ☀️ **Clima** | Analisa variações climáticas e recomenda o que levar na mala | "Como é o clima em Londres em dezembro?" |
| 🏛️ **Cultura** | Explica tradições, comportamentos sociais e ajuda a evitar gafes culturais | "Quais os costumes que devo conhecer na Índia?" |
| 🗣️ **Idioma** | Lista frases essenciais com guia de pronúncia simplificado | "Frases essenciais em italiano para turistas" |

## 🚀 Tecnologias Utilizadas

- ![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white) **Python 3.8+**
- ![LangChain](https://img.shields.io/badge/LangChain-Framework-green) **LangChain** - Framework para desenvolvimento com LLMs
- ![Google](https://img.shields.io/badge/Google-Gemini_2.5_Flash-4285F4?style=flat&logo=google&logoColor=white) **Gemini 2.5 Flash** - Modelo de linguagem da Google
- **python-dotenv** - Gerenciamento seguro de variáveis de ambiente
- **rich** - Formatação aprimorada de texto no terminal

## 📦 Instalação

### Pré-requisitos

- Python 3.8 ou superior
- Conta Google Cloud com acesso à API Gemini
- pip (gerenciador de pacotes Python)

### Passo a Passo

1. **Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/turismo-ai.git
cd turismo-ai
```

2. **Crie um ambiente virtual (recomendado):**
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

3. **Instale as dependências:**
```bash
pip install langchain langchain-google-genai python-dotenv rich
```

4. **Configure as variáveis de ambiente:**
   
   Crie um arquivo `.env` na raiz do projeto:
   ```bash
   touch .env  # Linux/Mac
   type nul > .env  # Windows
   ```
   
   Adicione sua chave de API do Google:
   ```env
   GOOGLE_API_KEY=sua_chave_api_aqui
   ```

   > **Como obter a chave API:**
   > 1. Acesse [Google AI Studio](https://makersuite.google.com/app/apikey)
   > 2. Faça login com sua conta Google
   > 3. Clique em "Create API Key"
   > 4. Copie a chave gerada

## 🎮 Como Usar

1. **Execute o script principal:**
```bash
python project.py
```

2. **Faça suas perguntas:**
   - Digite sua pergunta sobre viagens
   - Aguarde a resposta personalizada da IA
   - Continue a conversa ou digite `Q` para sair

### 📝 Exemplos de Perguntas

**Guia de Viagem:**
```
"Crie um guia de viagem de 5 dias para Paris"
"Roteiro de 3 dias em Roma"
```

**Ideias de Destinos:**
```
"Quais destinos você recomenda para lua de mel?"
"Lugares baratos para viajar em julho"
```

**Culinária:**
```
"Quais são os pratos típicos do Japão?"
"Onde comer paella autêntica em Barcelona?"
```

**Clima:**
```
"Como é o clima em Londres em dezembro?"
"O que levar na mala para Nova York em inverno?"
```

**Idioma:**
```
"Quais frases essenciais devo saber para viajar para a Espanha?"
"Ensine frases básicas em tailandês para turistas"
```

**Dicas de Viagem:**
```
"Me dê dicas de segurança para viajar sozinho"
"Como economizar em viagens internacionais?"
```

**Cultura:**
```
"Explique a cultura e costumes da Tailândia"
"Quais comportamentos evitar no Japão?"
```

## 🏗️ Estrutura do Projeto

```
turismo-ai/
│
├── turismo_ai.py          # Script principal com toda a lógica
├── .env                   # Variáveis de ambiente (não commitado)
├── .env.example           # Exemplo de configuração
├── .gitignore            # Arquivos ignorados pelo git
├── README.md             # Documentação do projeto
└── requirements.txt      # Dependências do projeto
```

### 🔧 Principais Funções

```python
cria_linha(tamanho)
```
Cria separadores visuais no terminal para melhor organização da interface.

```python
classifica_intencao(pergunta_do_usuario)
```
Utiliza IA para identificar a intenção por trás da pergunta do usuário, classificando em uma das 7 categorias disponíveis.

```python
responde_com_base_na_intencao(intencao, pergunta_do_usuario)
```
Gera respostas personalizadas baseadas na intenção detectada, utilizando prompts específicos para cada tipo de consulta.

## 🎯 Como Funciona

1. **Entrada do Usuário**: O usuário faz uma pergunta sobre viagem
2. **Classificação**: A IA analisa a pergunta e identifica a intenção
3. **Seleção de Persona**: O sistema escolhe a "persona" especializada adequada
4. **Geração de Resposta**: A IA gera uma resposta contextualizada e detalhada
5. **Exibição**: A resposta é formatada e exibida no terminal

## 🔒 Segurança

⚠️ **Importante:**
- **NUNCA** commite o arquivo `.env` com suas chaves de API
- Adicione `.env` ao seu `.gitignore`
- Mantenha suas credenciais seguras e privadas
- Use variáveis de ambiente para todas as informações sensíveis

**Arquivo `.gitignore` recomendado:**
```gitignore
# Environment variables
.env

# Python
__pycache__/
*.py[cod]
*$py.class
venv/
env/

# IDE
.vscode/
.idea/
*.swp
```

### 💡 Ideias para Contribuição

- Adicionar novas intenções de viagem
- Melhorar os prompts existentes
- Criar testes automatizados
- Adicionar suporte a outros idiomas
- Implementar cache de respostas

## 📈 Roadmap - Melhorias Futuras

- [ ] Interface web com Streamlit ou Gradio
- [ ] Suporte a múltiplos idiomas (inglês, espanhol)
- [ ] Integração com APIs de clima em tempo real
- [ ] Integração com APIs de cotação de moedas
- [ ] Sistema de cache para respostas frequentes
- [ ] Histórico de conversas persistente
- [ ] Exportação de roteiros em PDF
- [ ] Suporte a imagens de destinos
- [ ] Modo offline com respostas pré-carregadas
- [ ] Sistema de feedback do usuário

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👤 Autor

**Seu Nome**
- GitHub: [@VictorSena](https://github.com/VictorSena88)

## 🙏 Agradecimentos

- [LangChain](https://langchain.com/) pela excelente framework
- [Google](https://ai.google.dev/) pelo acesso ao Gemini
- Comunidade Python pelo suporte contínuo

---

⭐ Se este projeto foi útil para você, considere dar uma estrela!

**Feito com ❤️ e ☕**
