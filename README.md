# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 12 de Janeiro de 2026  
**Empresa:** Abstergo Industries  
**Responsável:** [Gustavson Menezes]

## Introdução

Este relatório apresenta o processo de implementação de ferramentas AWS na empresa Abstergo Industries, realizado por [Gustavson Menezes]. O objetivo do projeto foi selecionar 3 serviços AWS para redução imediata de custos, com foco no contexto de uma farmácia.

## Descrição do Projeto

O projeto foi dividido em 3 etapas, cada uma com objetivos específicos:

### Etapa 1: Otimização de Armazenamento com Amazon S3 Intelligent-Tiering

- **Click-Farma:** Amazon S3 Intelligent-Tiering  
- **Foco:** Redução de custos de armazenamento por meio da automação da movimentação de dados entre classes de armazenamento do S3, baseada nos padrões de acesso.  
- **Caso de uso:** Farmácias geram grandes volumes de dados (registros de pacientes, prescrições, inventário). Muitos desses dados são acessados com frequência no início, mas tornam-se menos acessados com o tempo. O S3 Intelligent-Tiering monitora automaticamente os padrões de acesso e move os dados para classes mais econômicas (como S3 Standard-IA ou S3 Glacier Instant Retrieval) quando o acesso diminui, sem impacto no desempenho ou disponibilidade.

### Etapa 2: Automação de Processos com AWS Lambda

- **Nome da ferramenta:** AWS Lambda  
- **Foco:** Execução de código sem provisionar ou gerenciar servidores (serverless), pagando apenas pelo tempo de computação consumido. Ideal para cargas de trabalho orientadas a eventos e processamento em tempo real.  
- **Caso de uso:** Processamento automático de eventos como novas prescrições digitais, atualizações de estoque ou notificações de reabastecimento. Exemplo: uma função Lambda pode ser acionada quando um novo arquivo de prescrição é carregado no S3, processando-o e atualizando o sistema da farmácia. Elimina a necessidade de servidores dedicados, reduzindo custos operacionais.

### Etapa 3: Otimização de Custo de Computação com Amazon EC2 Graviton

- **Nome da ferramenta:** Amazon EC2 com processadores AWS Graviton  
- **Foco:** Instâncias de computação de alto desempenho e baixo custo, otimizadas para cargas de trabalho nativas da nuvem, com melhor relação preço/desempenho em comparação com instâncias x86.  
- **Caso de uso:** Migração de sistemas de gestão de farmácia (ERP), bancos de dados de pacientes ou aplicações de análise para instâncias Graviton pode gerar economias de até 40% em custos de computação, mantendo ou melhorando o desempenho. Ideal para sistemas legados que não podem ser convertidos para arquitetura serverless.

## Conclusão

A implementação do Amazon S3 Intelligent-Tiering, AWS Lambda e Amazon EC2 Graviton na Abstergo Industries resulta na **redução imediata e contínua dos custos operacionais, otimização do uso de recursos e aumento da eficiência na gestão de dados e processos**. Recomenda-se a continuidade do uso das ferramentas e a busca por novas tecnologias para aprimorar ainda mais os processos da empresa.



**Assinatura:**  
[Gustavson Menezes]
