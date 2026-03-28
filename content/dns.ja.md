+++
title = "Mutualized Oblivious DNS（μODNS）"
+++

## 概要

このページでは、**Mutualized Oblivious DNS**（μODNS）と呼ばれる新しい匿名化DNSの概念を紹介します。
実装、公開サーバー、および詳細情報は以下の通りです。

---

## 論文

### 研究論文

- ジャーナル論文（拡張版）：
  > Jun Kurihara, Toshiaki Tanaka, and Takeshi Kubo, "μODNS: A Distributed Approach to DNS Anonymization with Collusion Resistance," *Computer Networks*, Elsevier, vol. 237, p. 110078, Dec. 2023. [Online] Available at [https://doi.org/10.1016/j.comnet.2023.110078](https://doi.org/10.1016/j.comnet.2023.110078).

- 初期コンセプト論文：
  > Jun Kurihara and Takeshi Kubo, "Mutualized oblivious DNS (μODNS): Hiding a tree in the wild forest," [https://arxiv.org/abs/2104.13785v3](https://arxiv.org/abs/2104.13785v3), Jun. 2021.

### 発表スライド

- μODNS初期コンセプト：
  > 栗原 淳、久保 武志、"Mutualized Oblivious DNS (μODNS): Hiding a tree in the wild forest"、IEICE NS研究会、2021年7月（日本語）[[Slideshare]](https://www.slideshare.net/JunKurihara2/mutualized-oblivious-dns-odns-hiding-a-tree-in-the-wild-forest-249693576)

---

## Oblivious DNS over HTTPS（ODoH）を拡張した実装

このODoHベースのプロトコルおよび実装を**μODoH**または**MODoH**と呼ぶこともあります。

### Do53 — Rustで実装したμODoH変換プロキシ

- ソース：[https://github.com/junkurihara/doh-auth-proxy](https://github.com/junkurihara/doh-auth-proxy)
- Docker：[https://hub.docker.com/r/jqtype/doh-auth-proxy](https://hub.docker.com/r/jqtype/doh-auth-proxy)

### 認証・アクセス制御機能付きμODoHリレー・ターゲットサーバー

- ソース：[https://github.com/junkurihara/modoh-server](https://github.com/junkurihara/modoh-server)
- Docker：[https://hub.docker.com/r/jqtype/modoh-server](https://hub.docker.com/r/jqtype/modoh-server)

DoS攻撃からDNSサーバーとリレーを保護するため、最初のホップリレーで認証を導入しています。
認証サーバーも別途必要です：

- ソース：[https://github.com/junkurihara/rust-token-server](https://github.com/junkurihara/rust-token-server)
- Docker：[https://hub.docker.com/r/jqtype/id-token-server](https://hub.docker.com/r/jqtype/id-token-server)

### 公開リレー・サーバー

現在、実現可能性をテスト中です。

### 謝辞

ODoHからMoDoHへの拡張に関する研究は、NICT22401、JSPS科研費（課題番号JP22K11994、JP21H03442）、KDDI財団の助成を受けています。

---

## Dnscryptプロトコルに基づくPoC実装

### Do53 — μODNS変換プロキシ（`dnscrypt-proxy`のfork）

- ソース：[https://github.com/junkurihara/dnscrypt-proxy-modns](https://github.com/junkurihara/dnscrypt-proxy-modns)
- Docker：[https://hub.docker.com/r/jqtype/dnscrypt-proxy-modns](https://hub.docker.com/r/jqtype/dnscrypt-proxy-modns)

### `encrypted-dns-server`に基づくμODNSサーバー

- ソース：[https://github.com/junkurihara/encrypted-dns-server-modns](https://github.com/junkurihara/encrypted-dns-server-modns)
- Docker：[https://hub.docker.com/r/jqtype/encrypted-dns-server-modns](https://hub.docker.com/r/jqtype/encrypted-dns-server-modns)
- Docker（`unbound`リゾルバー付き）：[https://hub.docker.com/r/jqtype/dnscrypt-server-modns](https://hub.docker.com/r/jqtype/dnscrypt-server-modns)

### 公開リゾルバー・リレー

- [https://github.com/junkurihara/experimental-resolvers](https://github.com/junkurihara/experimental-resolvers)

---

## μODNSエントリとしての公開DoHサーバー

> **本サービスは現在利用できません。**
> 代わりにDo53-μODoH変換プロキシをローカルでご利用ください。

[[トップページへ戻る](/) ]
