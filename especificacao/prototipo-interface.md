# Protótipo de Interface

## Objetivo
Este artefato apresenta uma proposta visual da interface do sistema de eventos, organizada a partir dos fluxos descritos no documento de fluxo de processo.

## Visão Geral do Protótipo
A interface é composta por telas que representam os principais cenários do sistema: visualização de eventos, inscrição, cancelamento, confirmação de pagamento, acompanhamento de vagas e emissão de certificados.

## Cenário 1 — Visualização de eventos
### Tela 1: Página inicial de eventos
- Cabeçalho com menu: Eventos, Minhas Inscrições, Certificados.
- Lista de eventos com nome, data, local e status de vagas.
- Filtro por categoria e tipo de evento.

```text
[Menu] Eventos | Minhas Inscrições | Certificados
[Busca] Buscar evento...
[Card] Workshop de UX
[Card] Palestra de Arquitetura
[Card] Oficina de Segurança
```

## Cenário 2 — Detalhes do evento e inscrição
### Tela 2: Detalhes do evento
- Informações do evento, descrição, vagas disponíveis e prazo de cancelamento.
- Botão "Inscrever-se".
- Se o evento for pago, exibe opção de pagamento.

```text
[Voltar] [Nome do Evento]
Descrição
Data | Horário | Local
Vagas: 12 disponíveis
Prazo de cancelamento: até 48h antes
[Inscrever-se]
```

### Tela 3: Inscrição confirmada ou pendente
- Se gratuito: exibe confirmação imediata.
- Se pago: exibe status "Pagamento pendente" até a confirmação.

```text
[Status da inscrição]
Confirmada / Pendente
[Comprovante] Baixar comprovante
[Voltar para eventos]
```

## Cenário 3 — Lista de espera e conflitos de agenda
### Tela 4: Lista de espera
- Exibe mensagem quando o evento estiver lotado.
- Permite entrar na lista de espera.

```text
Evento lotado
Você foi adicionado à lista de espera.
[Ver posição na fila]
```

### Tela 5: Conflito de workshops
- Informa que o participante já possui inscrição em workshop no mesmo horário.

```text
Conflito de horário
Este workshop não pode ser selecionado porque há sobreposição com outra atividade.
[Voltar]
```

## Cenário 4 — Cancelamento
### Tela 6: Minhas inscrições
- Lista as inscrições ativas e o status de cada uma.
- Botão para cancelar inscrição, quando permitido.

```text
Minhas Inscrições
[Evento A] Confirmada [Cancelar]
[Workshop B] Pendente [Cancelar]
```

### Tela 7: Cancelamento realizado ou bloqueado
- Se dentro do prazo: confirma cancelamento e libera vaga.
- Se fora do prazo: exibe regra aplicável.

```text
Cancelamento realizado
A vaga foi liberada.
ou
Cancelamento não permitido
O prazo foi encerrado.
```

## Cenário 5 — Acompanhamento financeiro e reembolso
### Tela 8: Pagamentos e reembolsos
- Exibe pagamentos pendentes, confirmados e reembolsos solicitados.

```text
Financeiro
Pagamento pendente
Reembolso solicitado
[Atualizar status]
```

## Cenário 6 — Certificados
### Tela 9: Certificados disponíveis
- Exibe certificados liberados após conclusão do evento ou confirmação de participação.

```text
Meus Certificados
[Certificado do Evento A]
[Certificado do Workshop B]
```

## Relação com o fluxo de processo
- A tela inicial e a tela de detalhes suportam o fluxo de visualização e inscrição.
- A tela de inscrição e de lista de espera representam o fluxo de validação de vagas e pagamento.
- As telas de minhas inscrições e cancelamento representam o fluxo de cancelamento.
- A tela de pagamentos e reembolsos representa o fluxo financeiro.
- A tela de certificados representa o encerramento do ciclo de participação.

## Observações
- O protótipo deve ser validado com participantes, organizadores e equipe financeira.
- As telas podem ser refinadas conforme novas regras e dúvidas forem esclarecidas.
