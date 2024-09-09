---
title: Identity crosswalks
description: Learn all about identity crosswalks in Real-Time CDP Collaboration, including how bring identity crosswalks in from different sources, and how to manage identity crosswalks. 
audience: admin, publisher, advertiser
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Identity crosswalks

>[!AVAILABILITY]
>
>Adobe Real-Time Customer Data Platform (CDP) Collaboration is currently an alpha product, available to select customers. Contact your Adobe representative to learn more. 

Learn all about identity crosswalks in Real-Time CDP Collaboration, including how to bring identity crosswalks in from different sources, and how to manage identity crosswalks.

Identity crosswalks facilitate the secure and privacy-compliant linking of customer identities across multiple datasets and platforms. By utilizing hashed identifiers, Real-Time CDP Collaboration ensures that users can synchronize and reconcile identities without exposing personal identifiable information (PII). This enables a unified view of the customer for better collaboration and targeted marketing efforts.

In Real-Time CDP Collaboration, use identity crosswalks alongside your audiences by [TODO] insert material here. 

As a first step, you must import identity crosswalks into Real-Time CDP Collaboration. To import identity crosswalks into Real-Time CDP Collaboration, read the section below:

>[!NOTE]
>
>In the alpha release of Real-Time CDP Collaboration, you can import identity crosswalks from your datasets in Real-Time CDP. Further options will be available in subsequent releases.

## Import identity crosswalks into Real-Time CDP Collaboration {#import-crosswalk}

Navigate to **[!UICONTROL Setup]** > **[!UICONTROL Identity crosswalks]** tab, select the Plus **+** symbol, and select **[!UICONTROL Identity crosswalk]**

![Recording of how to get to the screen to add identity crosswalks](/help/assets/setup/identity-crosswalks/import-identity-crosswalk.gif)

### Select Crosswalk Source

Select a source where you will be importing the identity crosswalk from. In the first release of Real-Time CDP Collaboration, Experience Platform is the only supported source for importing crosswalks. 

>[!TIP]
>
>The crosswalks that you are importing from Experience Platform are referred to as *datasets* in Platform.

After selecting Experience Platform as the source of your crosswalks, select the [Experience Platform sandbox](https://experienceleague.adobe.com/en/docs/experience-platform/sandbox/home) from which you are importing the identity crosswalk.

![Recording of how to select a crosswalk source](/help/assets/setup/identity-crosswalks/select-crosswalk-source.gif)

### Select Crosswalk

After selecting Experience Platform as the source of your crosswalks, 

### Provide Details

Provide a name and a description for the identity crosswalk that you are importing into the product. 

### Select Join Key {#select-join-key}

>[!CONTEXTUALHELP]
>id="rtcdp_collaboration_import_crosswalk_join_key"
>title="Join key"
>abstract="A join key is a unique identifier used to match and link records across different datasets. It ensures that data from various sources can be accurately associated with the same individual or entity. Any of the column headers from the selected crosswalk can serve as join key."

A join key is a unique identifier used to match and link records across different datasets. It ensures that data from various sources can be accurately associated with the same individual or entity. By selecting the appropriate join key, you can effectively merge and reconcile data, enhancing the accuracy and completeness of your campaigns.

Any of the column headers from the selected crosswalk can serve as join key.

Select the desired join key for the crosswalk table and select **[!UICONTROL Next]** to proceed to the next step.

### Review

Review any of the selections in the previous screens. When satisfied with your selection, select **[!UICONTROL Next]** to complete the workflow. 

## Next steps

After learning how to import identity crosswalks into Real-Time CDP, you can view all the identity crosswalks that you have so far added to Real-Time CDP Collaboration. You can also now use the identity crosswalks that you have imported when importing audiences into Real-Time CDP Collaboration. 
