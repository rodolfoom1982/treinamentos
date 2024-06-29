![](img/artigoCapaComFoto.png)

### O que é o Power Automate
O Power Automate é uma ferramenta da Microsoft que permite automatizar processos e tarefas repetitivas no trabalho. Imagine que você tem várias tarefas manuais que fazem parte do seu dia a dia, como enviar e-mails ou mover arquivos. O Power Automate ajuda a criar fluxos de trabalho automatizados para fazer tudo isso por você, economizando tempo e reduzindo erros.

<br>

### Como funciona o licenciamento premium
Para acessar alguns recursos avançados no Power Automate, você precisa de um licenciamento premium. Esses recursos incluem conectores especiais que permitem integrações mais complexas com outros serviços e aplicativos. Alguns exemplos de conectores premium são o SQL Server, Salesforce e o Dynamics 365. Esses conectores facilitam a conexão com sistemas importantes que você usa no seu trabalho, mas exigem uma licença extra.

> ![](img/licenciamentoPowerAutomate.png)

Se você desenvolve um fluxo do Power Automate que possui um conector *premium*, é necessário que você e todos aqueles com os quais você irá compartilhar este fluxo possuam um licenciamento *premium*, ao custo mensal de R$89,30/usuário (preços de referência em Junho/2024).

Para evitar que aqueles usuários que invocarão seu fluxo (via Power Automate ou qualquer outra solução do Power Platform: Power Apps, Power Pages e/ou Power BI) necessitem de um licenciamento *premium*, a adoção do uso de fluxos filhos torna-se uma excelente opção!

<br>

### O que são fluxos filhos (child flows)
Fluxos filhos, ou child flows, são sub-processos dentro de um fluxo principal no Power Automate. Pense neles como pequenos fluxos de trabalho que podem ser chamados pelo fluxo principal para executar tarefas específicas. Isso é útil quando você tem partes do processo que se repetem em diferentes fluxos, permitindo reutilizar esses blocos de automação em vários lugares.

<br>

### Vantagens de se utilizar fluxos filhos
Utilizar fluxos filhos no Power Automate traz diversas vantagens. Primeiramente, eles promovem a reutilização de código, permitindo que partes do fluxo sejam usadas em vários lugares sem duplicação. Isso facilita a manutenção, já que qualquer alteração no fluxo filho é automaticamente aplicada onde ele é utilizado. Além disso, fluxos filhos ajudam a simplificar fluxos complexos, dividindo-os em partes menores e mais gerenciáveis. Isso torna o processo de automação mais claro e organizado, facilitando tanto o desenvolvimento quanto a revisão e o debugging.

<br>

### Como os fluxos filhos reduzem o volume de licenciamento premium
Os fluxos filhos ajudam a reduzir o custo do licenciamento premium porque permitem que você reutilize os mesmos fluxos em diferentes automações sem precisar criar novos fluxos cada vez. Assim, ao invés de pagar por várias instâncias do mesmo conector premium, você pode usar um fluxo filho para centralizar a tarefa, economizando nas licenças necessárias.

> ![](img/diagrama.png)

No exemplo apresentado acima, o filho torna-se *premium* pois está utilizando um conector REST API, que também é *premium*. Já o fluxo principal (fluxo pai) não possui nenhum tipo de conexão *premium*. Desta forma, ao invocar o fluxo pai, o usuário é dispensado de ter uma licença *premium* do Power Automate. Genial, não é mesmo???

<br>

**Curtiu este conteúdo? Ele foi gerado com a ajuda de inteligência artitifical, porém foi revisado por alguém 100% humano! Se quiser se conectar comigo, me siga no [Linkedin](https://www.linkedin.com/in/rodolfoom/)!**

<br>

***Ilustração de capa***: gerada por meio da [Lexica.art](https://lexica.art/)

***Conteúdo***: gerado através do [ChatGPT](https://chatgpt.com/) e com revisões 100% humana (Eu!)

***Diagramas***: gerados por mim utilizando o [draw.io](https://app.diagrams.net/)
