---
services: functions, event-grid, cosmos-db
platforms: dotnet
author: nzthiago
---

# Content Reactor: Serverless Microservice Sample for Azure

In this sample, we have built four microservices that use an [Event Grid](https://docs.microsoft.com/en-us/azure/event-grid/overview) custom topic for inter-service eventing, and a front-end Angular.js app that uses [SignalR](https://www.asp.net/signalr) to forward Event Grid events to the user interface in real time.

This sample includes detailed documentation for explaining
all aspects of the system architecture as well as the processes you should use to 
develop the solution in either a start-up or enterprise enterprise environment.

* **Getting Started**
1. [Setup your machine, create and azure account, and get a Big Huge Thesaurus API Key.](/_docs/developing/setup.md) on your machine.
2. Determine an Azure-globally unique naming prefix that: 
    * contains only lowercase letters and numbers (no spaces or numbers).
    * is globally unique in Azure when suffixes are added (like `-web`, `-events`, etc.)
3. In PowerShell:

        git clone https://github.com/Stewartarmbrecht/Serverless-Eventing-Platform-for-Microservices.git
        cd ./Serverless-Eventing-Platform-for-Microservices
        az login
        # if you do not want to use your default subscription:
        az account set --subscription {your-subscription-id}
        ./scripts/buildanddeploy.ps1 -namePrefix {your-globall-unique-naming-prefix} -region westus2 -bigHugeThesaurusApiKey {your-api-key}
4. Navigate to the app: `http://{your-globall-unique-naming-prefix}-web-app.azurewebsites.net` and try it out.


_The last `buildanddeploy.ps1` script will take a long time to run for the first time.  Enjoy watching the output!_

* **Overview**
    * [Functionality](/_docs/overview/functionality.md)
    * [Architecture](/_docs/overview/architecture.md)

* **Developing**
    * [Setup](/_docs/developing/setup.md)
    * [Development Flow](/_docs/developing/development-flow.md)
    * [Building](/_docs/developing/building.md)
    * [Coding](/_docs/developing/coding.md)
    * [Testing](/_docs/developing/testing.md)
    * [Debugging](/_docs/developing/debugging.md)
    * [Documenting](/_docs/developing/documenting.md)
    * [Deploying](/_docs/developing/deploying.md)
    * [Troubleshooting](/_docs/monitoring/troubleshooting.md)
    * [Contributing](/_docs/monitoring/contributing.md)

* **Releasing**
    * [Continuous Integration](/_docs/releasing/continuous-integration.md)
    * [Continuous Deployment](/_docs/releasing/continuous-deployment.md)

* **Monitoring**
    * [Health Checks](/_docs/monitoring/health-checks.md)
    * [Application Monitoring](/_docs/monitoring/application-monitoring.md)
    * [End User Monitoring](/_docs/monitoring/end-user-monitoring.md)
    * [Alerting](/_docs/monitoring/alerting.md)
    * [Troubleshooting](/_docs/monitoring/troubleshooting.md)

* **Governing**
    * [Product Management](/_docs/governing/product-management.md)
    * [Design](/_docs/governing/design.md)
    * [Architecture](/_docs/governing/architecture.md)
    * [Infrastructure](/_docs/governing/infrastructure.md)
    * [Release Management](/_docs/governing/pipeline.md)
    * [Compliance](/_docs/governing/compliance.md)
    * [Legal](/_docs/governing/legal.md)
    * [Risk](/_docs/governing/risk.md)
    * [Internal Audit](/_docs/governing/internal-audit.md)
