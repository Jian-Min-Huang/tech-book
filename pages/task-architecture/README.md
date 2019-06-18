# 高並發任務架構設計

## Cron Trigger

* Instance 等級的鎖 \(只有 Master 能做, 可用Redis ZK DB 確立誰為 Master\)
* Method 等級的鎖 \(Shedlock for Spring Schedule, 也是用ZK、Redis、DB等作為鎖\)
* 使用Master -&gt; Multi Agent的架構

## Task

* Schedule or Quartz with Single Thread
* Kafka
* Akka
* Reactor Pub/Sub, Web Flux, WebClient
  * This model in GoLang, JS
* Google Cloud Pub/Sub

## 開獎中心

* multi-thread
* Reactor
* Coroutine
