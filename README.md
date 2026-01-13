# 🐾 Projeto: ONG de Animais
Este repositório contém o projeto de banco de dados desenvolvido para a gestão de uma ONG de Proteção Animal. O sistema abrange desde o controle de espécies e raças até o histórico clínico de vacinação e o processo final de adoção.

## 📌 Visão Geral do Banco de Dados
O banco de dados, denominado extensao, utiliza o motor InnoDB e codificação utf8mb4 para garantir a integridade referencial e suporte a caracteres especiais. Ele foi projetado para operar em servidores MariaDB/MySQL.

## 🏗️ Estrutura das Tabelas:

- **animal:** Tabela central que armazena informações como nome, idade, sexagem e o status atual (Ex: Disponível, Adotado, Em Tratamento).

- **especie e raca:** Tabelas de classificação para organizar os animais (Cães, Gatos, etc.) e suas respectivas raças.

- **adotante:** Cadastro completo de tutores, incluindo CPF, telefone, e-mail e endereço.

- **vacina e vacina_animal:** Gerenciamento do catálogo de vacinas e o registro de cada dose aplicada, permitindo rastrear o fabricante e a data da aplicação.

- **adocao:** Registra o vínculo formal entre o animal e o adotante, com a data da realização do processo.

## 📊 Inteligência de Dados (Views)
O projeto conta com diversas consultas pré-configuradas para gerar relatórios automáticos:

### 1. Controle de Estoque Animal
- **v_animais_disponiveis**: Lista os animais disponíveis para adoção.
- **v_total_animais_raca**: Quantitativo de animais agrupados por raça.

### 2. Saúde e Bem-estar
- **v_animaisvacinados**: Histórico completo de imunização por animal.
- **v_animais_disponiveis_sem_vacina**: Identifica animais disponíveis para adoção que ainda não receberam vacinação.
- **v_media_vacinas_aplicadas_ano**: Métricas anuais de produtividade da clínica veterinária.

### 3. Gestão de Adotantes
- **v_adocoes_adotante**: Ranking de adotantes mais ativos e contagem de adoções por pessoa.

## 🧩 Diagrama do Modelo Lógico
<p align="center">
  <img 
    src="https://github.com/user-attachments/assets/c1230587-c70a-4774-8a75-3043dca8d0e4"
    alt="Modelo Lógico da ONG de Animais"
    width="600"
  />
</p>
