# CFS (Completely Fair Scheduler)

## 説明

CFS（Completely Fair Scheduler）は、Linuxカーネルで採用されているプロセススケジューリング方式で、すべてのプロセスに「公平なCPU時間」を与えることを目的としています。
従来の優先度ベースのスケジューラとは異なり、CFSは厳密なタイムスライスを使用しません。代わりに、各プロセスがどれだけCPUを利用したかを記録し、その使用量が少ないプロセスから順に実行する仕組みになっています。これにより、処理が重いプロセスでも軽いプロセスでも、CPU時間が偏らずに与えられるようになります。

また、CFSは内部的に 赤黒木（Red-Black Tree） と呼ばれるデータ構造を使用しており、CPU使用量が最も少ないプロセスを効率よく取り出せる点も特徴です。
その結果、多くのプロセスが同時に動作する環境でも、公平性・応答性・安定性を維持できる優れたスケジューラとなっています。

## 参考文献

Linux Kernel Documentation – Scheduler（https://www.kernel.org/doc/html/latest/scheduler/index.html）

Red Hat Developer – How the Completely Fair Scheduler works（https://developers.redhat.com）

## 作成者

- 氏名: 萩原大城
- 学籍番号: G384722023
- 作成日: 2025-11-15
- 最終更新日: 2025-11-15