# k3d-lab

Rôle Ansible pour déployer automatiquement un cluster Kubernetes léger avec **k3d** et un service **NGINX** personnalisé.

## Prérequis

- Conteneur Ubuntu avec le socket Docker monté (`/var/run/docker.sock`)
- Ansible >= 2.10

## Variables

| Variable | Défaut | Description |
|---|---|---|
| `k3d_cluster_name` | `k3d-lab` | Nom du cluster |
| `k3d_servers` | `1` | Nombre de serveurs |
| `k3d_agents` | `1` | Nombre d'agents |
| `k3d_nodeport` | `30080` | Port NodePort exposé |
| `nginx_replicas` | `1` | Nombre de réplicas NGINX |
| `welcome_message` | `Bienvenue dans le k3d LAB` | Message de la page d'accueil |

## Utilisation

```yaml
- hosts: client1
  become: true
  roles:
    - k3d-lab
```

## Auteur

YanisHDD
