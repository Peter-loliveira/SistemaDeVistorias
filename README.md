# 🏠 Sistema de Laudo de Vistoria Imobiliária

Sistema web para elaboração de laudos de vistoria de imóveis, desenvolvido para corretores e imobiliárias. Permite documentar fotograficamente o estado do imóvel e gerar relatórios PDF profissionais.

---

## 📋 O que este sistema faz

### 1. Cadastro da Vistoria
- Registra informações do corretor (nome, CRECI, CPF)
- Identifica o tipo de vistoria (Inicial, Final ou Complementar)
- Cadastra dados do imóvel (endereço, tipo, destinação)
- Registra partes envolvidas (locador e locatário)

### 2. Avaliação do Estado do Imóvel
- Classifica o imóvel em: Novo, Excelente, Bom, Regular ou Ruim
- Cada classificação possui identificação visual por cores

### 3. Registro Fotográfico
O sistema permite adicionar fotos de duas formas:

**📷 Itens da Vistoria**
- Fotos de todos os ambientes e itens do imóvel
- Cada foto pode ter uma descrição detalhada

**🔧 Danos Encontrados**
- Registro fotográfico específico de problemas ou defeitos
- Documentação visual de estragos pré-existentes

### 4. Captura de Imagens
- **Câmera**: Acesse a câmera do dispositivo diretamente pelo navegador
- **Galeria**: Selecione fotos já existentes no dispositivo
- Visualização em cards organizados e de tamanho padronizado

### 5. Geração de PDF Profissional
- Laudo formatado com logo da empresa
- Texto introdutório automático com todos os dados cadastrados
- Tabelas organizadas com fotos e descrições
- Assinaturas digitais para locador, locatário e corretor
- Numeração de páginas personalizada

### 6. Exportação de Fotos
- Download de todas as fotos em arquivo ZIP organizado
- Pastas separadas: "Itens" e "Danos"

---

## 🚀 Como usar

### Acesso ao Sistema
1. Abra o arquivo `index.html` em um navegador moderno
2. O sistema funciona em computadores, tablets e smartphones

### Passo a Passo

#### 1. Preencha os Dados
- Selecione o tipo de vistoria
- Informe estado e município (Bahia e Camaçari já vêm pré-selecionados)
- Preencha datas, dados do corretor e do imóvel
- Selecione a condição do imóvel

#### 2. Adicione Fotos
- Clique em **Câmera** para tirar foto na hora
- Clique em **Galeria** para selecionar fotos do dispositivo
- Descreva cada foto no campo de texto do card
- Use o ícone 🗑️ para remover fotos indesejadas

#### 3. Gere o PDF
- Clique em **"Gerar PDF"**
- O arquivo será baixado automaticamente com o nome:  
  `LAUDO_DE_VISTORIA_{Locador}_{Locatario}.pdf`

#### 4. Salve as Fotos (opcional)
- Clique em **"Salvar Fotos"** para baixar todas as imagens em ZIP

---

## 📁 Estrutura de Arquivos
sistema-vistoria/
│
├── index.html          # Arquivo principal do sistema
├── assets/
│   └── Logo.png        # Logo da empresa no cabeçalho
├── JSON/
│   ├── estados.json    # Lista de estados brasileiros
│   └── municipios.json # Lista de municípios por estado
└── README.md           # Este arquivo


---

## ⚠️ Requisitos Importantes

### Navegador
- Use navegadores atualizados (Chrome, Firefox, Edge, Safari)
- É necessário permitir acesso à câmera para captura de fotos

### Arquivos JSON
Os arquivos `estados.json` e `municipios.json` devem estar na pasta `JSON/` com a seguinte estrutura:

**estados.json:**
```json
[
  {"id": 29, "name": "Bahia", "abbr": "BA"},
  ...
]

[
  {"id": 1, "state_id": 29, "name": "Camaçari"},
  ...
]