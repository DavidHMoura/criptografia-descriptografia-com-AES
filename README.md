AES File Cryptographer 🔒
Um projeto em Python para criptografar e descriptografar arquivos usando o algoritmo AES-256 no modo CBC (Cipher Block Chaining). Ideal para aprender fundamentos de criptografia aplicada em cybersecurity.

📌 Funcionalidades
✅ Criptografia de arquivos com AES-256-CBC.

✅ Geração segura de chaves (32 bytes aleatórios).

✅ Uso de Initialization Vector (IV) para maior segurança.

✅ Suporte a arquivos de qualquer tamanho (com padding automático).

✅ Descriptografia com verificação de integridade.

⚙️ Instalação
Clone o repositório:

bash
git clone https://github.com/seu-usuario/aes-file-cryptographer.git
cd aes-file-cryptographer
Instale as dependências:

bash
pip install pycryptodome
🛠️ Como Usar
1. Gerar uma Chave AES
Execute para criar uma chave secreta (secret.key):

bash
python key_manager.py
2. Criptografar um Arquivo
bash
python encrypt.py arquivo_original.txt
Saída: arquivo_original.txt.enc (contém IV + dados cifrados).

3. Descriptografar
bash
python decrypt.py arquivo_original.txt.enc
Saída: arquivo_original.txt.dec (igual ao arquivo original).

🔍 Exemplo Prático
bash
echo "Segredo muito importante!" > mensagem.txt
python encrypt.py mensagem.txt
python decrypt.py mensagem.txt.enc
cat mensagem.txt.dec  # Exibe "Segredo muito importante!"
📚 Explicação Técnica
AES-256-CBC
Chave: 256 bits (32 bytes), gerada aleatoriamente.

IV (Initialization Vector): 16 bytes aleatórios, único para cada operação.

Padding: Preenchimento PKCS#7 para ajustar ao tamanho do bloco (16 bytes).

Estrutura do Arquivo Cifrado
[IV (16 bytes)][Dados Cifrados + Padding]
⚠️ Avisos de Segurança
NUNCA reuse a mesma chave + IV para diferentes arquivos.

Proteja a chave (secret.key): Armazene em um local seguro (ex: cofre de senhas).

Para maior segurança: Use AES-GCM (com autenticação) em vez de CBC.

🚀 Melhorias Futuras
Adicionar suporte a AES-GCM.

Implementar derivação de chave com senha (PBKDF2).

Criar uma interface gráfica (GUI) com Tkinter.

📜 Licença
Este projeto está sob a licença MIT. Consulte o arquivo LICENSE para detalhes.

Desenvolvido por David H. Moura