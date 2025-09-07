# Guia Prático de Gerenciamento de Custos no Azure

## Projeto Custos no Azure - Bootcamp AZ900

Gerenciar os gastos na nuvem Azure de forma prática é um processo contínuo que se divide em duas grandes fases: a **estimativa e o planejamento** antes da implantação, e o **monitoramento e otimização** após os recursos estarem em produção. Abordaremos detalhadamente as ferramentas e conceitos para cada uma dessas etapas em um fluxo coeso.

## Fase 1: Estimativa e Planejamento (Pré-Implantação)

A jornada de otimização de custos começa antes mesmo de migrar ou criar um único recurso, utilizando as ferramentas de planejamento do Azure.

### Calculadora de Custo Total de Propriedade (TCO)

A primeira ferramenta, focada em justificar a migração, é a **Calculadora de Custo Total de Propriedade (TCO - Total Cost of Ownership)**. O objetivo desta calculadora é comparar os custos de manutenção da sua infraestrutura local (on-premises) com os custos equivalentes na Azure, demonstrando o potencial de economia.

O processo na prática envolve:
1.  **Definir as cargas de trabalho:** Você insere o inventário do seu datacenter atual (servidores Windows/Linux, bancos de dados SQL Server, armazenamento, etc.), detalhando CPUs, RAM e o tipo de carga de trabalho.
2.  **Ajustar as suposições:** Você refina custos ocultos do ambiente local, como o preço da eletricidade, os salários da equipe de TI e custos de aquisição de hardware/software.
3.  **Aplicar o Benefício Híbrido do Azure:** Se sua empresa possui licenciamento com **Software Assurance** ativo, você pode usar essas licenças na nuvem, pagando apenas pela infraestrutura base e gerando uma economia drástica.

Ao final, a ferramenta gera um relatório detalhado que mostra a economia total ao longo do tempo, comparando item por item.

### Calculadora de Preços

Enquanto a Calculadora TCO responde "por que migrar?", a **Calculadora de Preços** responde "quanto exatamente vai custar o que eu quero construir?". Ela serve para obter uma estimativa detalhada para novas arquiteturas.

Ao estimar o preço de uma máquina virtual, por exemplo, você precisa configurar diversas variáveis:
* **Região** (os preços variam globalmente)
* **Sistema Operacional**
* **Tamanho da instância** (vCPUs e RAM)
* **Tipo de armazenamento** (SSD Premium, SSD Standard, etc.)
* **Modelo de pagamento** (**Pay-as-you-go**, **Instâncias Reservadas** ou **Planos de Economia**)

Para ambientes de Dev/Test, assinaturas como **MSDN (Visual Studio Subscriptions)** oferecem créditos mensais, permitindo testes sem impactar o faturamento.

## Fase 2: Monitoramento e Otimização (Pós-Implantação)

Uma vez que os recursos estão em execução, a gestão de custos torna-se uma atividade contínua, realizada através da ferramenta **Microsoft Cost Management and Billing**.

### Análise de Custos

A funcionalidade de **Análise de Custos** é o seu painel central de visibilidade. Nela, você pode:
* Visualizar gastos atuais e projetados.
* Detalhar custos por assinatura, grupo de recursos ou serviço.
* Filtrar custos por **tags**. A prática de "tagear" (etiquetar) todos os recursos com informações como centro de custo ou projeto é fundamental para uma alocação eficaz.

### Alertas de Custos

Para evitar surpresas na fatura, a criação de **alertas de custos** é indispensável. Você pode criar **orçamentos (budgets)** para um determinado escopo (assinatura, grupo de recursos) e configurar limites de notificação para quando os gastos atingirem um percentual do valor orçado (ex: 80% ou 100%). Isso transforma o gerenciamento de custos de uma análise histórica para uma abordagem proativa.

## Conclusão

Gerenciar os gastos no Azure é um ciclo virtuoso de **estimar** com precisão usando as calculadoras, **monitorar** de perto com a Análise de Custos, **controlar** proativamente com orçamentos e alertas e, finalmente, usar os insights obtidos para **otimizar** os recursos e refinar as estimativas futuras.
