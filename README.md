# 🎵 Sistema Musical

Sistema web em PHP + MySQL para gerenciamento de artistas, músicas e biblioteca musical, com autenticação de usuários, upload de imagens e sessão de login.

## Visão geral

Este projeto foi desenvolvido para cadastrar artistas e músicas, organizar uma biblioteca musical e permitir o acesso por meio de login com autenticação de sessão. A interface foi estruturada em páginas PHP com CSS próprio e banco de dados relacional.

## Funcionalidades

- Login e logout com sessão
- Proteção de páginas por autenticação
- Cadastro de artistas
- Cadastro de músicas
- Upload de imagens para artistas e capas de álbum
- Biblioteca musical com filtros e visualização
- Estrutura pronta para uso em ambiente local com XAMPP/WAMP/Laragon

## Tecnologias

- PHP
- MySQL
- HTML/CSS
- JavaScript (quando necessário em páginas dinâmicas)
- Biblioteca GD para processamento de imagens

## Requisitos

- PHP 7 ou superior
- MySQL
- Apache/Nginx
- Extensão GD habilitada no PHP
- phpMyAdmin (opcional, mas recomendado)

## Estrutura do projeto

```text
artistas-musicas/
├── README.md
├── README-fase2.md
├── bd.sql
├── conexao.php
├── geraSenha.php
├── valida_sessao.php
├── login.php
├── logout.php
├── index.php
├── cadastro_artista.php
├── cadastro_musica.php
├── listagem_musicas.php
├── styles.css
├── teste_conexao.php
├── img/
└── img - Ref/
```

## Configuração do banco de dados

1. Inicie o Apache e o MySQL no seu ambiente local.
2. Acesse o phpMyAdmin.
3. Crie o banco de dados e importe o arquivo `bd.sql`.
4. Verifique se a tabela `usuarios` foi criada corretamente.
5. Ajuste as credenciais no arquivo `conexao.php` caso necessário.

Exemplo de configuração:

```php
$servername = "localhost";
$username   = "root";
$password   = "sua_senha";
$dbname     = "sistema_musical_v2";
```

## Usuário padrão

O sistema já inclui um usuário padrão para acesso inicial:

- Usuário: `admin`
- Senha: `123`

A senha é armazenada em hash seguro com `password_hash`, não em texto puro.

## Como executar

1. Coloque a pasta do projeto dentro do diretório do servidor local, por exemplo:

```text
C:\xampp\htdocs\artistas-musicas
```

2. Acesse no navegador:

```text
http://localhost/artistas-musicas/login.php
```

3. Faça login com as credenciais padrão.

## Fluxo do sistema

- `login.php` → autenticação do usuário
- `valida_sessao.php` → bloqueia acesso sem login
- `index.php` → menu principal
- `cadastro_artista.php` → cadastro e gerenciamento de artistas
- `cadastro_musica.php` → cadastro e gerenciamento de músicas
- `listagem_musicas.php` → visualização da biblioteca musical
- `logout.php` → encerra a sessão

## Observações importantes

- A pasta `img` é criada automaticamente pelo arquivo `conexao.php`.
- Certifique-se de que a extensão GD do PHP esteja habilitada para trabalhar com upload e redimensionamento de imagens.
- Em produção, evite expor detalhes técnicos de conexão e erro no navegador.

## Autor

Projeto desenvolvido para fins de estudo e gerenciamento musical em PHP/MySQL.

## Licença

Este projeto não possui uma licença formal definida no repositório. Caso deseje reutilizar ou distribuir, verifique antes com o responsável pelo projeto.
