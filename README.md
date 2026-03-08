# Projeto DevSecOps - JPetStore

Projeto de implementação DevSecOps completo para deploy de aplicação Java (JPetStore) usando:

- **Jenkins** - CI/CD
- **Docker** - Containerização
- **Kubernetes** - Orquestração
- **Terraform** - Infraestrutura como Código
- **Maven 3.9.9** - Build
- **SonarQube** - Análise de código
- **Trivy** - Segurança de containers
- **Ansible** - Automação

## Estrutura do Projeto

```
projeto-java/
├── terraform/        # Infraestrutura AWS (EC2, Security Groups)
│   └── main.tf
└── jpetstore-6/      # Aplicação Java (Pet Store)
    ├── src/
    ├── Ansible/
    ├── deployment.yaml
    └── pom.xml
```

## Pré-requisitos

- AWS CLI configurado
- Terraform instalado
- Key Pair AWS criada
- Docker instalado
- Kubernetes (kubectl/minikube)
- Java 17+ e Maven

## Como usar

### 1. Provisionar infraestrutura

```bash
cd terraform
terraform init
terraform plan
terraform apply
```

### 2. Build da aplicação

```bash
cd jpetstore-6
mvn clean package
```

## Notas de Segurança

⚠️ **Nunca commitar:**
- Arquivos `.pem` (chaves privadas)
- Credenciais AWS
- Arquivos `terraform.tfstate`

Baseado no projeto: [DevOps-Project-25](https://github.com/NotHarshhaa/DevOps-Projects/tree/master/DevOps-Project-25)
