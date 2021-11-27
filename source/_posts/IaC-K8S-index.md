---
title: "[目錄頁] 以 IaC 與 CaC 在 GCP 上自動建立高可用的 K8S 平台，並使用 Grafana, Loki, Prometheus 監測方案"
subtitle: 此頁為 K8S 與 IaC 等等的技術專欄目錄頁
date: 2021-11-26 23:47:09
tags:
  - 目錄
  - IaC
  - K8S
  - GCP
  - GSDC
  - Loki
  - Ansible
  - Grafana
  - Terraform
  - Prometheus
comment: valine
excerpt: 此頁為技術專欄的目錄頁，會介紹如何以 IaC 與 CaC 在 GCP 上自動建立高可用的 K8S 平台，並使用 Grafana, Loki, Prometheus 監測方案，且會一步步的帶著讀者使用 Ansible 自動建立 K8S 平台
---

## 簡介

此頁為技術專欄的目錄頁，會介紹如何以 IaC 與 CaC 在 GCP 上自動建立高可用的 K8S 平台，並使用 Grafana, Loki, Prometheus 監測方案，且會一步步的帶著讀者自動地建立 K8S 平台~

K8S 是目前很流行的容器編排平台，而當前的微服務及某些工具很多都是透過該平台來實現快速的水平擴展與彈性的部署，並且基於該平台還可以搭配 istio, linkerd 等 service mesh 工具實現像是金絲雀, 藍綠等部署策略來部署應用。
但也是因為它的功能強大，造成維運的複雜度增加。因此本期專欄將先從各種基礎元件介紹，並搭配使用 Terraform 這類的 Infrastructure as Code(IaC) 工具在 GCP 上建立要使用的 Infra，接著是使用 Ansible 這種的 Configuration as Code 快速地部署高可用的 K8S 叢集。
一般來說建立 K8S 叢集後並不會在沒有監控的情況下使用，因此我們會使用 Grafana, Loki, Prometheus 去監測叢集的狀態，以確保叢集的健康狀態。
那麼本期專欄將會以每兩週一次的頻率更新技術專欄並介紹以上的內容，以讓讀者可以了解 Iac, CaC 並在 GCP 上擁有維運和自動化建置 K8S 叢集的能力。

## 目標

- 學習 K8S 的基本概念
- 了解如何作出具備 HA 架構的 K8S 叢集，以及基本的 Container Network Interface
- 學習如何基於 Google Cloud Platform 架設出 K8S 叢集
- 學習如何在 K8S 上架設一套應用，並使其可被監測
- 了解為何要有 IaC, CaC，並且如何透過它解決維運問題以及優化整體部署流程
- 學習如何使用 Terrafrom 在 Google Cloud Platform 上自動建立所需主機
- 學習如何使用 Ansible 去自動化部署 K8S 叢集

## 使用工具與平台

- 架設平台
  - [Google Cloud Platform](https://console.cloud.google.com/)
- IaC 與 CaC
  - [Ansible](https://www.ansible.com/)
  - [Terraform](https://www.terraform.io/)
- 監控元件
  - [Loki](https://grafana.com/oss/loki/)
  - [Grafana](https://grafana.com/oss/grafana/)
  - [Prometheus](https://prometheus.io/)
- Kubernetes 相關
  - [Kubernetes](https://kubernetes.io/)
  - [Kubeadm](https://github.com/kubernetes/kubeadm)
  - [Kubespray](https://github.com/kubernetes-sigs/kubespray)
  - [K9s](https://k9scli.io/)
  - [Helm](https://helm.sh/)

## 文章目錄

- 預計 12/12 更新，主題為 `K8S 概念理解`
