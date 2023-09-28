# Git revert

- reverte para o arquivo anterior, ainda tem acesso ao commit que ocorreu o erro
- O commit com erro não é apagado
- para voltat o commit com defeito, git reset

```shell
git revert --no-edit <códgo-do-commit-com problema>
```


>[!warning]
>A principal diferença entre o git revert e o git reset é a abordagem para desfazer alterações. O git reset desfaz um ou mais commits descartando-os completamente, o que pode levar a uma perda permanente das alterações feitas nesses commits.   
>O uso do git revert é recomendado quando você está trabalhando em um ambiente colaborativo, onde outros membros da equipe podem ter se baseado nos commits anteriores. O git revert permite desfazer alterações de forma segura, preservando o histórico e evitando possíveis conflitos com outros desenvolvedores.  
  Em resumo, o git revert é útil para desfazer alterações de forma segura e manter o histórico consistente, enquanto o git reset é mais adequado para redefinir o estado do repositório de forma mais drástica, descartando alterações não desejadas. A escolha entre eles dependerá das necessidades do seu projeto e das circunstâncias específicas.
