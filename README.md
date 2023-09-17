# Projeto Infra as Code

Passo 1: Utilize a network-stack.yml no CloudFormation para configurar a VPCId e as SubnetIds Publicas e Privadas.

Passo 2: Utilize o ecs-wordpress-stack.yml no CloudFormation para iniciar o provisionamento dos recursos para hopedagem do WordPress com banco de dados MySQL.

Parametros a serem definidos pelo usuario:

      VPCId:
        VPC que você deseja provisionar os recursos.
      PrivateSubnetIds:
        Selecione 2 sub-redes privadas para os recursos serem configurados.
      PublicSubnetIds:
        Selecione 2 sub-redes públicas para os recursos serem configurados.
      DatabaseInstanceClass:
        Instancia EC2 que deve ser usada para o banco de dados.
      DatabaseAllocatedStorage:
        Quantidade de armazenamento (em gigabytes) que deve ser alocada para o banco de dados.
      DatabaseMaxAllocatedStorage:
        Quantidade máxima (em gigabytes) que o Amazon RDS pode dimensionar automaticamente o armazenamento do banco de dados.
      DatabaseBackupRetentionPeriod:
        Quanto tempo os backups automatizados do banco de dados devem ser mantidos.
      EnableDatabaseMultiAZ:
        Se o banco de dados deve ser implantado em diversas zonas de disponibilidade.
      EnableDatabaseReadReplica:
        Ativar uma replica de leitura.
      DatabaseCredentialsRotationSchedule:
        Frequencia em que as credenciais do banco de dados devem ser alteradas.
      EnableEFSAutomaticBackups:
        Ativar backup automatico dos dados do sistema de arquivos (EFS).
      EFSPerformanceMode:
        Modo de desempenho deve ser usado para o sistema de arquivos.
      EFSThroughputMode:
        Modo de transferencia deve ser usado para o sistema de arquivos.
      EFSProvisionedThroughput:
        Taxa de transferencia provisionada caso o modo de transferencia selecionado seja provisionado.
      CustomDomain:
        Especificar um dominio personalizado.
      CustomDomainCertificateARN:
        Certificado ARN do dominio personalizado.
      ECSTaskvCPU:
        vCPU que a tarefa deve usar.
      ECSTaskMemory:
        Memoria que a tarefa deve usar.
      ECSLogRetentionPeriod:
        Tempo em que os logs de eventos devem ser retidos.
      ECSServiceAutoScalingMetric:
        Metrica a ser usada para auto scaling.
      ECSServiceAutoScalingTargetValue:
        Valor que a metrica deve usar para auto scaling, caso seja uso da cpu sera uma porcentagem de uso.
      ECSServiceAutoScalingTargetMinCapacity:
        Capacidade minima desejada para o auto scaling.
      ECSServiceAutoScalingTargetMaxCapacity:
        Capacidade maxima desejada para o auto scaling.


![arquitetura](arquitetura.png)
