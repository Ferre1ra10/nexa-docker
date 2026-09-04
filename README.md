# 🐳 Nexa Sistemas — Desafio Docker

> ⚠️ **Nota:** Este projeto é apenas um exemplo de estudos desenvolvido exclusivamente para fins de aprendizado sobre conteinerização de aplicações web com Docker e servidor Nginx.

---

## 📌 Sobre o Projeto

Este repositório contém a simulação de implantação da página institucional da **Nexa Sistemas** dentro de um container Docker isolado. O site foi construído em HTML5 e CSS3 inspirado no *Design System Aaply*, contando com layout responsivo, animações fluidas e a apresentação dos serviços da empresa.

### 🛠️ Serviços Apresentados no Site

* **Desenvolvimento de Sistemas:** Soluções personalizadas para empresas.
* **Análise de Dados:** Transformação de dados em inteligência de negócio.
* **Infraestrutura:** Soluções modernas para ambientes tecnológicos.

---

## 🧰 Tecnologias Utilizadas

* **HTML5 & CSS3:** Interface desenvolvida com conceito visual moderno.
* **Nginx (latest):** Servidor web responsável por servir os arquivos estáticos.
* **Docker:** Ferramenta para criação de imagens e gerenciamento de containers.

---

## 📂 Estrutura do Projeto

```text
nexa-docker/
├── html/
│   └── index.html
├── Dockerfile
└── README.md
```

---

## 🚀 Como Executar o Projeto

### Pré-requisito

* Docker Desktop instalado e em execução na sua máquina.

### Passo a Passo de Execução

**1. Abrir o terminal na pasta do projeto:**
Abra o PowerShell ou Prompt de Comando dentro do diretório do projeto:

```bash
cd nexa-docker
```

**2. Construir a imagem Docker:**
Execute o comando de build para gerar a imagem `nexa-site`:

```bash
docker build -t nexa-site .
```

**3. Criar e iniciar o container:**
Rode o container mapeando a porta 9090 da sua máquina para a porta 80 do Nginx:

```bash
docker run -d -p 9090:80 --name nexa-container nexa-site
```

**4. Visualizar no navegador:**
Abra o navegador de sua preferência e acesse: [http://localhost:9090](http://localhost:9090)

---

## 🧹 Como Parar e Remover o Container

Após concluir o teste de estudo, execute os comandos abaixo para encerrar o ambiente e liberar recursos da máquina:

```bash
# Parar o container
docker stop nexa-container

# Remover o container
docker rm nexa-container
```
