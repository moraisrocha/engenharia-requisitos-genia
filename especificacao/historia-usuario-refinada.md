# Histórias de Usuário Refinadas com Critérios de Aceitação

## Visão Geral
Este artefato organiza as principais histórias de usuário do sistema de gestão de eventos, com base nos requisitos funcionais, regras de negócio e dúvidas levantadas na fase de análise.

## Histórias de Usuário

### HU-01 — Visualizar eventos
**Como** participante  
**Quero** visualizar todos os eventos disponíveis em um único local  
**Para que** eu possa escolher facilmente as atividades de meu interesse.

**Critérios de aceitação**
- Sucesso: a interface exibe todos os eventos disponíveis em uma lista ou catálogo único.
- Sucesso: cada evento apresenta informações básicas como nome, data, horário e categoria.
- Falha: se não houver eventos cadastrados, o sistema exibe uma mensagem clara informando a ausência de atividades.

### HU-02 — Inscrever-se em eventos e workshops
**Como** participante  
**Quero** me inscrever em eventos e workshops  
**Para que** eu participe das atividades desejadas.

**Critérios de aceitação**
- Sucesso: o sistema permite inscrição em eventos gratuitos e pagos.
- Sucesso: para eventos pagos, a inscrição só é confirmada após aprovação do pagamento.
- Falha: se houver conflito de horário ou dados inválidos, o sistema impede a inscrição e informa o motivo.

### HU-03 — Emitir comprovante de inscrição
**Como** participante  
**Quero** receber um comprovante de inscrição imediatamente após confirmar a inscrição  
**Para que** eu tenha registro da minha participação.

**Critérios de aceitação**
- Sucesso: o sistema gera e disponibiliza o comprovante logo após a confirmação da inscrição.
- Sucesso: o comprovante contém identificação do evento, data e status da inscrição.
- Falha: se a inscrição não for confirmada, o sistema não gera o comprovante e informa o motivo.

### HU-04 — Cancelar inscrição
**Como** participante  
**Quero** cancelar minha inscrição dentro do prazo definido  
**Para que** eu não precise entrar em contato manualmente com a organização.

**Critérios de aceitação**
- Sucesso: o participante consegue cancelar a inscrição pela própria interface.
- Sucesso: o sistema valida se a cancelamento está dentro do prazo permitido.
- Falha: se a inscrição estiver fora do prazo, o sistema impede o cancelamento e informa a regra aplicável.

### HU-05 — Emitir certificado
**Como** participante  
**Quero** emitir meu certificado após o evento  
**Para que** eu tenha comprovante de participação.

**Critérios de aceitação**
- Sucesso: o certificado é disponibilizado somente após confirmação de participação ou conclusão do evento.
- Sucesso: o sistema gera o certificado de forma automática, quando aplicável.
- Falha: se a participação não for confirmada, o sistema não disponibiliza o certificado.

### HU-06 — Inscrever-se em vários workshops no mesmo dia
**Como** participante  
**Quero** me inscrever em diversos workshops no mesmo dia  
**Para que** eu possa participar de mais de uma atividade sem conflito.

**Critérios de aceitação**
- Sucesso: o sistema permite inscrição em múltiplos workshops, desde que não haja conflito de horário.
- Sucesso: quando houver sobreposição, o sistema impede a seleção do workshop conflitante.
- Falha: se o participante tentar inscrever-se em atividades simultâneas, o sistema bloqueia a ação e apresenta uma mensagem de aviso.

### HU-07 — Controlar vagas disponíveis
**Como** organizador  
**Quero** controlar automaticamente as vagas disponíveis dos eventos  
**Para que** eu possa evitar excesso de inscrições e manter a capacidade adequada.

**Critérios de aceitação**
- Sucesso: o sistema atualiza automaticamente a quantidade de vagas disponíveis após cada inscrição ou cancelamento.
- Sucesso: quando o evento atingir a capacidade, o sistema exibe a situação de lotado.
- Falha: se ocorrer inconsistência nos dados, o sistema registra o erro e não permite nova inscrição sem correção.

### HU-08 — Criar lista de espera
**Como** organizador  
**Quero** criar automaticamente uma lista de espera quando um evento estiver lotado  
**Para que** eu possa organizar novas inscrições de forma ordenada.

**Critérios de aceitação**
- Sucesso: ao atingir a capacidade, o sistema cria automaticamente uma lista de espera para novas inscrições.
- Sucesso: a lista de espera mantém a ordem de entrada das solicitações.
- Falha: se a lista não for criada corretamente, o sistema informa o problema e impede novas inscrições pendentes.

### HU-09 — Acompanhar inscritos em tempo real
**Como** organizador  
**Quero** acompanhar, em tempo real, a quantidade de inscritos por evento  
**Para que** eu possa monitorar a demanda e tomar decisões rapidamente.

**Critérios de aceitação**
- Sucesso: o sistema exibe a quantidade atual de inscritos para cada evento em tempo real.
- Sucesso: a informação é atualizada automaticamente após novas inscrições ou cancelamentos.
- Falha: se o sistema não conseguir atualizar os dados, o organizador visualiza uma mensagem de indisponibilidade.

### HU-10 — Consultar lista de participantes
**Como** organizador  
**Quero** consultar a lista de participantes inscritos em minhas atividades  
**Para que** eu possa realizar o acompanhamento das atividades sob minha responsabilidade.

**Critérios de aceitação**
- Sucesso: o organizador consegue visualizar a lista de participantes de cada atividade vinculada a ele.
- Sucesso: a lista exibe informações relevantes para o acompanhamento da atividade.
- Falha: se o usuário não tiver permissão, o sistema bloqueia o acesso e exibe mensagem de autorização negada.

### HU-11 — Confirmar pagamento e liberar inscrição
**Como** equipe financeira  
**Quero** confirmar pagamentos e liberar inscrições de eventos pagos  
**Para que** eu possa garantir que as inscrições sejam validadas corretamente.

**Critérios de aceitação**
- Sucesso: o sistema bloqueia ou aguarda confirmação do pagamento antes de liberar a inscrição em eventos pagos.
- Sucesso: após a confirmação, a inscrição passa para status confirmado.
- Falha: se o pagamento não for validado, a inscrição permanece pendente e não é liberada.

### HU-12 — Acompanhar reembolsos
**Como** equipe financeira  
**Quero** acompanhar reembolsos de eventos pagos  
**Para que** eu possa registrar e gerenciar as solicitações de forma controlada.

**Critérios de aceitação**
- Sucesso: o sistema permite registrar e acompanhar reembolsos conforme a política da organização.
- Sucesso: o status do reembolso é atualizado e visível para a equipe financeira.
- Falha: se a solicitação não for compatível com a política, o sistema impede o reembolso e informa o motivo.

### HU-13 — Acessar o sistema com segurança
**Como** participante ou organizador  
**Quero** acessar o sistema com segurança  
**Para que** meus dados pessoais e minhas operações fiquem protegidos.

**Critérios de aceitação**
- Sucesso: o sistema exige autenticação para acessar áreas restritas.
- Sucesso: o sistema concede acesso apenas às funcionalidades permitidas para cada perfil.
- Falha: se o usuário tentar acessar dados não autorizados, o sistema bloqueia a ação e registra a tentativa.

### HU-14 — Utilizar uma interface acessível e intuitiva
**Como** participante, organizador ou equipe financeira  
**Quero** utilizar uma interface clara, intuitiva e acessível  
**Para que** eu consiga realizar minhas tarefas com eficiência e sem barreiras.

**Critérios de aceitação**
- Sucesso: a interface apresenta navegação clara, textos compreensíveis e elementos acessíveis.
- Sucesso: as principais ações são identificadas com facilidade em diferentes dispositivos.
- Falha: se a interface dificultar o uso, o sistema deve oferecer mecanismos de orientação ou mensagens de ajuda.

### HU-15 — Garantir disponibilidade do sistema
**Como** usuário do sistema  
**Quero** que o sistema esteja disponível durante os horários operacionais  
**Para que** eu possa realizar inscrições e consultas sem interrupções significativas.

**Critérios de aceitação**
- Sucesso: o sistema permanece disponível nos horários previstos para a operação dos eventos.
- Sucesso: em caso de falha, o sistema exibe mensagem de indisponibilidade e registra o incidente.
- Falha: se houver interrupções frequentes, o sistema deve gerar alerta para a equipe responsável.
