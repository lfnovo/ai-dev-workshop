
Este é um projeto de documentação para vários projetos open source de nossa organização. A ideia deste repositório é ser a especificação única que direciona todas as outras especificações, código, design e artefatos de teste. É nossa fonte canônica de verdade para todos os nossos projetos.

Cada projeto tem sua própria pasta sob a pasta @/projects/
Dentro de cada uma dessas pastas, há um arquivo index.md que aponta para todos os outros recursos úteis do projeto.

## Uso

### /build-index

Se nenhum argumento for fornecido, o comando construirá o arquivo index.md raiz dos projetos sob a pasta @/projects/
Este índice deve fornecer informações básicas sobre cada projeto, tais como:

- nome com link para sua pasta
- descrição breve
- id do projeto linear
- id da equipe linear
- url do repositório

Esta informação está facilmente disponível dentro dos arquivos principais dos projetos (seja index.md ou 2-project_management.md)

Não adicione mais nada além das informações acima.


### /build-index <nome-do-projeto>

Isso é usado para reconstruir o índice do projeto depois que mudamos a estrutura de diretórios e arquivos.
Por favor, vá através da estrutura de pastas do projeto, entenda quais arquivos e pastas estão lá e refine o arquivo index.md para o projeto. Se o projeto não tiver um arquivo index.md, crie-o. Se tiver, edite-o para refletir a estrutura atual.

O índice deve apontar para todos os outros recursos úteis na pasta do projeto.

Argumentos fornecidos: #$ARGUMENTS
