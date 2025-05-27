# Istio Setup

Esta pasta contém a configuração do Istio gerenciada pelo Argo CD.

## Estrutura
```
istio/
├── apps/              # Configurações de aplicações do Istio
│   ├── base.yaml     # Instalação base do Istio
│   └── gateway.yaml  # Configuração do Ingress Gateway
└── README.md         # Este arquivo
```

## Componentes Instalados
- Istio Base
- Istiod (Control Plane)
- Istio Ingress Gateway

## Ordem de Instalação
1. Istio Base (CRDs e componentes base)
2. Istiod (Control Plane)
3. Ingress Gateway

A ordem é controlada através das annotations `argocd.argoproj.io/sync-wave` nos manifestos. 