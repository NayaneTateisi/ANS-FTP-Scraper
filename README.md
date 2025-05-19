# 🏥 ANS FTP Scraper

Este projeto tem como objetivo **automatizar o processo de extração dos arquivos `.zip` disponibilizados no FTP da ANS (Agência Nacional de Saúde Suplementar)**. 
A ANS fornece esses arquivos de forma **individual**, o que torna o download manual extremamente **moroso e ineficiente**, especialmente quando se trata de grandes volumes de dados.

Com este script, você consegue:

- ✅ Fazer o download automático de todos os arquivos `.zip` disponíveis em uma lista de URLs.
- ✅ Extrair automaticamente os arquivos `.CSV` contidos nos zips.
- ✅ Armazenar os dados em uma pasta local.
- ✅ Realizar filtros (Razão Social (Cod Operadora)/Período de referência).
- ✅ (Opcional) Deletar os arquivos após o processamento.

---

## 📂 Estrutura do Projeto

├── sibInativos.ipynb # Script para download do SIB de beneficiários inativos
├── share_mensal.ipynb # Script para download do SIB de beneficiários ativos mês a mês
├── README.md # Documentação do projeto
├── data/ # Pasta onde os arquivos são salvos e extraídos
└── .gitignore / # Arquivo com o caminho das pastas e arquivos gerados


---

## 🚀 Como usar

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/ans-ftp-scraper.git
cd ans-ftp-scraper
```
---

## 🚀 Configuração

### 2. Configure as URLs e filtros desejados

```bash
#URL pasta com bases desejadas
url =  'https://dadosabertos.ans.gov.br/FTP/PDA/informacoes_consolidadas_de_beneficiarios-024/'
url2 = 'https://dadosabertos.ans.gov.br/FTP/PDA/dados_de_beneficiarios_por_operadora/'


#pastas onde os arquivos serão salvos e extraídos
dir = 'Share_SP'
dir_adj = 'Share_ADJ_SP'
dir2 = 'Cancelamento'

#Número de anos desejados
last_Year= links[-14:-1]

#SIB Inaitvo, caso deseje os ativos alterar para 'sib_ativo'
if href.startswith('sib_inativo'):
```

## 🚀 Execução

### 4. Instale os pacotes e bibliotecas necessárias e execute o scrapper


## ⚙️ Funcionalidades adicionais


```bash
#Delays aleatórios entre os downloads para evitar bloqueios no servidor:
time.sleep(random.uniform(1, 3))

#Filtro por operadoras, inclua o código da operadora desejada
op = [327417, 335100, 350249, 366561]

```

## 📌 Observações

O FTP da ANS não possui API para agrupamento ou download em massa, e disponibiliza arquivos separadamente em .zip. Este projeto resolve essa lacuna com automação.Cuidado com arquivos mal formatados. Recomendado usar o parâmetro error_bad_lines=False no pandas.read_csv() se necessário.

##✨ Contribuições
Contribuições são bem-vindas! Sinta-se livre para abrir issues ou pull requests com melhorias, correções ou novas funcionalidades.


