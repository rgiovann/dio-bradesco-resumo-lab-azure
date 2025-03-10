# Configurando uma Pesquisa com Azure AI Search

Este guia fornece um passo a passo para configurar uma solução de pesquisa utilizando o Azure AI Search, além de discutir insights, ferramentas beneficiadas por essa tecnologia e aprendizados adquiridos durante o processo.

## Sumário

- [Introdução](#introdução)
- [Pré-requisitos](#pré-requisitos)
- [Passo a Passo para Configuração](#passo-a-passo-para-configuração)
  - [1. Criar um Serviço de Pesquisa no Azure](#1-criar-um-serviço-de-pesquisa-no-azure)
  - [2. Criar um Recurso de Serviços Cognitivos](#2-criar-um-recurso-de-serviços-cognitivos)
  - [3. Criar uma Conta de Armazenamento](#3-criar-uma-conta-de-armazenamento)
  - [4. Carregar Documentos no Armazenamento do Azure](#4-carregar-documentos-no-armazenamento-do-azure)
  - [5. Configurar o Indexador e Enriquecer os Dados](#5-configurar-o-indexador-e-enriquecer-os-dados)
  - [6. Consultar o Índice de Pesquisa](#6-consultar-o-índice-de-pesquisa)
- [Insights e Ferramentas Beneficiadas](#insights-e-ferramentas-beneficiadas)
- [Aprendizados Adquiridos](#aprendizados-adquiridos)
- [Referências](#referências)

## Introdução

O Azure AI Search é uma solução de pesquisa como serviço que permite a criação de experiências de pesquisa sofisticadas em aplicativos web e móveis. Ele oferece recursos como indexação de texto completo, enriquecimento de dados com habilidades de IA e integração com diversas fontes de dados.

## Pré-requisitos

- Uma assinatura ativa do Azure. Se você não tiver uma, pode criar uma conta gratuita.
- Familiaridade básica com o portal do Azure e conceitos de armazenamento em nuvem.

## Passo a Passo para Configuração

### 1. Criar um Serviço de Pesquisa no Azure

1. Acesse o [portal do Azure](https://portal.azure.com/) e faça login.
2. Clique em **+ Criar um recurso**, pesquise por **Azure AI Search** e selecione **Criar**.
3. Preencha os seguintes campos:
   - **Assinatura**: Selecione sua assinatura do Azure.
   - **Grupo de recursos**: Crie ou selecione um grupo de recursos existente.
   - **Nome do serviço**: Insira um nome único para o serviço de pesquisa.
   - **Região**: Escolha uma região disponível (por exemplo, "East US 2").
   - **Camada de preço**: Selecione "Básico".
4. Clique em **Revisar + criar** e, após a validação, em **Criar**.

### 2. Criar um Recurso de Serviços Cognitivos

1. No portal do Azure, clique em **+ Criar um recurso** e pesquise por **Serviços Cognitivos**.
2. Selecione **Criar** e preencha os seguintes campos:
   - **Assinatura**: Selecione sua assinatura do Azure.
   - **Grupo de recursos**: Utilize o mesmo grupo de recursos do serviço de pesquisa.
   - **Região**: Certifique-se de que seja a mesma do serviço de pesquisa.
   - **Nome**: Insira um nome único para o recurso de Serviços Cognitivos.
   - **Camada de preço**: Selecione "Standard S0".
3. Marque a caixa de confirmação e clique em **Revisar + criar**. Após a validação, clique em **Criar**.

### 3. Criar uma Conta de Armazenamento

1. No portal do Azure, clique em **+ Criar um recurso** e pesquise por **Conta de Armazenamento**.
2. Selecione **Criar** e preencha os seguintes campos:
   - **Assinatura**: Selecione sua assinatura do Azure.
   - **Grupo de recursos**: Utilize o mesmo grupo de recursos dos recursos anteriores.
   - **Nome da conta de armazenamento**: Insira um nome único.
   - **Região**: Escolha a mesma região dos recursos anteriores.
   - **Desempenho**: Selecione "Standard".
   - **Redundância**: Selecione "Locally redundant storage (LRS)".
3. Clique em **Revisar + criar** e, após a validação, em **Criar**.

### 4. Carregar Documentos no Armazenamento do Azure

1. No recurso de armazenamento, selecione **Containers** e clique em **+ Container**.
2. Nomeie o container como `coffee-reviews` e defina o nível de acesso público como **Container (leitura anônima para blobs e containers)**.
3. Baixe os arquivos de exemplo de avaliações de café a partir deste [link](https://aka.ms/mslearn-coffee-reviews) e extraia-os em uma pasta local.
4. No container `coffee-reviews`, clique em **Upload**, selecione todos os arquivos extraídos e clique em **Upload**.

### 5. Configurar o Indexador e Enriquecer os Dados

1. No portal do Azure, acesse o recurso do Azure AI Search e selecione **Importar dados**.
2. Em **Conectar aos seus dados**, selecione **Azure Blob Storage** e configure a fonte de dados.

## Insights e Ferramentas Beneficiadas

- **Plataformas de e-commerce**: Melhoram a pesquisa de produtos.
- **Setor financeiro**: Facilita a busca de relatórios e documentos.
- **Aplicativos de suporte ao cliente**: Ajuda na recuperação rápida de respostas.

## Aprendizados Adquiridos

- **Importância da indexação bem estruturada**.
- **Uso de IA para melhorar resultados de busca**.
- **Gerenciamento de fontes de dados distribuídas**.

## Referências

- [Microsoft Learn - AI Search](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)
- [Documentação oficial do Azure AI Search](https://learn.microsoft.com/pt-br/azure/search/)

