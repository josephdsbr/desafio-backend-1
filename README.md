# Projeto de teste de back-end <img src="https://coderockr.com/assets/images/coderockr.svg" align="right" height="50px" />

Você deve ver esse desafio como uma oportunidade de criar um aplicativo seguindo as práticas recomendadas de desenvolvimento moderno (dada a pilha de sua escolha), mas também sinta-se à vontade para usar suas próprias preferências de arquitetura (padrões de codificação, organização de código, bibliotecas de terceiros, etc.) . É perfeitamente normal usar código vanilla ou qualquer estrutura ou biblioteca.

## Escopo

Neste desafio você deverá construir uma API para uma aplicação que armazena e gerencia investimentos, ela deverá ter as seguintes funcionalidades:

1. _Criação_ de um investimento com proprietário, data de criação e valor.
    1. A data de criação de um investimento pode ser hoje ou uma data passada.
    2. Um investimento não deve ser nem tornar-se negativo.
2. _Visão_ de um investimento com seu valor inicial e saldo esperado.
    1. O saldo esperado deve ser a soma do valor investido e dos [ganhos][].
    2. Se um investimento já foi retirado, o saldo deve refletir os ganhos desse investimento
3. _Retirada_ de um investimento.
    1. O saque será sempre a soma do valor inicial e seus ganhos,
       retirada parcial não é suportada.
    2. As retiradas podem acontecer no passado ou hoje, mas não podem acontecer antes da criação do investimento ou no futuro.
    3. [Impostos][impostos] precisam ser aplicados aos saques antes de mostrar o valor final.
4. _Lista_ dos investimentos de uma pessoa
    1. Esta lista deve ter paginação.

_NOTA:_ a implementação de uma interface não será avaliada.

### Cálculo de ganho

O investimento pagará 0,52% todo mês no mesmo dia da criação do investimento.

Dado que o ganho é pago mensalmente, deve ser tratado como [ganho composto][], o que significa que a cada novo período (mês) o valor ganho passará a fazer parte do saldo do investimento para o próximo pagamento.

### Tributação

Quando o dinheiro é retirado, o imposto é acionado. Os impostos aplicam-se apenas à parte do lucro/ganho do dinheiro retirado. Por exemplo, se o investimento inicial foi de 1.000,00, o saldo atual é de 1.200,00, então os impostos serão aplicados sobre os 200,00.

A percentagem de imposto muda de acordo com a antiguidade do investimento:
*Se tiver menos de um ano o percentual será de 22,5% (imposto = 45,00).
*Se tiver entre um e dois anos o percentual será de 18,5% (imposto = 37,00).
*Se tiver mais de dois anos o percentual será de 15% (imposto = 30,00).

## Requisitos
1. Crie projeto utilizando qualquer tecnologia de sua preferência. É perfeitamente normal usar código vanilla ou qualquer estrutura ou biblioteca;
2. Embora você possa usar quantas dependências quiser, você deve gerenciá-las com sabedoria;
3. Não é necessário enviar os e-mails de notificação, porém o código necessário para isso será bem-vindo;
4. A API deve ser documentada de alguma forma.

## Entregáveis
O código-fonte e as dependências do projeto devem ser disponibilizados no GitHub. Aqui estão as etapas que você deve seguir:
1. Bifurque este repositório para sua conta GitHub (crie uma conta se não tiver uma, você precisará que ela trabalhe conosco).
2. Crie um branch de "desenvolvimento" e envie o código para ele. Não envie o código para o branch principal.
3. Inclua um arquivo README que descreva:
    - Instruções especiais de construção, se houver
    - Lista de bibliotecas de terceiros usadas e breve descrição de por que/como foram usadas
    - Um link para a documentação da API.
4. Assim que o trabalho for concluído, crie uma solicitação pull de "desenvolvimento" para "principal" e envie-nos o link.
5. Evite usar commits enormes para esconder seu progresso. Sinta-se à vontade para trabalhar em um branch e usar git rebase para ajustar seus commits antes de enviar a versão final.

## Padrões de codificação
Ao trabalhar no projeto, seja o mais limpo e consistente possível.

## Prazo do Projeto
Idealmente, você terminaria o projeto de teste em 5 dias. Não deve demorar mais do que uma semana inteira.

## Garantia da Qualidade
Use a lista de verificação a seguir para garantir a alta qualidade do projeto.

### Em geral
- Em primeiro lugar, a aplicação deve funcionar sem erros.
- Todos os requisitos definidos acima foram atendidos?
- O estilo de codificação é consistente?
- A API está bem documentada?
- A API possui testes unitários?

## Envio
1. Um link para o repositório Github.
2. Descreva resumidamente como você decidiu quais ferramentas usar.

## Divirta-se codificando 🤘
- Esta descrição do desafio é intencionalmente vaga em alguns aspectos, mas se precisar de ajuda, sinta-se à vontade para pedir ajuda.
- Se algum deles parecer fora do seu nível atual, você pode ignorá-lo, mas lembre-se de nos informar sobre isso na solicitação pull.

## Créditos

Este desafio de codificação foi inspirado em [kinvoapp/kinvo-back-end-test](https://github.com/kinvoapp/kinvo-back-end-test/blob/2f17d713de739e309d17a1a74a82c3fd0e66d128/README.md)

[ganhos]: #cálculo-ganho
[impostos]: #tributação
[juros]: #cálculo de juros
[ganho composto]: https://www.investopedia.com/terms/g/gain.asp