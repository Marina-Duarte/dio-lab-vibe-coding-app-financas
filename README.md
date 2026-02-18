# 💸 App de Organização de Finanças Pessoais com Vibe Coding
Nome do aplicativo: Duarte Valore

PRD refinado com a ajuda do COPILOT
> Crie um aplicativo com base no meu PRD - Product Requirements Document
(Documento de Requisitos do Produto).
Produto: Duarte Valore
# Contexto
Aplicativo no‑code para clientes de investimentos controlarem receitas e despesas por meio de conversas em linguagem natural de fácil compreensão.  
Além do controle financeiro, o app deve realizar já no cadastro inicial uma análise de perfil do investidor.  
Com o valor destinado aos aportes já definido após a análise de receitas e despesas, o cliente terá acesso a uma aba contendo suas metas financeiras, descritas pelo próprio usuário, com prazo de realização.  
Nessa aba, deverão aparecer ativos compatíveis com cada meta financeira, alinhando aportes mensais ao perfil e horizonte de investimento.  
Adicionar uma aba de “Fale com a assessora”. Com link direcionando para conversar pelo whatsapp pelo número +55 (88)992548361.
Esses ativos serão sugeridos pela assessora através de um relatório detalhado das recomendações que será entregue em PDF e apresentado pela assessora.  
Dentro do app, o cliente verá apenas a recomendação direta de ativos para cada meta, de acordo com seu perfil de investidor.  
O controle de receitas e despesas será feito exclusivamente pelo cliente, sem acesso por terceiros (inclusive a assessora), garantindo privacidade e individualidade.  
O aplicativo deverá alertar o cliente caso ele não consiga atingir o valor necessário de aportes a cada mês e, após 3 meses de não atingimento da meta, deverá alertar a assessora para uma interação pessoal.  
O cálculo será feito assim: O cliente vai colocar as rendas e desse valor, será separado 20% para investir. Caso o cliente supere esse percentual, o aplicativo deverá enviar mensagem parabenizando e incentivando a manter o ritmo. 

# Problema
Muitas pessoas desistem de controlar seus gastos porque os apps atuais exigem muita entrada manual e pouca personalização.  
Mesmo quando conseguem poupar, não sabem como direcionar o dinheiro para investimentos adequados ao seu perfil e objetivos.  
Quero resolver isso com uma experiência de conversa, recomendações automáticas de economia e sugestões de ativos alinhados ao perfil de investidor.  

# Público-Alvo
- Clientes de gestão de carteira com diferentes perfis de risco (conservador, moderado, agressivo).  
- Pessoas que querem começar a organizar suas finanças de forma prática e receber orientação clara sobre onde investir.  

# Funcionalidades-Chave
1. Registrar gastos via chat em linguagem natural.  
2. Classificar automaticamente as transações.  
3. Definir e acompanhar metas financeiras.  
4. Analisar perfil de investidor no onboarding.  
5. Sugerir ativos compatíveis com cada meta e perfil.  
6. Receber dicas de economia do “Agente Financeiro”.  
7. Visualizar relatórios simples e personalizados.  
8. Alertas de não atingimento de metas e escalonamento para a assessora após 3 meses.
9. Adicionar gráficos de receitas x despesas e de classificação dos gastos.
10. Adicionar uma barra com percentual de atingimento de metas.
11. Adicionar no campo das metas, a possibilidade de ajustar o saldo todo mês e recalcular o percentual da meta atingida.   

# Entregável da IA
Gerar um plano de MVP com:  
- Principais telas: Onboarding (com análise de perfil), Dashboard, Adicionar Transação, Metas (com recomendação de ativo), Relatórios, Configurações.  
- Recursos necessários: banco de dados com usuários, transações, metas, perfil de investidor e alertas; workflows para classificação NLP, cálculo de aporte, recomendação de ativos e alertas.  
- Esboço de validação inicial:  
  - Testar registro de transações via chat.  
  - Validar cálculo de aporte sugerido e recomendação de ativo por meta.  
  - Simular alertas de não atingimento e escalonamento após 3 meses.  
  - Confirmar que o perfil de investidor influencia corretamente as recomendações.  
Tom educativo e linguagem acessível, em português.
# Questionário de Perfil de Investidor
1. Qual é o seu principal objetivo com os investimentos?
a) Preservar o capital, evitando oscilações.  
b) Obter rentabilidade superior à poupança, aceitando alguma oscilação.  
c) Buscar alta rentabilidade, mesmo com risco elevado.  

2. Qual é o prazo médio dos seus objetivos financeiros?
a) Curto prazo (até 2 anos).  
b) Médio prazo (2 a 5 anos).  
c) Longo prazo (mais de 5 anos).  

3. Como você reagiria a uma queda de 20% no valor dos seus investimentos?
a) Ficaria muito preocupado e retiraria o dinheiro.  
b) Manteria os investimentos, esperando recuperação.  
c) Aproveitaria para investir mais, buscando ganhos futuros.  

4. Qual é o seu nível de conhecimento sobre investimentos?
a) Baixo: conheço apenas produtos básicos (poupança, CDB).  
b) Médio: já investi em fundos ou títulos públicos.  
c) Alto: tenho experiência em ações, fundos multimercado ou derivativos.  

5. Qual percentual do seu patrimônio você está disposto a investir em produtos de maior risco?
a) Até 10%.  
b) Entre 10% e 30%.  
c) Acima de 30%.  

---

# Lógica de Classificação

- **Conservador**: maioria das respostas em "a".  
  Perfil focado em segurança e liquidez. Recomendação: Tesouro Selic, CDB com liquidez diária, fundos conservadores.  

- **Moderado**: maioria das respostas em "b".  
  Perfil equilibrado, aceita alguma oscilação em busca de rentabilidade. Recomendação: Tesouro IPCA, fundos multimercado conservadores, debêntures.  

- **Agressivo**: maioria das respostas em "c".  
  Perfil disposto a assumir riscos para buscar maior retorno. Recomendação: ações, ETFs, fundos multimercado agressivos, previdência de renda variável.  

# Observações
- Se houver empate entre categorias, considerar o prazo das metas como critério de desempate.  
- O resultado deve ser armazenado no cadastro do cliente e usado para sugerir ativos compatíveis com cada meta.  
Esse questionário simples e direto deve ser implementado facilmente como parte do fluxo de onboarding.

# Lista de Ativos Sugeridos por Prazo e Perfil
## Perfil Conservador
- Curto prazo (até 2 anos):
  - Tesouro Selic
  - CDB com liquidez diária
  - Fundos DI
- Médio prazo (2 a 5 anos):
  - Tesouro IPCA+ curto
  - LCIs/LCA de bancos sólidos
  - Fundos de renda fixa indexados à inflação
- Longo prazo (mais de 5 anos):
  - Tesouro IPCA+ longo
  - Previdência conservadora (renda fixa)
  - Debêntures incentivadas de baixo risco

## Perfil Moderado
- Curto prazo (até 2 anos):
  - Tesouro Selic
  - CDBs com liquidez diária
  - Fundos multimercado conservadores
- Médio prazo (2 a 5 anos):
  - Tesouro IPCA+ médio
  - Fundos multimercado balanceados
  - Debêntures incentivadas
- Longo prazo (mais de 5 anos):
  - Tesouro IPCA+ longo
  - Previdência balanceada (multimercado)
  - Fundos de ações com gestão ativa

## Perfil Agressivo
- Curto prazo (até 2 anos):
  - Tesouro Selic (para reserva de liquidez)
  - Fundos multimercado de maior risco
- Médio prazo (2 a 5 anos):
  - Fundos multimercado agressivos
  - ETFs de renda variável
  - Debêntures de maior risco
- Longo prazo (mais de 5 anos):
  - Ações individuais
  - ETFs de índices (Ibovespa, S&P500)
  - Fundos de ações setoriais
  - Previdência agressiva (renda variável)
 - Criptomoedas

Interações com o Lovable
. Crie um aplicativo com base no meu PRD - Product Requirements Document (Documento de Requisitos do Produto).
Produto: Duarte Valore {PRD} 
.Não gostei dessas cores, use tons mais leves, tá muito escuro.
.No chat você pode atualizar e colocar os aportes também. Quando eu disser "Carro Novo" adicione o valor na meta e coloque na categoria "Investimentos" lá nas despesas.

- Resultado Final no Lovable: https://savvy-chat-invest.lovable.app/

- <img width="1920" height="869" alt="image" src="https://github.com/user-attachments/assets/b49cbf7c-6689-40a6-a294-881a019d7263" />
 <img width="805" height="776" alt="image" src="https://github.com/user-attachments/assets/6e1ff9b3-a0e9-4d8b-908b-206d4a7ee284" />
 <img width="440" height="941" alt="image" src="https://github.com/user-attachments/assets/e7018af4-8fd8-4624-ae1a-6d480e425ac0" />
<img width="468" height="865" alt="image" src="https://github.com/user-attachments/assets/c0cef2cf-eae6-4e5d-b917-aaef0d89794d" />
<img width="465" height="1008" alt="image" src="https://github.com/user-attachments/assets/a287636b-2e2d-4627-a164-71926c00a054" />
<img width="443" height="1446" alt="image" src="https://github.com/user-attachments/assets/bf22bb39-0514-4753-b788-645c2a1bac38" />
<img width="534" height="863" alt="image" src="https://github.com/user-attachments/assets/375b6389-e11a-44ba-9806-612e55d21c93" />
<img width="587" height="865" alt="image" src="https://github.com/user-attachments/assets/59664703-0a1d-4ffe-ba17-34eefe8a8759" />


# Resumo da funcionalidade do aplicativo: 
A intenção é usar esse aplicativo como valor agregado ao serviço de gestão de carteira e não apenas controle de receitas e despesas.
Criei uma aba para objetivos financeiros e sugestões de ativos para investir, de acordo com a análise do perfil do investidor e do prazo para o atingimento da meta.
Pedi para criar algo visual para classificar quão perto o cliente está de atingir cada meta para incentivá-lo no progresso. 
Adicionei um link direto para falar com a assessoria em caso de dúvidas ou aperfeiçoamento da gestão dos ativos.

# Reflexão sobre o processo: 
No início eu achei que seria muito mais difícil a parte prática, pensei que iria me atrapalhar em termos técnicos e códigos necessários. 
No fim das contas, achei muito mais fácil. Basta ter bem desenhado na mente o que você quer e saber pedir para a IA. Minha meta era deixar o PRD mais explicado possível para não precisar fazer muitos ajustes.
Pedi para corrigir a questão das cores que inicialmente não gostei, classificar os aportes em "Investimentos". 
Minhas interações terminaram, mas com o uso do aplicativo senti a necessidade de corrigir algumas questões. Por exemplo, a classificação de despesas não está bem clara e o aplicativo adiciona muitas despesas em "Outros". A próxima atualização no aplicativo será nesse sentido. Sinto que não incluí essas questões no PRD. No mais, gostei muito do primeiro resultado. 
Eu aprendi que conversar com a IA é como conversar com uma criança super dotada, tem que explicar bem o que você quer para a "criança" entender e ela retorna com muito mais conteúdo do que imaginamos. É um mundo de possibilidades e eu estou cada vez mais encantada. 

# 💬 Conclusão

Vibe Coding é sobre clareza, curiosidade e criatividade, não sobre perfeição técnica. O verdadeiro objetivo aqui é aprender a pensar junto com a IA, transformando ideias em conceitos reais e enxergando a tecnologia como uma extensão do seu raciocínio criativo. Cada interação é um experimento, quanto mais clara for sua intenção, mais surpreendente será o resultado.
