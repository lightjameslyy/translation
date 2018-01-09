# 云监控入门

原文作者：Angela Stringfellow

原文地址：https://dzone.com/articles/a-cloud-monitoring-primer

云监控是评估、监控和管理基于云的服务、应用程序和基础架构的过程。许多公司利用各种应用程序监视工具来监视基于云的应用程序。下面我们来看看云监控的运行机制和成功的实践。

## 要监控的云服务类型

有多种类型的云服务要监控。云监控不仅仅是监控AWS或Azure上托管的服务器。对于企业来说，他们也非常重视监控他们所使用的基于云的服务。包括Office 365和其他的服务。

- SaaS - 像Office 365，Salesforce这样的服务
- PaaS - 开发人员友好的服务，如SQL数据库，缓存，存储等
- IaaS - 由Azure，AWS，Digital Ocean等云提供商托管的服务器
- FaaS - 新的无服务器应用程序，如AWS Lambda和Azure Functions
- 应用程序托管 - Azure App Services，Heroku等服务

其中许多可以通过传统的应用程序性能监视工具进行监视。但是，云监控对基本的服务器监控工具有一些[独特的要求](https://stackify.com/cloud-monitoring-vs-server-monitoring/)。

## 云监控如何运行

“云”这个术语是指一组网络托管的应用程序，通过网络对数据进行存储和访问，而不是通过计算机的硬盘。

- 对于消费者来说，使用互联网查看网页、通过诸如Gmail等服务访问电子邮件帐户以及将文件存储在Dropbox中都是云计算为消费者提供服务的例子。
- 企业以相同的方式使用云。他们还可以使用软件即服务（SaaS）选项来订阅业务应用程序或租用服务器空间来托管专有应用程序，以向消费者提供服务。

云监控通过一系列监控运行应用程序的服务器，资源和应用程序的工具来工作。这些工具通常有两个来源：

- **来自云提供商的内部工具** - 这中方式比较简单，因为这些工具是服务的一部分。无需安装，可以无缝整合。
- **独立SaaS提供商提供的工具** - 虽然SaaS提供商可能与云服务提供商不同，但这并不意味着这两种服务无法一起正常工作。这些提供商在管理性能和成本方面也有专长。

云监控工具查找可能会阻止或限制企业向客户提供服务的问题。通常，这些工具提供有关性能，安全性和客户行为的数据：

- **网络安全**是[保护网络免受网络攻击](https://www.datapipe.com/blog/2015/04/30/cloud-monitoring-is-often-undervalued/)的必要组成部分。 IT团队可以使用它来及早发现漏洞和易受攻击的地方，并在造成无法挽回的损害之前保护网络安全。
- **通过定期进行测试**，机构可以快速发现错误并纠正错误，从而减轻对性能和功能的损害，改善客户体验，促进销售并提高客户保留率。
- **速度** —就像功能和用户体验—是客户满意度的主要驱动力。监控速度指标并生成数据可以帮助机构优化网站和应用程序。

如果一个机构及早并经常地进行监督，他们可以使用这些数据来排除问题，并及时（即便不是即时）进行修复。

## 云监控的好处

利用云监控工具的主要优势包括：

- 已经有了基础设施和配置。安装快速简单。
- 专用工具由主机维护，包括硬件。
- 这些解决方案适用于各种规模的机构。所以如果云活动增加，正确的监控工具可以无缝扩展。
- 基于订阅的解决方案可以降低成本。他们不需要负担启动或基础设施的支出，维护成本分散在多个用户之间。
- 由于资源不是该机构的服务器和工作站的一部分，因此当本地问题扰乱该机构时，它们不会受到干扰。
- 许多工具可用于多种类型的设备 - 台式电脑，平板电脑和电话。这使得各种机构可以从任何可以访问网络的位置监控应用程序和服务。

## 最佳实践

各种机构需要将云监控作为优先事项并对其进行规划。该计划应包括需要回答的问题和要实施的目标，例如：

- **确定指标和事件** - 需要监测哪些活动？并非所有可以测量的东西都需要报告。监控那些确实很重要的指标。
- **使用一个平台汇报所有的数据** - 除了要监控云服务之外，一些机构可能拥有自己的基础设施。他们需要解决方案能够在单一平台上汇报不同来源的数据，从而可以计算出统一的度量标准并获得综合性能的结果。
- **监控云服务的使用和费用** - 扩展的能力是云服务的一个关键特性，但是增加云的使用会导致成本增加。健壮的监视解决方案应该跟踪在云上活动的数量以及它的成本。
- **监控用户体验** - 组织需要了解用户在使用基于云的应用程序时的体验。通过监视指标，如响应时间和使用频率，以获得性能的完整视图。
- **使用数据触发规则** - 如果活动超过或低于定义的阈值，正确的解决方案应该能够添加或减少服务器以保持效率和性能。
- **分散和集中数据** - 机构应该将监控数据与应用程序和服务分开存储，并且应该集中起来，方便关键的涉众访问。
- **尝试失败** - 测试您的工具，看看中断或数据入侵发生的原因是什么，并在满足某些阈值时评估警报系统。

## 其他的资源和教程

如果想获得更多的信息和建议，请访问以下资源:

- [云监控与服务器监控不同的6个原因](https://stackify.com/cloud-monitoring-vs-server-monitoring/)
- [云监控工具和最佳实践指南](http://www.datacenterknowledge.com/archives/2014/03/21/guide-cloud-monitoring-tools-best-practices/)
- [监控您不拥有的云基础设施的4个最佳实践](https://www.sevone.com/white-paper/4-best-practices-monitoring-cloud-infrastructure-you-dont-own)
- [设计和实现云治理:云，云治理是新兴的能力](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=12&cad=rja&uact=8&ved=0ahUKEwj7wOPFsvzVAhXDTCYKHSv9Boo4ChAWCEUwAQ&url=https%3A%2F%2Fwww.eiseverywhere.com%2Ffile_uploads%2F8d78b669e86b0120d704469d84fbf680_CLF_2011_Governance_Frameworks_Eric_Marks.pdf&usg=AFQjCNFHtkQ-4DNbeQejXtaYLm0sAie_Ag)
- [持续的监控策略](https://cloud.gov/docs/ops/continuous-monitoring/)

对于任何使用云计算的机构来说，监控都是必须的，无论是为了安全性还是性能，但是选择合适的应用程序性能监控(APM)解决方案是很有挑战性的。阅读[这篇文章](https://stackify.com/mistakes-implementing-application-performance-monitoring-solutions/)，了解IT管理团队在评估和实现APM解决方案时所犯的常见错误。有吵闹的邻居影响你的表现?请阅读[这篇文章](https://stackify.com/how-to-monitor-noisy-cloud-neighbors-your-web-apps-using-stackifys-apm/)，了解如何使用Stackify's Retrace for APM来监控“吵闹”的云邻居和web应用程序。最后，想获取对于DevOps流动、服务器监控和云计算的一些专家见解，这次[对Sean Hull的采访](https://stackify.com/devops-movement-sean-hull-interview/)是必读的。
