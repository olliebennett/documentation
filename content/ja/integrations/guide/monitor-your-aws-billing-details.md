---
aliases:
- /ja/integrations/faq/how-do-i-monitor-my-aws-billing-details
kind: ガイド
title: AWS の請求の詳細を監視する
---

Datadog-AWS Billing インテグレーションを利用することで、AWS から請求メトリクスを収集することができます。

詳細は、こちらのアプリ内でご確認ください:
https://app.datadoghq.com/account/settings#integrations/amazon_billing

請求メトリクスの収集を開始するには

1. [AWS 構成タイル][1]で "Billing" を選択し、Datadog の AWS ポリシーに `budgets:ViewBudget` という権限を入れてください。

2. [AWS コンソール][2]内で請求メトリクスを有効にします。

Datadog-AWS Billing インテグレーションを使用すると、以下のメトリクスを利用できます。

| 名前                            | 単位   | 説明                                                                                                                                        |
| -----                           | ------  | ------                                                                                                                                             |
| `aws.billing.actual_spend`      | ドル | 予算期間中の実際の支出コスト                                                                                                   |
| `aws.billing.budget_limit`      | ドル | 予算期間中の支出限度額                                                                                                          |
| `aws.billing.estimated_charges` | ドル | AWS の使用量に応じた見積もり料金です。これは、1 つのサービスの見積もり料金、またはすべてのサービスの見積もり料金のロールアップのいずれかにすることができます。 |
| `aws.billing.forecasted_spend`  | ドル | 予算期間中の予測の支出コスト                                                                                               |

AWS に加え、多くのクラウドサービスにまたがるより強固なコスト監視のために、Datadog は [CloudHealth][3] とサードパーティーのインテグレーションをサポートしています。[CloudHealth][3] がどのように Datadog とインテグレーションし、ホストされたインフラストラクチャー全体のコストを可視化するかについては、[このブログ記事][4]でより詳しく解説しています。

[1]: /ja/integrations/amazon_web_services/
[2]: http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html#turning_on_billing_metrics
[3]: /ja/integrations/cloudhealth/
[4]: https://www.datadoghq.com/blog/monitor-cloudhealth-assets-datadog