Design of Plasma Globe

- Plasma Store on Kubernetes

- [Daemonset](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/) to initialize plasma store, plasma manager, and lean API server

- Use host path to mount shared memory across pods

  - https://kubernetes.io/docs/concepts/storage/volumes/#hostpath

- Primary reference:

  - https://groups.google.com/forum/#!msg/kubernetes-dev/iBUBJ4ZPLSM/OqsvN3VNEQAJ

- Shared memory inside pods

  - either all container mount to the same shared memory on host/node

  - or: 

    - ```
      emptyDir:
          medium: Memory
      ```

    - https://docs.openshift.org/latest/dev_guide/shared_memory.html

- Detail plasma configuration: https://github.com/ray-project/ray/issues/1315



