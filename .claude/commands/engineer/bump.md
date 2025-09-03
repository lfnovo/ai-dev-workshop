Vamos preparar isso para um release aumentando o número da versão.

Siga estas regras para versionamento x.y.z:

- x (Versão major): Incremente quando você fizer mudanças incompatíveis na API ou funcionalidade. Exemplos incluem:
Mudanças que quebram APIs públicas (ex.: remover ou renomear métodos).
Reescritas majors ou refatoração que alteram comportamento.
Mudanças que requerem que usuários atualizem seu código ou dependências para manter compatibilidade.
- y (Versão minor): Incremente quando você adicionar novas funcionalidades ou melhorias de forma retrocompatível. Exemplos incluem:
Adicionando novos métodos, endpoints, ou funcionalidades.
Depreciar funcionalidades (mas não removê-las ainda).
Melhorias que não quebram funcionalidades existentes.
- z (Versão patch): Incremente quando você fizer correções de bugs retrocompatíveis ou pequenas atualizações. Exemplos incluem:
Corrigir bugs sem alterar funcionalidade pretendida.
Pequenas melhorias de performance.
Atualizações de documentação ou mudanças de metadata.

Altere a versão no pyproject.toml.
Então, execute `uv sync --all-extras` para regenerar o lock file. 