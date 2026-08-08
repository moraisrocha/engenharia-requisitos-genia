# Matriz de Rastreabilidade

## Objetivo
Esta matriz relaciona requisitos funcionais, regras de negócio, histórias de usuário e artefatos de especificação para garantir cobertura e rastreabilidade do projeto.

## Requisitos Funcionais
| ID | Requisito Funcional | História de Usuário | Artefato Relacionado | Observação |
|----|---------------------|---------------------|-----------------------|------------|
| RF-001 | Permitir visualizar todos os eventos disponíveis em um único local | HU-01 | Histórias de usuário, Protótipo de interface | Requisito inicial de navegação e consulta |
| RF-002 | Permitir inscrição em eventos e workshops | HU-02 | Histórias de usuário, Protótipo de interface | Relacionado à regra RNG-001 |
| RF-003 | Emitir comprovante de inscrição após confirmação | HU-03 | Histórias de usuário, Protótipo de interface | Garante registro imediato do participante |
| RF-004 | Permitir cancelamento de inscrição dentro do prazo | HU-04 | Histórias de usuário, Diagrama de fluxo | Relacionado à regra RNG-003 |
| RF-005 | Permitir emissão de certificado após o evento | HU-05 | Histórias de usuário, Matriz de rastreabilidade | Dependente de confirmação de participação |
| RF-006 | Permitir inscrição em vários workshops no mesmo dia, sem conflito | HU-06 | Histórias de usuário, Diagrama de fluxo | Relacionado à regra RNG-004 |
| RF-007 | Controlar automaticamente as vagas disponíveis | HU-07 | Diagrama de fluxo, Matriz de rastreabilidade | Requisito operacional essencial |
| RF-008 | Criar automaticamente lista de espera quando houver lotação | HU-08 | Diagrama de fluxo, Matriz de rastreabilidade | Vinculado à regra RNG-002 |
| RF-009 | Permitir acompanhamento em tempo real do número de inscritos | HU-09 | Diagrama de fluxo, Matriz de rastreabilidade | Apoia a gestão dos organizadores |
| RF-010 | Permitir consulta da lista de participantes das atividades | HU-10 | Histórias de usuário, Protótipo de interface | Requisito de gestão e controle |
| RF-011 | Bloquear ou aguardar confirmação do pagamento antes de liberar inscrição | HU-11 | Diagrama de fluxo, Matriz de rastreabilidade | Requisito financeiro e de validação |
| RF-012 | Permitir acompanhamento de reembolsos | HU-12 | Matriz de rastreabilidade | Relacionado à regra RNG-006 |

## Regras de Negócio
| ID | Regra de Negócio | História de Usuário | Artefato Relacionado | Observação |
|----|-------------------|---------------------|-----------------------|------------|
| RNG-001 | Eventos gratuitos permitem inscrição imediata; eventos pagos dependem de confirmação do pagamento | HU-02, HU-11 | Histórias de usuário, Diagrama de fluxo | Define o comportamento inicial da inscrição |
| RNG-002 | Quando o evento atingir a capacidade, as inscrições adicionais entram em lista de espera | HU-07, HU-08 | Diagrama de fluxo, Matriz de rastreabilidade | Regras de controle de vagas |
| RNG-003 | Cancelamentos só são permitidos dentro do prazo definido pela organização | HU-04 | Histórias de usuário, Diagrama de fluxo | Requisito de política de cancelamento |
| RNG-004 | Workshops no mesmo horário não podem ser inscritos simultaneamente pelo mesmo participante | HU-06 | Histórias de usuário, Diagrama de fluxo | Evita conflitos de agenda |
| RNG-005 | Certificados são emitidos somente após confirmação de participação ou conclusão do evento | HU-05 | Histórias de usuário, Matriz de rastreabilidade | Vincula emissão de certificado à participação |
| RNG-006 | Reembolsos são concedidos somente em situações previstas pela política da organização | HU-12 | Matriz de rastreabilidade | Regras financeiras a serem validadas |

## Histórias de Usuário
| ID | História de Usuário | Requisito(s) Vinculado(s) | Artefato Relacionado | Observação |
|----|---------------------|---------------------------|-----------------------|------------|
| HU-01 | Eu como participante quero visualizar todos os eventos disponíveis para que eu possa escolher facilmente as atividades de meu interesse | RF-001 | Histórias de usuário, Protótipo de interface | História base da navegação de eventos |
| HU-02 | Eu como participante quero me inscrever em eventos e workshops para que eu participe das atividades desejadas | RF-002, RNG-001 | Histórias de usuário, Protótipo de interface | História principal de inscrição |
| HU-03 | Eu como participante quero receber um comprovante de inscrição para que eu tenha registro da minha participação | RF-003 | Histórias de usuário, Protótipo de interface | Vinculada à confirmação da inscrição |
| HU-04 | Eu como participante quero cancelar minha inscrição dentro do prazo definido para que eu não precise entrar em contato manualmente com a organização | RF-004, RNG-003 | Histórias de usuário, Diagrama de fluxo | Garante autonomia do participante |
| HU-05 | Eu como participante quero emitir meu certificado após o evento para que eu tenha comprovante de participação | RF-005, RNG-005 | Histórias de usuário, Matriz de rastreabilidade | Relacionada ao encerramento do processo |
| HU-06 | Eu como participante quero me inscrever em diversos workshops no mesmo dia para que eu possa participar de mais de uma atividade sem conflito | RF-006, RNG-004 | Histórias de usuário, Diagrama de fluxo | Garante compatibilidade de agenda |
| HU-07 | Eu como organizador quero controlar automaticamente as vagas disponíveis para que eu possa evitar excesso de inscrições e manter a capacidade adequada | RF-007, RNG-002 | Diagrama de fluxo, Matriz de rastreabilidade | História de gestão de capacidade |
| HU-08 | Eu como organizador quero criar automaticamente uma lista de espera quando um evento estiver lotado para que eu possa organizar novas inscrições de forma ordenada | RF-008, RNG-002 | Diagrama de fluxo, Matriz de rastreabilidade | História de organização de fila |
| HU-09 | Eu como organizador quero acompanhar em tempo real a quantidade de inscritos por evento para que eu possa monitorar a demanda rapidamente | RF-009 | Diagrama de fluxo, Matriz de rastreabilidade | História de acompanhamento operacional |
| HU-10 | Eu como organizador quero consultar a lista de participantes inscritos em minhas atividades para que eu possa realizar o acompanhamento adequado | RF-010 | Histórias de usuário, Protótipo de interface | História de gestão de participantes |
| HU-11 | Eu como equipe financeira quero confirmar pagamentos e liberar inscrições de eventos pagos para que eu possa garantir que as inscrições sejam validadas corretamente | RF-011, RNG-001 | Diagrama de fluxo, Matriz de rastreabilidade | História de validação financeira |
| HU-12 | Eu como equipe financeira quero acompanhar reembolsos para que eu possa registrar e gerenciar as solicitações de forma controlada | RF-012, RNG-006 | Matriz de rastreabilidade | História de controle financeiro |

## Requisitos Não Funcionais
| ID | Requisito Não Funcional | História de Usuário | Artefato Relacionado | Observação |
|----|--------------------------|---------------------|-----------------------|------------|
| RNF-001 | Oferecer tempo de resposta adequado para consulta, inscrição e atualização de dados | HU-02, HU-03, HU-09 | Histórias de usuário, Diagrama de fluxo | Relacionado à performance do sistema |
| RNF-002 | Proteger dados pessoais por meio de autenticação, autorização e controle de acesso | HU-13 | Histórias de usuário, Protótipo de interface | Requisito de segurança |
| RNF-003 | Manter integridade e rastreabilidade das inscrições, pagamentos, cancelamentos e certificados | HU-03, HU-05, HU-12 | Histórias de usuário, Matriz de rastreabilidade | Garante confiabilidade dos registros |
| RNF-004 | Disponibilizar interface clara, intuitiva e acessível | HU-01, HU-14 | Histórias de usuário, Protótipo de interface | Requisito de usabilidade e acessibilidade |
| RNF-005 | Manter disponibilidade compatível com os horários de operação dos eventos | HU-15 | Histórias de usuário, Diagrama de fluxo | Requisito de disponibilidade |

## Observações
- A matriz deve ser revisada sempre que novas regras, dúvidas ou requisitos forem esclarecidos.
- Cada requisito funcional, regra de negócio e requisito não funcional agora possui vínculo com pelo menos uma história de usuário e um artefato de especificação.
