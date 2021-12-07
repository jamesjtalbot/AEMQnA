## Question 1: **Does the BPA tool report on the code which is not clustering? Or is that an advanced use case?**

- Answer 1: The BPA tool does not specifically analyze code that is not written for clustering.

## Question 2: **Where should we run resource intensive code? Is there an option to design a custom solution?**

- Answer 2: Offload it to the Adobe I/O runtime. Within the product it’s now an asynchronous job. Use the async jobs framework.

## Question 3: **Is there a way to format reports in the BPA?**

- Answer 3: BPA is meant to be used to generate the report in a CSV format, which can then be uploaded to Cloud Acceleration Manager (CAM). Currently, only CSV formats of the report are accepted in CAM.

## Question 4: **What's the update cadence for the BPA Analyzer tool?**

- Answer 4: The Best Practices Analyzer (BPA) typically has a new version once per month. But this can change. Best way to keep track of the latest version is by reading the monthly Release Notes.

## Question 5: **What is the percentage of confidence in the BPA report and are there blind spots in the tool**

- Answer 5: We add patterns to the BPA consistently to ensure we can detect all possible violations when it comes to compatibility with AEM as a Cloud Service. However, since the BPA does not have access to the source code, there are areas that BPA cannot detect. For example, BPA cannot detect if Dispatcher configurations are compatible with AEM as a Cloud Service. There may be other areas such as this. 

## Question 6: **What are some of the examples to use the BPA tool and CAM (are we uploading the same report)? What’s going to be more helpful in cloud acceleration on Experience Cloud vs when you run it locally?**

- Answer 6: BPA generates the report in a CSV format which is not easy to read. This report can then be uploaded to CAM. CAM provides a visual representation of the CSV file and provides guidance on the best practices to follow as well as guidance on areas to refactor as part of a migration. CAM also helps streamline the migration journey based on Adobe’s recommended migration methodology.

## Question 7: **What is the navigation to CAM and dashboard?**

- Answer 7: If you are an AEM on-premise, AMS, or Cloud Service customer, you can access CAM by following the steps below: 

1. Login to Adobe Experience Cloud 
2. Click on Experience Manager card 
3. Click on Launch on the Cloud Acceleration Manager card to open the landing page 

## Question 8: **Is there a way to filter out the ACS common data in the Repository Modernizer?**

- Answer 8: To filter out ACS commons findings from the BPA results, you can set a filter while running the BPA. 	However, please note that filtering out ACS commons findings doesn’t mean that you can ignore them. Please refer to the [ACS Commons](https://adobe-consulting-services.github.io/acs-aem-commons/). to determine compatibility with AEM as a Cloud Service. 

## Question 9: **Does the modernizer tool update all the references on the content??**

- Answer 9: At this time the tool does not update references unless it is included as part of a node rewrite rule. However, this is a priority roadmap item and is currently being evaluated for upcoming new features. 

## Question 10: **Can the modernizer tool update configurations?**

- Answer 10: The AEM Modernization Tools are intended to update content previously curated by Authors. OSGi configurations are associated with Software deployments, and therefore not processed by the tool. Any changes to these configurations would have required an associated code update, delivered by the development team.

## Quesstion 11 **Can the modernizer tool run on both Author and Publish?**

- Answer 11: The Modernization Tools can be run on either Author or Publish systems. However, the standard use case is to update the Author content only, to allow for stakeholder review. Once approved, normal publishing processes can make the updated content available to the consumer. 
