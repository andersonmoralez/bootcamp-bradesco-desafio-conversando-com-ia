[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1wcJEPZuHUb-JcAOuVcWvcR1rouDdcV1K?usp=sharing)

# 🎙️ Multi-Language Voice Assistant: Whisper + Gemini AI
Este projeto consiste em um assistente de voz inteligente capaz de ouvir áudio em diversos idiomas, transcrever o conteúdo, processar a tradução usando modelos de linguagem de última geração (LLMs) e responder vocalmente na linguagem desejada.

Originalmente concebido como um desafio da DIO, este projeto foi evoluído por mim para utilizar o Google Gemini 1.5 Flash, trazendo maior velocidade e eficiência para o pipeline de processamento.

# 🏗️ Arquitetura do Sistema
O fluxo de dados segue quatro etapas principais:

1. Speech-to-Text (STT): Utilização do modelo Whisper (OpenAI) para converter áudio bruto em texto com alta precisão multilíngue.

2. Processamento de Linguagem Natural (NLP): O texto transcrito é enviado ao Google Gemini 1.5 Flash (via API google-genai), onde é processado conforme as instruções de sistema (tradução, resposta ou análise).

3. Text-to-Speech (TTS): A resposta textual da IA é convertida em fala natural utilizando o gTTS (Google Text-to-Speech).

4. Interface de Saída: O arquivo de áudio resultante é reproduzido diretamente no ambiente de execução.

# 🛠️ Tecnologias e Ferramentas
• Linguagem: Python 3.x

• Transcrição: openai-whisper

• Inteligência Artificial: google-genai (Google Gemini 1.5 Flash)

• Síntese de Voz: gTTS

• Ambiente: Google Colab (Integração com userdata para segurança de chaves de API).

# 🛡️ Boas Práticas e Segurança
Diferente de implementações básicas, este projeto foca em segurança de credenciais:

• Segredos do Colab: As chaves de API não estão expostas no código. Elas são gerenciadas via google.colab.userdata, garantindo que o notebook possa ser compartilhado no GitHub sem comprometer a segurança do desenvolvedor.

• Migração de API: O código foi atualizado para as bibliotecas mais recentes (google-genai v1), evitando o uso de métodos depreciados e garantindo a longevidade da solução.

# 🚀 Como Executar
1. Clone este repositório.

2. Abra o arquivo .ipynb no Google Colab.

3. Configure sua GEMINI_API_KEY nos Secrets (ícone de chave) do Colab.

4. Execute as células sequencialmente.

# 📝 Notas do Desenvolvedor
Este projeto demonstra competências em:

• Consumo de APIs REST e SDKs de Inteligência Artificial.

• Manipulação de arquivos de áudio e processamento de strings em Python.

• Configuração de ambientes de desenvolvimento em nuvem.

• Documentação técnica e versionamento de código.
