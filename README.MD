# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Pipeline de Análise Integrada de Dados Cardiológicos (Numéricos, Textuais e Visuais)

## Grupo: Data Health Solutions

## 👨‍🎓 Integrantes: 

- <a href="https://www.linkedin.com/in/gabriel-oliveira-b6353a16b/">Gabriel Oliveira dos Santos</a>
- <a href="https://www.linkedin.com/in/arthur-bruttel-7171b8381">Arthur Bruttel Nascimento</a>
- <a href="https://www.linkedin.com/in/jonviotti/">Jonatan Viotti Rodrigues da Silva</a>
- <a href="https://www.linkedin.com/in/eusamuelrocha/">Samuel Nicolas Oliveira Rocha</a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/in/leonardoorabona/">Leonardo Ruiz Orabona</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/company/inova-fusca">André Godoi Chiovato</a>

## 📜 Descrição do Projeto

Este projeto acadêmico foi desenvolvido para estruturar, organizar e fundamentar um pipeline de Inteligência Artificial voltado à saúde cardiovascular. O escopo do projeto contempla a integração de três pilares fundamentais de dados essenciais para o aprendizado de máquina e sistemas de suporte à decisão clínica:

1. **Dados Numéricos / Tabulares:** Dataset estruturado contendo variáveis clínicas de pacientes (pressão arterial, colesterol, frequência cardíaca, sintomas e histórico cardíaco).
2. **Dados Textuais (NLP):** Documentos e diretrizes médicas em texto plano abordando saúde cardiovascular, protocolos de emergência e fatores de risco clínicos.
3. **Dados Visuais (Visão Computacional):** Coleção de exames cardiológicos visuais (traçados de eletrocardiogramas - ECGs) para detecção de padrões e anomalias.

O repositório organiza esses ativos de forma padronizada, fornecendo os links públicos de acesso à nuvem e a documentação técnica justificando a relevância de cada modalidade de dados para projetos de IA aplicada à saúde.

## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>assets</b>: elementos visuais do repositório (logos, imagens explicativas e screenshots).
- <b>docs</b>: diretório contendo os textos médicos e diretrizes em formato `.txt` utilizados na Parte 2 (NLP).
- <b>README.md</b>: guia e explicação geral sobre o projeto (o arquivo que você está lendo agora).

---

## 🔬 Partes do Projeto e Fontes de Dados

### Parte 1 – Dados Numéricos (Tabulares / IoT)
* **Descrição:** Dataset estruturado contendo 918 linhas e 12 variáveis clínicas (idade, sexo, tipo de dor no peito, pressão arterial em repouso, colesterol sérico, glicemia de jejum, ECG de repouso, frequência cardíaca máxima e diagnóstico de doença cardíaca).
* **Origem dos Dados:** Base de dados real consolidada e disponibilizada publicamente através do Kaggle (*Heart Failure Prediction Dataset*), combinando 5 estudos clínicos internacionais (Cleveland, Hungria, Suíça, Long Beach e Statlog).
* **Hospedagem Externa:** O conjunto de dados (`heart.csv`) está hospedado publicamente na nuvem através do link.
  * 👉 **[Dataset Numérico > (Google Drive)](https://drive.google.com/file/d/1NZifpKE5M525iM2nFak5ORHhh6r4t69U/view?usp=sharing)**
* **Relevância Clínica para Inteligência Artificial:**
  * **Variáveis Críticas (`RestingBP`, `Cholesterol`, `MaxHR`, `ChestPainType`):** Permitem que modelos preditivos (como árvores de decisão, XGBoost ou redes neurais densas) calculem o escore de risco cardiovascular e identifiquem correlações precoces entre disfunções metabólicas e obstruções coronarianas.
  * **Redução de Erros Médicos:** Auxilia sistemas de suporte à decisão clínica a priorizar pacientes de alto risco em filas de atendimento médico.

---

### Parte 2 – Dados Textuais (Processamento de Linguagem Natural - NLP)
* **Descrição:** Arquivos em formato `.txt` contendo trechos essenciais extraídos de diretrizes cardiológicas oficiais da Sociedade Brasileira de Cardiologia (SBC).
* **Arquivos na Subpasta `docs/`:**
  * 📄 **[`diretriz_dor_toracica.txt`](docs/diretriz_dor_toracica.txt)** – Orientações de triagem, tempo porta-ECG e rotas de investigação para dor torácica.
  * 📄 **[`diretriz_hipertensao.txt`](docs/diretriz_hipertensao.txt)** – Critérios diagnósticos, epidemiologia e fatores de risco da hipertensão arterial.
* **Exploração por Algoritmos de NLP:**
  * **Reconhecimento de Entidades Nomeadas (Clinical NER):** Utilização de modelos baseados em *Transformers* (*BioBERT* / *ClinicalBERT*) para extração automática de termos médicos, sintomas, patologias e classes terapêuticas.
  * **Classificação e Sumarização de Protocolos:** Categorização de prontuários em texto livre e cruzamento automatizado com diretrizes para auditoria de condutas médicas.
* **Relevância para a IA na Saúde:** Cerca de 80% das informações hospitalares estão em formato de texto livre em prontuários. O PLN permite estruturar esses dados não estruturados, agilizando triagens em prontos-socorros e garantindo adesão à medicina baseada em evidências.

---

### Parte 3 – Dados Visuais (Visão Computacional - VC)
* **Descrição:** Lote contendo mais de 100 imagens de exames cardiológicos do tipo eletrocardiograma (ECG) em formatos `.jpg`/`.png`.
* **Origem dos Dados:** Repositório público do Kaggle (*ECG Image Dataset* / *ECG Images* de exames digitalizados e classificados).
* **Hospedagem Externa:** As imagens organizadas por categorias de diagnóstico encontram-se hospedadas na nuvem através do link.
  * 👉 **[ECG Images > (Google Drive)](https://drive.google.com/drive/folders/1dWTdmmGs0Cs2CPYPeo8aKjwvhpZpa6-J?usp=sharing)**
* **Exploração por Algoritmos de Visão Computacional:**
  * **Detecção de Padrões e Segmentação de Ondas:** Redes Neurais Convolucionais (CNNs) e arquiteturas de visão profunda podem ser treinadas para segmentar os complexos do ECG (ondas P, QRS, T) e medir intervalos temporais de forma automatizada.
  * **Reconhecimento de Anomalias:** Identificação visual de sinais precoces de infarto (como o supradesnivelamento do segmento ST) e classificação de arritmias cardíacas.
* **Relevância para a IA na Saúde:** A análise visual automatizada de exames complementares reduz o tempo de resposta em ambientes críticos de emergência médica, auxiliando na triagem instantânea de traçados eletrocardiográficos complexos.

---

## 🔧 Como Executar e Validar o Repositório

### Pré-requisitos
- Python 3.8 ou superior
- Git para clonagem do repositório

### Clonagem e Organização
```
git clone <url-do-repositorio-github>
cd projeto-cardio-ia
```


## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>

