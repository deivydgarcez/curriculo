# Estudos em Andamento

Skills identificadas como gap para vagas DevOps/Cloud em grandes empresas.

---

## Kubernetes (K8s)
Orquestração de containers — presente em praticamente toda vaga DevOps/SRE/Cloud de empresa de médio/grande porte.

**Recursos:**
- Documentação oficial: https://kubernetes.io/docs/home/
- Curso gratuito: KodeKloud (Kubernetes for Beginners)
- Prática local: Minikube ou Kind

**Conteúdo-alvo:**
- Pods, Deployments, Services, ConfigMaps, Secrets
- Namespaces, RBAC, Ingress
- Helm Charts
- EKS (AWS Elastic Kubernetes Service) — conexão direta com stack AWS já conhecida

---

## Terraform
Infrastructure as Code (IaC) — padrão para provisionamento de infra AWS/Azure/GCP em grandes empresas. Substitui criação manual de recursos.

**Recursos:**
- Documentação oficial: https://developer.hashicorp.com/terraform/docs
- Curso gratuito: HashiCorp Learn (Terraform on AWS)
- Prática: provisionar EC2, S3, Lambda já conhecidos via código

**Conteúdo-alvo:**
- HCL básico (providers, resources, variables, outputs)
- State file e remote backend (S3 + DynamoDB)
- Modules
- Terraform com AWS (IAM, EC2, Lambda, VPC)

---

## Prioridade sugerida
1. **Terraform primeiro** — curva menor, aproveita o conhecimento AWS que já tem
2. **Kubernetes depois** — mais complexo, mas o Docker já listado no CV é a base
