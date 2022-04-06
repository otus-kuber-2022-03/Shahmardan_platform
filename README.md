# Выполнено ДЗ № 1

- [ ] Основное ДЗ
  - Разберитесь почему все pod в namespace kube-system восстановились после удаления. Укажите причину в описании PR
  
  ``` sh
    ~ % kubectl get pods -n kube-system
    coredns-64897985d-5j8jn            1/1     Running   0          40m
    etcd-minikube                      1/1     Running   3          40m
    kube-apiserver-minikube            1/1     Running   3          40m
    kube-controller-manager-minikube   1/1     Running   3          40m
    kube-proxy-thcpm                   1/1     Running   0          40m
    kube-scheduler-minikube            1/1     Running   3          40m
  
  ```

[static Pods](https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/):
*kube-apiserver-minikube, kube-controller-manager-minikube,kube-controller-manager-minikube, kube-proxy-thcpm, kube-scheduler-minikube* restarted by **kubelet**

[ReplicationController](https://kubernetes.io/docs/concepts/workloads/controllers/replicationcontroller/#what-is-a-replicationcontroller)
*coredns-64897985d-5j8jn*

- [ ] Задание со *