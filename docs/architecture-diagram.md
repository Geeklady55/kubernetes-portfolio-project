\# Architecture Diagram



\## High-Level Flow



```text

User Browser

&#x20;   |

&#x20;   v

kubectl port-forward / NodePort Service

&#x20;   |

&#x20;   v

Kubernetes Service (nginx-service)

&#x20;   |

&#x20;   v

Kubernetes Deployment (nginx-deployment)

&#x20;   |

&#x20;   v

Pods (2 replicas)

&#x20;   |

&#x20;   v

Nginx Container

