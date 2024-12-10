# les-crd-k8s
# CRD Couramment Intégrées aux Clusters Kubernetes

## 1. CRD pour le réseau et la sécurité
| **CRD**               | **Description**                                                              |
|------------------------|------------------------------------------------------------------------------|
| `GlobalNetworkPolicy`  | Règles réseau globales pour tout le cluster (Calico).                       |
| `NetworkPolicy`        | Règles réseau pour un namespace spécifique (Calico/Canal).                 |
| `IPPool`               | Plages d'adresses IP utilisées par les pods (Calico).                      |
| `BGPPeer`              | Pairing BGP pour la connectivité inter-clusters (Calico).                  |
| `HostEndpoint`         | Points de terminaison réseau des nœuds ou interfaces spécifiques (Calico).  |

---

## 2. CRD pour les certificats
| **CRD**             | **Description**                                                               |
|---------------------|-------------------------------------------------------------------------------|
| `Certificate`       | Définit un certificat TLS à gérer (Cert-Manager).                            |
| `ClusterIssuer`     | Émetteur de certificats pour tout le cluster (Cert-Manager).                 |
| `Issuer`            | Émetteur de certificats limité à un namespace (Cert-Manager).               |

---

## 3. CRD pour le monitoring et l’observabilité
| **CRD**             | **Description**                                                               |
|---------------------|-------------------------------------------------------------------------------|
| `Prometheus`        | Configuration d'une instance Prometheus (Prometheus Operator).               |
| `Alertmanager`      | Gestion des alertes (Prometheus Operator).                                   |
| `ServiceMonitor`    | Collecte des métriques d'un service spécifique (Prometheus Operator).        |
| `PodMonitor`        | Collecte des métriques des pods (Prometheus Operator).                       |
| `GrafanaDashboard`  | Déploiement de tableaux de bord Grafana personnalisés (Grafana Operator).    |

---

## 4. CRD pour les sauvegardes et le stockage
| **CRD**             | **Description**                                                               |
|---------------------|-------------------------------------------------------------------------------|
| `VolumeSnapshot`    | Capture instantanée d'un volume persistant (CSI).                            |
| `Backup`            | Sauvegarde des données du cluster (Velero).                                  |
| `Restore`           | Restauration des données d'une sauvegarde (Velero).                          |
| `CephCluster`       | Gestion des clusters Ceph pour le stockage (Rook).                           |
| `LonghornVolume`    | Gestion des volumes persistants (Longhorn).                                  |

---

## 5. CRD pour la gestion des workflows
| **CRD**             | **Description**                                                               |
|---------------------|-------------------------------------------------------------------------------|
| `Workflow`          | Gestion des workflows (Argo Workflows).                                      |
| `CronWorkflow`      | Planification des workflows récurrents (Argo Workflows).                     |
| `PipelineRun`       | Exécution de pipelines CI/CD (Tekton Pipelines).                             |
| `TaskRun`           | Exécution de tâches spécifiques dans un pipeline (Tekton Pipelines).         |

---

## 6. CRD pour les bases de données
| **CRD**             | **Description**                                                               |
|---------------------|-------------------------------------------------------------------------------|
| `PgCluster`         | Gestion des clusters PostgreSQL (CrunchyData Operator).                      |
| `MongoDBCommunity`  | Gestion des clusters MongoDB (MongoDB Community Operator).                   |
| `MySQLCluster`      | Gestion des clusters MySQL (MySQL Operator).                                 |

---

## 7. CRD pour les événements et les messages
| **CRD**             | **Description**                                                               |
|---------------------|-------------------------------------------------------------------------------|
| `KafkaCluster`      | Gestion des clusters Kafka (Strimzi Operator).                               |
| `RabbitmqCluster`   | Gestion des clusters RabbitMQ (RabbitMQ Operator).                           |
| `EventBus`          | Gestion des événements (Knative Eventing).                                   |

---

## 8. CRD pour la sécurité et la gouvernance
| **CRD**             | **Description**                                                               |
|---------------------|-------------------------------------------------------------------------------|
| `ClusterPolicy`     | Gestion des politiques globales de sécurité (Kyverno, Gatekeeper).           |
| `Policy`            | Politiques de sécurité au niveau du namespace (Kyverno, Gatekeeper).         |
| `VaultSecret`       | Gestion des secrets stockés dans HashiCorp Vault (Vault Operator).           |

---

## Commandes Utiles

### Lister toutes les CRD disponibles
```bash
kubectl get crd
