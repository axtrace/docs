# Deleting a {{ k8s }} cluster

{% note alert %}

{% include [about-cluster-delete](../../../_includes/managed-kubernetes/note-k8s-cluster-delete.md) %}

{% endnote %}

{% include [yc-cluster-list](../../../_includes/managed-kubernetes/cluster-list.md) %}

{% list tabs %}

- Management console

  1. Open **{{ managed-k8s-name }}** in the folder you want to delete the {{ k8s }} cluster from.
  1. Click ![image](../../../_assets/vertical-ellipsis.svg) icon in the row of the {{ k8s }} cluster to be deleted.
  1. In the menu that opens, click **Delete**.
  1. In the window that opens, click **Delete**.

- CLI

  {% include [cli-install](../../../_includes/cli-install.md) %}

  1. Delete a {{ k8s }} cluster:

     ```bash
     yc managed-kubernetes cluster delete test-k8s-cluster
     .....................done
     ```

  1. Make sure that the {{ k8s }} cluster was deleted:

     ```bash
     yc managed-kubernetes cluster list
     +----+------+------------+--------+--------+-------------------+-------------------+
     | ID | NAME | CREATED AT | HEALTH | STATUS | EXTERNAL ENDPOINT | INTERNAL ENDPOINT |
     +----+------+------------+--------+--------+-------------------+-------------------+
     +----+------+------------+--------+--------+-------------------+-------------------+
     ```

- API

  To delete a {{ k8s }} cluster, use the [delete](../../api-ref/Cluster/delete.md) method for the [Cluster](../../api-ref/Cluster/) resource.

{% endlist %}