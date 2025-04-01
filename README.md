# 🔐 **AI-Powered Encryption API**  
Segurança de dados elevada a um novo patamar 🚀  

## 📜 **Visão Geral**  
Bem-vindo ao **AI-Powered Encryption API**, uma plataforma inovadora que utiliza **inteligência artificial** para **selecionar dinamicamente o melhor algoritmo de criptografia** para cada tipo de arquivo. Este projeto integra **Flask**, **Machine Learning** e diversos métodos de criptografia para fornecer **proteção robusta e eficiente** aos seus dados.  

🔗 **Repositório:** [Thalys-Riquelmy/App_Criptografia](https://github.com/Thalys-Riquelmy/App_Criptografia.git)  

## 🌟 **Destaques do Projeto**  
✅ **IA para Escolha Inteligente** – A API analisa as características do arquivo e recomenda o **melhor algoritmo de criptografia**.  
✅ **Suporte a Vários Algoritmos** – Trabalhamos com **AES, DES, Blowfish, Fernet e RSA**.  
✅ **Gerenciamento de Chaves Seguras** – As chaves de criptografia são geradas automaticamente e podem ser baixadas para **uso futuro na descriptografia**.  
✅ **Interface Web Amigável** – API pronta para integrar-se com **aplicações modernas** via HTTP.  
✅ **Código Aberto e Modular** – Fácil personalização e expansão do sistema.  

## 🔍 **Como Funciona?**  
1️⃣ **Treinamento do Modelo de IA** – O sistema treina um classificador baseado no tamanho do arquivo para prever o algoritmo adequado.  
2️⃣ **Envio do Arquivo** – O usuário faz upload de um arquivo via API para ser criptografado.  
3️⃣ **Processamento Inteligente** – A IA **escolhe automaticamente** o algoritmo ou permite que o usuário **defina um**.  
4️⃣ **Criptografia e Geração de Chaves** – O arquivo é criptografado e a chave correspondente é gerada.  
5️⃣ **Download Seguro** – O usuário baixa um **arquivo ZIP contendo o arquivo criptografado, o original e a chave**.  
6️⃣ **Descriptografia Simples** – Basta fazer upload do arquivo criptografado e da chave via API para recuperar os dados originais.  

## ⚡ **Instalação e Uso**  

### 🔧 **Pré-requisitos**  
- Python 3.x  
- Flask  
- Flask-CORS  
- NumPy  
- scikit-learn  
- Cryptography  
- PyCryptodome  

### 🚀 **Instalação**  
```bash
git clone https://github.com/Thalys-Riquelmy/App_Criptografia.git
cd App_Criptografia
pip install -r requirements.txt
python app.py
```
O servidor iniciará em `http://localhost:5000`.  

### 🛠️ **Como Testar no Postman**  

#### 📌 **Predição Automática do Algoritmo e Criptografia**  
1️⃣ Abra o **Postman** e crie uma nova requisição.  
2️⃣ Configure o método como **POST** e a URL para:  
   ```
   http://localhost:5000/predict
   ```  
3️⃣ Vá até a aba **Body**, selecione `form-data`, e adicione um campo:  
   - **Chave:** `file`  
   - **Tipo:** `File`  
   - **Valor:** Selecione o arquivo que deseja criptografar  
4️⃣ Clique em **Send** e faça o download do arquivo ZIP retornado.  

#### 🔑 **Criptografia Manual**  
1️⃣ Configure o método como **POST** e a URL:  
   ```
   http://localhost:5000/encrypt
   ```  
2️⃣ Na aba **Body**, selecione `form-data` e adicione:  
   - **Chave:** `file` (Tipo: `File`, selecione o arquivo)  
   - **Chave:** `algorithm` (Tipo: `Text`, insira `AES`, `DES`, `Blowfish`, `Fernet` ou `RSA`)  
3️⃣ Clique em **Send** e baixe o arquivo ZIP criptografado.  

#### 🔓 **Descriptografia**  
1️⃣ Configure o método como **POST** e a URL:  
   ```
   http://localhost:5000/decrypt
   ```  
2️⃣ Na aba **Body**, selecione `form-data` e adicione:  
   - **Chave:** `encrypted_file` (Tipo: `File`, selecione o arquivo criptografado)  
   - **Chave:** `key_file` (Tipo: `File`, selecione o arquivo de chave)  
3️⃣ Clique em **Send** e baixe o arquivo descriptografado.  

## 📂 **Estrutura do Projeto**  
```
📁 App_Criptografia
│── 📁 uploads/          # Armazena arquivos enviados
│── 📁 downloads/        # Armazena chaves criptográficas
│── 📁 venv/             # Ambiente virtual do projeto
│── 🔹 app.py            # Código principal Flask
│── 🔹 cryptography_ai.py # Código adicional de criptografia com IA
│── 🔹 encryption_model.pkl # Modelo IA treinado
│── 🔹 meuarquivo.txt    # Arquivo de teste
│── 🔹 meuarquivo.txt.encrypted # Arquivo de teste criptografado
│── 🔹 README.md         # Documentação do projeto
│── 🔹 requirements.txt  # Dependências do projeto
```

## 🛡️ **Por que Usar Este Projeto?**  
🔹 **Proteção de Dados** – Ideal para quem deseja criptografar arquivos sensíveis em **sistemas empresariais** ou **aplicações pessoais**.  
🔹 **Automação Inteligente** – A integração com **machine learning** elimina a necessidade de decidir manualmente o algoritmo adequado.  
🔹 **Segurança e Facilidade** – O uso de **Flask** e **API REST** permite integração rápida com diferentes aplicações.  

