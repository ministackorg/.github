<div align="center">

<img src="https://ministack.org/og-image.png" alt="MiniStack" width="640" />

# The best AWS emulator & LocalStack alternative

**Free. Open source. MIT. Forever.**
60+ AWS services. One container. One port. No account, no telemetry, no tiers.

[![Website](https://img.shields.io/badge/website-ministack.org-0ea5e9?style=flat-square)](https://ministack.org)
[![PyPI](https://img.shields.io/pypi/v/ministack?style=flat-square&color=3776AB)](https://pypi.org/project/ministack/)
[![Docker](https://img.shields.io/badge/docker-ministackorg%2Fministack-2496ED?style=flat-square&logo=docker&logoColor=white)](https://hub.docker.com/r/ministackorg/ministack)
[![License: MIT](https://img.shields.io/badge/license-MIT-22c55e?style=flat-square)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://pypi.org/project/ministack/)
[![GitHub stars](https://img.shields.io/github/stars/ministackorg/ministack?style=flat-square&color=facc15)](https://github.com/ministackorg/ministack)

[**Quickstart**](#-quickstart) ·
[**Ecosystem**](#-the-ecosystem) ·
[**Why MiniStack**](#-why-ministack) ·
[**Community**](#-community)

</div>

---

## ⚡ Quickstart

```bash
pip install ministack && ministack
```

or:

```bash
docker run -p 4566:4566 ministackorg/ministack
```

Point any AWS SDK / CLI / CDK / Terraform at `http://localhost:4566`:

```bash
aws --endpoint-url=http://localhost:4566 s3 mb s3://hello
aws --endpoint-url=http://localhost:4566 dynamodb list-tables
```

Done. No login, no cloud account, no credit card.

---

## 🧱 The Ecosystem

| Project | What it is | Status |
| --- | --- | --- |
| 🟢 **[ministack](https://github.com/ministackorg/ministack)** | The emulator. 60+ AWS services on `:4566`. Drop-in LocalStack replacement. | **Stable** |
| 🟢 **[ministack-mcp](https://github.com/ministackorg/ministack-mcp)** | Model Context Protocol server — give Claude/Cursor/Copilot live access to the MiniStack service catalog and AWS parity data. | **Stable** |
| 🟢 **[testcontainers-ministack](https://github.com/ministackorg/testcontainers-ministack)** | Testcontainers module. Spin MiniStack inside any JVM/Python/Node test suite. | **Stable** |
| 🟢 **[ministack-power](https://github.com/ministackorg/ministack-power)** | Learn and test AWS with MiniStack inside the [Kiro IDE](https://kiro.dev). | **Stable** |
| 🟠 **[miniflake](https://github.com/ministackorg/miniflake)** | Local Snowflake emulator powered by DuckDB. Same DNA, different cloud. | **Preview** |
| 🔵 **v1.4.0** | Multi-region · Amazon Bedrock (Converse, Agents, Knowledge Bases, Guardrails) · Amazon MSK | **Coming** |

---

## 🚀 Why MiniStack

### Real AWS parity
Wire shape verified against `botocore` for every operation we ship — request/response field names, types, error codes, HTTP status codes, headers, SigV4 scopes, ARN formats, eventstream framing. boto3, AWS CLI, CDK, Terraform, openai-python, anthropic-sdk-python — they can't tell us from AWS at the API boundary.

### Lean by design
One container. One port. No JVM. No background daemons. Stdlib-only runtime. Heavy data planes (Kafka, Spark, LLMs) plug in by env-var passthrough to your own infra — we don't bundle what you don't need.

### Free, forever
MIT. No "pro" tier, no feature gates, no telemetry, no upsell. If it works for you, [⭐ the repo](https://github.com/ministackorg/ministack) is the only thanks needed.

### Built for the real toolchain
✅ Terraform · ✅ AWS CDK · ✅ AWS SAM · ✅ CloudFormation · ✅ Pulumi · ✅ boto3 / AWS SDK for every language · ✅ Testcontainers · ✅ docker-compose · ✅ GitHub Actions · ✅ GitLab CI

---

## 🧰 What's inside

<details open>
<summary><b>Compute, Storage, Database, Messaging, Networking, Identity, Observability, IaC, AI/ML</b> — 60+ services</summary>

| Category | Services |
| --- | --- |
| **Compute** | Lambda (warm containers, layers, ESMs, Durable Functions) · ECS · EKS · Batch · EMR |
| **Storage** | S3 (versioning · checksums · replication) · EFS · S3 Tables (Iceberg REST) |
| **Database** | DynamoDB (transactions · streams) · RDS (Postgres + MySQL backed) · ElastiCache |
| **Messaging** | SQS · SNS · Kinesis · EventBridge · Pipes · Firehose |
| **Networking** | API Gateway v1/v2 + WebSocket · ALB/ELBv2 · Route53 · ACM · AppSync (GraphQL + Events) |
| **Identity** | IAM · STS · Cognito (idp + identity) · Secrets Manager · KMS |
| **Observability** | CloudWatch · CloudWatch Logs · CloudTrail |
| **Orchestration** | Step Functions · MWAA · Glue · Scheduler |
| **Other** | CodeBuild · ECR · CloudFront · WAF v1/v2 · IoT · MediaConnect · Transfer (SFTP) · Inspector2 · ServiceDiscovery · ResourceGroups · SSM · Organizations · Account · CUR · Backup · AutoScaling · APIGW v1 / v2 · CFN |
| **Coming v1.4** | 🔵 **Bedrock** (foundation models, Converse, InvokeModel, Agents, Knowledge Bases, Guardrails, Mantle/OpenAI-shape) · 🔵 **MSK** (Amazon Managed Streaming for Kafka) · 🔵 **Multi-region** |

</details>

---

## 💬 Community

<div align="center">

[![Website](https://img.shields.io/badge/-ministack.org-0ea5e9?style=for-the-badge&logo=googlechrome&logoColor=white)](https://ministack.org)
[![GitHub Discussions](https://img.shields.io/badge/-Discussions-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ministackorg/ministack/discussions)
[![Issues](https://img.shields.io/badge/-Issues-d4263e?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ministackorg/ministack/issues)
[![Reddit](https://img.shields.io/badge/-r%2Fministack-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/r/ministack/)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/ministackorg/)
[![Docker Hub](https://img.shields.io/badge/-Docker%20Hub-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/r/ministackorg/ministack)

</div>

**Built by MiniStackers, for MiniStackers. Welcome ❤️**

---

<div align="center">

*Free. Open source. MIT. **Forever.***
*Star us on GitHub if MiniStack saves you cloud bills.*

</div>
