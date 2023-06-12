# SonarQube Pricing Analysis and Recommendations

## SonarQube Subscription Plans

SonarQube offers three commercial subscription plans:

1. **Developer Edition**: Starting at $150/year for a maximum analysis of 100,000 Lines of Code (LOC), up to $65K/year for 20 million LOC. The Developer Edition is the minimum required for SQL code analysis. [source](https://www.sonarsource.com/plans-and-pricing/developer/)
2. **Enterprise Edition**: Starting at $20K/year for a maximum analysis of 1 million LOC, up to $240K/year for 100 million LOC. This version provides additional functionalities like Portfolio Management and Executive Reports. [source](https://www.sonarsource.com/plans-and-pricing/enterprise/)
3. **Data Center Edition**: Pricing details to be requested from SonarQube sales. This version is recommended for organizations requiring high availability and performance at scale. [source](https://www.sonarsource.com/plans-and-pricing/data-center/)

## Understanding Lines of Code (LOC)

In SonarQube, LOC refers to the number of physical lines that contain at least one character which is neither a whitespace, nor a tabulation, nor part of a comment. [source](https://community.sonarsource.com/t/how-are-the-exact-lines-of-code-calculated/7271) For SQL projects, LOC is determined by the number of semi-colons (';') in your code. [source](https://www.sonarsource.com/plans-and-pricing/developer/)

## Estimating LOC for a New Project

When estimating the LOC in a new data warehouse project, consider using an older code base to create a prototype or reference model. This will give you an indication of how much code a warehouse of similar complexity might require. Keep in mind that SonarQube's LOC count is based on unique LOC across all projects, not cumulative LOC from multiple scans of the same codebase. [source](https://www.sonarsource.com/plans-and-pricing/developer/)

Using the Community Edition of SonarQube to count the LOC in your old project can provide a good estimate of the potential size of your new data warehouse. This approach will allow you to select the most cost-effective SonarQube subscription plan for your needs.

## Recommendations for SonarQube Subscriptions

It is important to select the subscription plan that not only suits your budget but also meets your project requirements. To decide this, consider the following:

1. **Project Size**: As a general rule, larger projects with higher LOC counts will need higher tier subscriptions. Assess the estimated LOC of your new project, and choose the subscription accordingly.
2. **Required Features**: Each subscription offers additional features. For example, the Enterprise Edition offers Portfolio Management and Executive Reports, which may be useful for project management and executive decision-making. Review the features of each plan and consider if your project will benefit from these.
3. **Scalability**: If your project is expected to grow in size and complexity over time, it might be more cost-effective to opt for a higher tier subscription from the start. This would provide additional features and capacity, saving potential upgrade costs and time in the future.
4. **Trial Periods**: Consider utilizing trial periods if available. This allows you to evaluate the features and performance of the different SonarQube editions without committing to a full subscription.

Ultimately, the choice of subscription should provide the best balance between cost-effectiveness, project needs, and future growth potential.
