# Monitoring Stack

Este repositório contém a configuração do stack de monitoramento usando:
- Prometheus
- Grafana
- Alertmanager

## Estrutura
```
monitoring/
├── bootstrap.yaml        # Configuração bootstrap do Argo CD
└── charts/
    └── monitoring-stack.yaml  # Configuração do stack de monitoramento
```

## Instalação

1. Primeiro, aplique o bootstrap no cluster:
```bash
kubectl apply -f bootstrap.yaml
```

2. O Argo CD irá automaticamente sincronizar e aplicar todas as configurações.

## Acessos

- Grafana: http://localhost:3000 (admin/admin123)
- Prometheus: http://localhost:9090
- Alertmanager: http://localhost:9093

## Manutenção

Para atualizar as configurações:
1. Faça as alterações necessárias nos arquivos YAML
2. Commit e push para o repositório
3. O Argo CD detectará as mudanças e aplicará automaticamente 