Agora é solicitado que você faça um PR. Siga estes passos cuidadosamente para completar a tarefa:

1. Primeiro, garanta que todos os testes estão funcionando para a branch atual. Execute a suíte de testes apropriada para seu projeto e confirme que todos os testes passam. Se algum teste falhar, corrija os problemas antes de prosseguir.

2. Faça commit das mudanças que você fez. Use uma mensagem de commit clara e concisa que resuma as alterações.

3. Mova o card do Linear associado com esta tarefa para o status "In Review". 

4. Abra um Pull Request (PR) com os detalhes da implementação:

   Importante: Não mencione nenhum código relacionado a AI ou Claude no PR.

5. Aguarde 3 minutos e verifique comentários da ferramenta automatizada de code review. Se nenhum comentário aparecer, aguarde mais 3 minutos e verifique novamente.

6. Uma vez que você receba comentários da ferramenta automatizada de code review, analise cada comentário cuidadosamente. Determine quais comentários requerem correções e quais podem ser ignorados com segurança ou explicados. Apresente suas sugestões ao usuário e peça permissão para fazer as mudanças.

7. Para os comentários que requerem correções:
   a. Faça as mudanças necessárias no código
   b. Faça commit dessas mudanças com uma mensagem de commit clara
   c. Faça push do(s) novo(s) commit(s) para a mesma branch

8. Após abordar os comentários e fazer push das atualizações, notifique o usuário que a tarefa está completa e pronta para sua revisão final e merge manual.

REGRA DE OURO: Sempre faça commit APENAS dos arquivos que você alterou. Não use `git add .` para prevenir commits de arquivos que não deveriam ser commitados.

Seu output final deve ser uma mensagem para o usuário, formatada da seguinte forma:

<task_completion_message>
Tarefa completada:
- Testes estão passando
- Mudanças commitadas
- Card do Linear [INSERT CARD ID] movido para "In Review"
- PR aberto: [INSERT PR TITLE]
- Comentários do code review automatizado abordados e correções pushed

O PR está agora pronto para sua revisão final e merge manual.

[INSERT PR LINK]
</task_completion_message>

