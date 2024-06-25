---
title: Calculating overlap counts and percentages
description: Understand how overlap counts and percentages are calculated in various areas of Adobe Real-Time CDP Collaboration
audience: admin, publisher, advertiser
badgealpha: label="Alpha" type="Informative" url="https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2b-edition-prime-and-ultimate-packages.html newtab=true"
---

# Calculating overlap counts and percentages

In Adobe Real-Time CDP Collaboration, understanding audience overlap is crucial for optimizing your marketing strategies and ensuring effective collaboration between advertisers and publishers. This document explains how overlap counts and percentages in various product areas are calculated using sample data.

## Sample Data - Identity Count

### Assumptions for Calculation Purposes

For this example, let's assume:
* The advertiser has three audiences (A1, A2, A3).
* The publisher has three audiences (P1, P2, P3).
* All match key identities are mutually exclusive across all audiences.

>[!NOTE]
>
>In reality, there would be some overlap between each audience's match key identities, but for simplicity, this example assumes they are exclusive in this case.

### Advertiser Audiences

| Advertiser Audiences | A1   | A2   | A3   | ALL  |
|----------------------|------|------|------|------|
| HEM identities       | 300K | 450K | 250K | 1M   |
| Liveramp Id identities | 500K | 200K | 700K | 1.4M |
| Total identity count | 800K | 650K | 950K | 2.4M |

### Publisher Audiences

| Publisher Audiences | P1   | P2   | P3   | ALL  |
|---------------------|------|------|------|------|
| HEM identities      | 150K | 600K | 550K | 1.3M |
| Liveramp Id identities | 400K | 350K | 100K | 850K |
| Total identity count | 550K | 950K | 800K | 2.3M |

## Calculating Overlap Counts and Percentages

### Sample Data - Overlap Count

#### Advertiser Each vs Publisher Each

|                     | A1 - P1 | A2 - P2 | A3 - P3 |
|---------------------|---------|---------|---------|
| Overlap by HEM      | 100K    | 300K    | 150K    |
| Overlap by Liveramp Id | 200K    | 150K    | 50K     |
| Total overlap       | 300K    | 450K    | 200K    |

#### Advertiser Each vs Publisher ALL

|                     | A1 - P ALL | A2 - P ALL | A3 - P ALL |
|---------------------|------------|------------|------------|
| Overlap by HEM      | 250K       | 400K       | 200K       |
| Overlap by Liveramp Id | 350K       | 150K       | 230K       |
| Total overlap       | 600K       | 550K       | 430K       |

#### Advertiser ALL vs Publisher Each

|                     | A ALL - P1 | A ALL - P2 | A ALL - P3 |
|---------------------|------------|------------|------------|
| Overlap by HEM      | 120K       | 530K       | 200K       |
| Overlap by Liveramp Id | 350K       | 330K       | 50K        |
| Total overlap       | 470K       | 860K       | 250K       |

#### Advertiser ALL vs Publisher ALL

|                     | A ALL - P ALL |
|---------------------|---------------|
| Overlap by HEM      | 850K          |
| Overlap by Liveramp Id | 730K          |
| Total overlap       | 1.58M         |

## Discover Module

The Discover module in Adobe Real-Time CDP Collaboration provides valuable insights into your audience data. By understanding audience overlaps, you can identify potential collaboration opportunities and optimize your marketing strategies. The Audience Insights section within the Discover module helps you analyze the overlap counts and percentages between different audience segments.

### All advertiser audiences & all publisher audiences

| Advertiser Audiences | Publisher Audiences | Identity Count (A) | Overlapping Identities (B) | Overlap Percent | Match Key Breakdown | Match Key Breakdown % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| ALL                  | ALL                 | Total identity count of ALL advertiser audiences <br> Identity count = 1M + 1.4M = 2.4M | Total overlap between ALL advertiser audiences and ALL publisher audiences for all match keys <br> Overlapping identities = 1.58M | Percent of Overlapping identities over total identity count of ALL advertiser audiences <br> Overlap % = (B / A) * 100 = (1.58M / 2.4M) * 100 = 65.83% <br> Overlap percent = 65.83% | Overlapping identities per match key <br> Overlap by HEM = 850K <br> Overlap by Liveramp Id = 730K | Percentage of match key overlap over total overlapping identities <br> Match key % for HEM = (850K / 1.58M) * 100 = 53.8% <br> for Liveramp Id = (730K / 1.58M) * 100 = 46.2% |

### All advertiser audiences & one publisher audience

| Advertiser Audiences | Publisher Audiences | Identity Count (A) | Overlapping Identities (B) | Overlap Percent | Match Key Breakdown | Match Key Breakdown % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| ALL                  | 1 P2                | Total identity count of all advertiser audiences <br> Identity count = 1M + 1.4M = 2.4M | Total overlap between ALL advertiser audiences and selected publisher audience P2 for all match keys <br> Overlapping identities = 860K | Percent of Overlapping identities over total identity count of ALL advertiser audiences <br> Overlap % = (B / A) * 100 = (860K / 2.4M) * 100 = 35.83% <br> Overlap percent = 35.83% | Overlapping identities per match key <br> Overlap by HEM = 530K <br> Overlap by Liveramp Id = 330K | Percentage of match key overlap over total overlapping identities <br> Match key % for HEM = (530K / 860K) * 100 = 61.62% <br> for Liveramp Id = (330K / 860K) * 100 = 38.38% |

### One advertiser audience & all publisher audiences

| Advertiser Audiences | Publisher Audiences | Identity Count (A) | Overlapping Identities (B) | Overlap Percent | Match Key Breakdown | Match Key Breakdown % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A1                 | ALL                 | Total identity count of advertiser selected audience A1 <br> Identity count = 300K + 500K = 800K | Total overlap between advertiser audience A1 and ALL publisher audiences for all match keys <br> Overlapping identities = 600K | Percent of Overlapping identities over identity count of advertiser selected audience (A1) <br> Overlap % = (B / A) * 100 = (600K / 800K) * 100 = 75% <br> Overlap percent = 75% | Overlapping identities per match key <br> Overlap by HEM = 250K <br> Overlap by Liveramp Id = 350K | Percentage of match key overlap over total overlapping identities <br> Match key % for HEM = (250K / 600K) * 100 = 41.67% <br> for Liveramp Id = (350K / 600K) * 100 = 58.33% |

### One advertiser audience & one publisher audience

| Advertiser Audiences | Publisher Audiences | Identity Count (A) | Overlapping Identities (B) | Overlap Percent | Match Key Breakdown | Match Key Breakdown % |
|----------------------|---------------------|--------------------|----------------------------|-----------------|---------------------|-----------------------|
| 1 A2                 | 1 P2                | Total identity count of advertiser selected audience A2 <br> Identity count = 450K + 200K = 650K | Total overlap between selected advertiser audience A2 and selected publisher audience P2 for all match keys <br> Overlapping identities = 450K | Percent of Overlapping identities over identity count of my selected audience (A2) <br> Overlap % = (B / A) * 100 = (450K / 650K) * 100 = 69.23% <br> Overlap percent = 69.23% | Overlapping identities per match key <br> Overlap by HEM = 300K <br> Overlap by Liveramp Id = 150K | Percentage of match key overlap over total overlapping identities <br> Match key % for HEM = (300K / 450K) * 100 = 66.67% <br> for Liveramp Id = (150K / 450K) * 100 = 33.33% |
