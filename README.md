## **Does the BPA tool report on the code which is not clustering? Or is that an advanced use case?**

- The BPA tool does not specifically analyze code that is not written for clustering.

## **Where should we run resource intensive code? Is there an option to design a custom solution?**

- Offload it to the Adobe I/O runtime. Within the product it’s now an asynchronous job. Use the async jobs framework.

## **Is there a way to format reports in the BPA?**

- BPA is meant to be used to generate the report in a CSV format, which can then be uploaded to Cloud Acceleration Manager (CAM). Currently, only CSV formats of the report are accepted in CAM.

## **What's the update cadence for the BPA Analyzer tool?**

- The Best Practices Analyzer (BPA) typically has a new version once per month. But this can change. Best way to keep track of the latest version is by reading the monthly Release Notes.

## **What is the percentage of confidence in the BPA report and are there blind spots in the tool**

- We add patterns to the BPA consistently to ensure we can detect all possible violations when it comes to compatibility with AEM as a Cloud Service. However, since the BPA does not have access to the source code, there are areas that BPA cannot detect. For example, BPA cannot detect if Dispatcher configurations are compatible with AEM as a Cloud Service. There may be other areas such as this. 

## **What are some of the examples to use the BPA tool and CAM (are we uploading the same report)? What’s going to be more helpful in cloud acceleration on Experience Cloud vs when you run it locally?**

- BPA generates the report in a CSV format which is not easy to read. This report can then be uploaded to CAM. CAM provides a visual representation of the CSV file and provides guidance on the best practices to follow as well as guidance on areas to refactor as part of a migration. CAM also helps streamline the migration journey based on Adobe’s recommended migration methodology.

## **What is the navigation to CAM and dashboard?**

- If you are an AEM on-premise, AMS, or Cloud Service customer, you can access CAM by following the steps below: 

1. Login to Adobe Experience Cloud 
2. Click on Experience Manager card 
3. Click on Launch on the Cloud Acceleration Manager card to open the landing page 

## **Is there a way to filter out the ACS common data in the Repository Modernizer?**

- To filter out ACS commons findings from the BPA results, you can set a filter while running the BPA. 	However, please note that filtering out ACS commons findings doesn’t mean that you can ignore them. Please refer to the [ACS Commons](https://adobe-consulting-services.github.io/acs-aem-commons/). to determine compatibility with AEM as a Cloud Service. 

## **Does the modernizer tool update all the references on the content??**

- At this time the tool does not update references unless it is included as part of a node rewrite rule. However, this is a priority roadmap item and is currently being evaluated for upcoming new features. 

## **Can the modernizer tool update configurations?**

- The AEM Modernization Tools are intended to update content previously curated by Authors. OSGi configurations are associated with Software deployments, and therefore not processed by the tool. Any changes to these configurations would have required an associated code update, delivered by the development team.

## **Can the modernizer tool run on both Author and Publish?**

- The Modernization Tools can be run on either Author or Publish systems. However, the standard use case is to update the Author content only, to allow for stakeholder review. Once approved, normal publishing processes can make the updated content available to the consumer. 
