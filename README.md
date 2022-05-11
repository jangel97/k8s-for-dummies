# Kubernetes for dummies
This repository contains notes and Ansible playbooks to manage a Kubernetes cluster.

# Objectives
- Provide our own custom version of Kubernetes the hard way for dummies.
- Provide tooling and examples on how to manage infrastructure and systems as code via Ansible.
- Provide examples on how to build and deploy Kubernetes applications. 
- Provide best practices to secure Kubernetes cluster and applications.
- Provide material to prepare the Kubernetes certifications via Ansible playbooks and documentation.  

# Project structure
```bash
.
├── ansible/
│   └── collections/
│       └── customizer/
│           └── contabo/
│               ├── docs/
│               ├── galaxy.yml
│               ├── plugins/
│               │   └── README.md
│               ├── README.md
│               └── roles/
├── infrastructure/
│   ├── config-as-code/
│   ├── infra-as-code/
│   │   └── README.md
│   └── README.md
├── LICENSE
└── README.md
```

# Possible Improvements
- Infra as code could be managed via Terraform. Terraform is a declarative tool whereas Ansible is imperative. Please, bear in mind that everything as code should be managed using declarative directives.

#### Notes
The maintainers of this repository are very dummy and need their own documentation to properly do Kubernetes stuff.