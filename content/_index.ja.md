+++
title = "自己紹介"
+++

## 自己紹介

ネットワーク、通信アーキテクチャ、およびネットワークのセキュリティとプライバシーを専門とするソフトウェアエンジニアです。
2018年1月より[株式会社Zettant](https://www.zettant.com/)の主任研究員として在籍しています。
また、2026年1月より[東京科学大学 情報理工学院 情報工学系](https://educ.titech.ac.jp/cs/)の准教授を務めています。
2020年1月から2025年12月まで[兵庫県立大学 大学院情報科学研究科](https://www.u-hyogo.ac.jp/gsis/)の准教授を務めました。
2006年4月から2017年12月まで、KDDI株式会社および株式会社KDDI総合研究所（現KDDI Research, Inc.）にて、セキュリティ・応用数学・ネットワークアーキテクチャの研究開発および戦略立案に従事しました。
2013年から2014年にかけてPalo Alto Research Center（PARC、米国カリフォルニア州）、2022年にCyLab, Carnegie Mellon University（米国ペンシルバニア州）に客員研究員として在籍しました。
東京工業大学にて工学の学士（2004年）、修士（2006年）、博士（2012年）を取得しています。

詳細なCVは[こちら（PDF）](/cv/cv-en.pdf)からご覧いただけます。

現在の主な研究テーマ：

- DNS（ドメインネームシステム）および関連するインターネットサービスにおけるプライバシーとセキュリティ
- 新たなコンピューティング・ネットワークアーキテクチャと「セキュリティ・バイ・デザイン」。特に、エッジコンピューティングのアーキテクチャとそのセキュリティ・プライバシー（安全なネットワーク内通信・計算の理論的枠組み、プライバシー保護計算など）に関心があります。
- 情報指向ネットワーク（Named-data networking; NDN）とその新しいセキュリティ機構
- 符号理論を用いた情報セキュリティ・プライバシー技術（秘密分散、プライベート情報検索など）

---

## ソフトウェア開発プロジェクト

主にFLOSS（フリー/リブレ・オープンソースソフトウェア）プロジェクトです。

- **Mutualized Oblivious DNS（μODNS）**: 匿名化DNSプロジェクト — [プロジェクトページ](/ja/dns)
- **rpxy**: TLS終端対応・複数ドメイン名対応の超高速リバースプロキシ（Rust実装）— [GitHub](https://github.com/junkurihara/rust-rpxy) / [https://rpxy.io](https://rpxy.io)
- **rpxy-l4**: プロトコルマルチプレクサ付きレイヤ4（TCP+UDP）リバースプロキシ（Rust実装）— [GitHub](https://github.com/junkurihara/rust-rpxy-l4)
- **rust-gd**: Generalized Deduplicationのrust実装 — [GitHub](https://github.com/junkurihara/rust-gd)
- **jscu**: JavaScriptユニバーサル暗号ライブラリ — [GitHub](https://github.com/junkurihara/jscu)
- その他 [GitHub](https://github.com/junkurihara) 参照

---

## 主要論文

### 符号理論およびセキュリティ技術への応用

- K. Nakano, J. Kurihara and T. Tanaka, "Extensive study on the security of private information delivery from coded storage," *IEICE Transactions on Fundamentals*, vol. E109-A, no. 3, pp. 725--733, Mar. 2026. [[JSTAGE](https://doi.org/10.1587/transfun.2025EAP1094)] \[[paper](/repo/sita-2025-paper.pdf)\] \[[slides](/repo/sita-2025-slides.pdf)\]
- I. Kurihara, J. Kurihara and T. Tanaka, "A New Security Measure in Secret Sharing Schemes and Secure Network Coding," *IEEE Access*, vol. 12, pp. 69163--69171, May 2024. [[IEEE Xplore](https://doi.org/10.1109/ACCESS.2024.3401471)]
- J. Kurihara, T. Nakamura and R. Watanabe, "Private Information Retrieval from Coded Storage in the Presence of Omniscient and Limited-Knowledge Byzantine Adversaries," *IEICE Trans. Fundamentals*, vol. E104-A, no. 9, pp. 1271--1283, Sep. 2021. \[[pdf](/repo/ieice-e104-a_9_1271.pdf)\]
- J. Kurihara, R. Matsumoto and T. Uyematsu, "Relative Generalized Rank Weight of Linear Codes and Its Applications to Network Coding," *IEEE Trans. Information Theory*, vol. 61, no. 7, pp. 3912--3936, Jul. 2015. [[arXiv](https://arxiv.org/abs/1301.5482)] \[[slides](/repo/sita-2014_slides.pdf)\]
- J. Kurihara, T. Uyematsu and R. Matsumoto, "Secret Sharing Schemes Based on Linear Codes Can Be Precisely Characterized by the Relative Generalized Hamming Weight," *IEICE Trans. Fundamentals*, vol. E95-A, no. 11, pp. 2067--2075, Nov. 2012. \[[pdf](/repo/ieice-e95-a_11_2067.pdf)\]
- J. Kurihara, S. Kiyomoto, K. Fukushima and T. Tanaka, "On a Fast (k,n)-threshold Secret Sharing Scheme," *IEICE Trans. Fundamentals*, vol. E91-A, no. 9, pp. 2365--2378, Sep. 2008. \[[pdf](/repo/ieice-e91-a_09_2365.pdf)\]

### 新ネットワーク・コンピューティングアーキテクチャとそのセキュリティ

- R. Watanabe, A. Kubota, J. Kurihara, and K. Sakurai, "Extension of Resource Authorization Method with SSI in Edge Computing," *Proc. AINA 2024*, vol. 6, pp. 385--394, Apr. 2024.
- J. Kurihara, T. Tanaka and T. Kubo, "μODNS: A Distributed Approach to DNS Anonymization with Collusion Resistance," *Computer Networks*, Elsevier, vol. 237, p. 110078, Dec. 2023. [[ScienceDirect](https://doi.org/10.1016/j.comnet.2023.110078)] \[[pdf](/repo/computer-networks_237_110078.pdf)\]
- R. Watanabe, A. Kubota and J. Kurihara, "Application of Generalized Deduplication Techniques in Edge Computing Environments," *Proc. AINA 2023*, pp. 585--596, Mar. 2023.
- J. Kurihara, K. Yokota and A. Tagami, "List Interest: Simply Packing Interests Dramatically Reduces Router Workload in Content-Centric Networking," *IEICE Trans. Communications*, vol. E99-B, no. 12, pp. 2520--2531, Dec. 2016. \[[pdf](/repo/ieice-e99-b_12_2520.pdf)\]
- J. Kurihara, K. Yokota and A. Tagami, "A Consumer-driven Access Control Approach to Censorship Circumvention in Content-Centric Networking," in *Proc. ACM ICN 2016*, Sep. 2016, pp. 186--194. [[sigcomm.org](http://conferences2.sigcomm.org/acm-icn/2016/proceedings/p186-kurihara.pdf)]

---

## 担当講義

- 情報リテラシー1・2（2026年度 1Q-2Q、東京科学大学 学部）
- セキュリティエンジニアリング特論（2020〜2025年度 秋学期、兵庫県立大学 大学院情報科学研究科）
- ネットワークセキュリティ特論（2021〜2025年度 春学期、兵庫県立大学 大学院情報科学研究科）
- 情報セキュリティ科学概論（2021〜2025年度 春学期、兵庫県立大学 大学院情報科学研究科）
- 情報セキュリティ（2023〜2025年度 秋学期、兵庫県立大学 社会情報科学部）

---

## 獲得資金

- NSF-NICT JUNO 3、2022〜2025年度（Co-PI）
- KDDI財団 研究助成、2022〜2024年度（PI）
- JSPS科研費：
  - 基盤研究（B）、2025〜2028年度（PI）
  - 基盤研究（C）、2022〜2025年度（PI）
  - 基盤研究（B）、2021〜2024年度（分担；PI：小泉佑揮 准教授、大阪大学）
  - 研究活動スタート支援、2020〜2022年度（PI）
- 兵庫県立大学 若手研究者特別研究助成、2021年度（PI）、2020年度（PI）

---

## リンク

[GitHub](https://github.com/junkurihara) &nbsp;|&nbsp;
[LinkedIn](https://www.linkedin.com/in/junkurihara/) &nbsp;|&nbsp;
[Google Scholar](https://scholar.google.co.jp/citations?user=e0XuwAoAAAAJ&hl=ja) &nbsp;|&nbsp;
[Researchmap](https://researchmap.jp/junkurihara) &nbsp;|&nbsp;
[Speaker Deck](https://speakerdeck.com/junkurihara) &nbsp;|&nbsp;
[研究室](https://secarchlab.github.io)

---

## 連絡先

[LinkedInページ](https://www.linkedin.com/in/junkurihara/)よりメッセージをお送りいただくか、最近の論文に記載のメールアドレスよりご連絡ください。
