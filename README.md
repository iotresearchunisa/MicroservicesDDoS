
# DDoS Attack Detection in Microservices Architectures

## Overview
This repository contains datasets and code for benchmarking and evaluating DDoS attack detection strategies in microservices applications. The datasets include both normal and malicious traffic patterns, simulating real-world scenarios with various types of attacks. The dataset is designed for training and evaluating machine learning models for intrusion detection.

## Repository Structure
```
Dataset/
├── Classic DDoS/         # Classic DDoS attack dataset
├── No attacks/            # Normal traffic dataset
├── Slow DDoS/             # Slow DDoS attack dataset
├── SYN Flood/             # SYN Flood attack dataset
├── GET Flood/             # GET Flood attack dataset
├── labels.csv             # Labels for classification

```

## Dataset Description
The datasets were collected using a microservices-based benchmark system, *TrainTicket*, under different attack scenarios and normal traffic conditions. The following attack types are included:
- **Classic DDoS**: Overwhelming traffic floods the system.
- **Slow DDoS**: Maintains open connections for extended periods to exhaust resources.
- **SYN Flood**: Exploits the TCP handshake process to overwhelm the target.
- **GET Flood**: Sends excessive HTTP GET requests to exhaust the server’s resources.

## Monitoring Metrics
### CAdvisor ([Documentation](https://github.com/google/cadvisor/blob/master/docs/storage/prometheus.md))
- **ContainerUsage**: Number of bytes consumed by the container on this filesystem.
- **CPUThrottling**: Total time duration the container has been throttled.
- **CPUUsage**: CPU quota of the container.
- **MemoryUsage**: Current memory usage, including all memory regardless of when it was accessed.
- **NetworkIO**: Cumulative count of bytes received/transmitted.
- **PacketsDropped**: Cumulative count of packets dropped while receiving.

### Kube-state-metrics ([Documentation](https://github.com/kubernetes/kube-state-metrics/blob/main/docs/metrics/workload/pod-metrics.md))
- **PodReady**: Describes whether the pod is ready to serve requests.
- **ResourceLimits**: The number of requested limit resources by a container.
- **PodStatus (Restarts)**: The number of container restarts per container.

## Authors

- [@Massimo Ficco](https://docenti.unisa.it/058291/home)
- [@Pietro Fusco](https://docenti.unisa.it/064613/home)
- [@Antonio Guerriero](https://www.docenti.unina.it/#!/professor/414e544f4e494f47554552524945524f4752524e544e39324d3036483933314c/riferimenti)
- [@Roberto Pietrantuono](https://www.docenti.unina.it/#!/professor/524f424552544f5049455452414e54554f4e4f50545252525438305332344632323448/riferimenti)
- [@Marco Russo](https://www.linkedin.com/in/marco-russo-ba4b95167/)
- [@Stefano Russo](https://www.docenti.unina.it/#!/professor/53544546414e4f525553534f52535353464e36335032304638333959/riferimenti)

## Mention our work
```
@article{DDoS_microservices,
  author    = {M. Ficco and P. Fusco and A. Guerriero and R. Pietrantuono and M. Russo and F. Palmieri and S. Russo},
  title     = {A Benchmark for DDoS Attacks Detection in Microservice Architectures},
  journal   = {ICNC 2025},
  year      = {2025}
}
```
## Acknowledgements

This work is part of the research activities realized within the projects SERICS (CUP PE00000014, under the NRRP MUR program funded by the EU - NGEUm) and FLEGREA (Federated Learning for Generative Emulation of Advanced Persistent Threats - CUP E53D23007950001, Bando PRIN 2022). The work by R. Pietrantuono, A. Guerriero, and S. Russo received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant agreement No 871342 “uDEVOPS”.
