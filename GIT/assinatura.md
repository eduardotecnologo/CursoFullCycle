## Gerando chave gpg e assinando commits

-- Verifica se já existe uma chave

❯ gpg --list-secret-key --keyid-form LONG

-- Criando uma chave
❯ gpg --full-generate-key
gpg (GnuPG) 2.2.19; Copyright (C) 2019 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      <n>  = key expires in n days
      <n>w = key expires in n weeks
      <n>m = key expires in n months
      <n>y = key expires in n years
Key is valid for? (0) 1y
Key expires at Sun Feb 18 15:51:54 2024 -03
Is this correct? (y/N) y

GnuPG needs to construct a user ID to identify your key.

Real name: eduardotecnologo
Email address: eduardotecnologo@hotmail.com
Comment: assinatura
You selected this USER-ID:
    "eduardotecnologo (assinatura) <eduardotecnologo@hotmail.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O

-- Listando as cghaves
❯ gpg --list-secret-key --keyid-form LONG
-- Visualisando a chave
❯ gpg --armor --export "ID"

-- Configurando o git para sempre verificar a assinatura
❯ git config --global user.signingkey "ID"

-- Variáveis de ambiente

❯ export GPG_TTY=$(tty)
❯ vim ~/.zshrc
❯ vim ~/.bashrc
❯ vim ~/.zshrc

-- Assinando todos os commits por padrão
❯ git config --global commit.gpgsign true
