---
title: Filter, sort, and search galleries with Copilot (preview)
description: Learn how to use Copilot to quickly sort, filter, and search canvas app galleries using natural language.
ms.date: 06/03/2024
ms.topic: article
ms.component: pa-user
ms.subservice: end-user
author: jordanchodak
ms.author: jordanchodak
ms.reviewer: sericks
search.audienceType: 
  - enduser
contributors:
- lancedMicrosoft
---


# Filter, sort, and search galleries with Copilot (preview)

[This article is prerelease documentation and is subject to change.]

You can use Copilot to quickly sort, filter, and search the items in canvas app galleries. Copilot uses a natural language expression to generate a query to the database that scopes the current view of records in a gallery or grid. This helps users to quickly find the records they need. 

Copilot for galleries and grids supports three key kinds of commands: 

- Search for a specific set of records using a _starts with_ text example. 
- Filter the list of records to a specific set with complex criteria. This list includes _and_ and _or_ statements and relational operators such as, _equal_, _greater than_, and more). 
- Sort the list of records, such as in ascending or descending order.

Copilot for galleries and grids don't support aggregate queries, for example, _top_, _min_, _max_, _sum_, and _average_, as these answers can't be shown as a list of records. 

Copilot for galleries and grids provides five key benefits:

- Copilot enables natural language commands. Users can express commands (search, filter, and sort) in natural language. The prompt user interface (UI) helps users formulate sentences by showing different examples of natural language sentences that work. 
- Copilot enables queries over the full query result. Users can search, filter, and sort on fields even if the application doesn't provide UI controls for these tasks. For example, you can search for records even if the application doesn't have a search bar.  
- Copilot saves development time. Authors save time developing apps because they don't need to develop all the UI controls necessary for the app. Instead, they can rely on Copilot for this functionality. 
- Copilot is query safe. It only generates queries that can be run on the server. Authors don't need to worry about whether or not their queries can be delegated. 
- Copilot keeps private data private. It only works with the data that is normally returned to the application. It doesn't access fields that aren't returned to the app in a gallery/grid or form.


> [!IMPORTANT]
> - This feature is not yet available and is expected to begin rollout as on-by-default in late June.  However, if you turn the feature off before the release, the feature should be turned off when it rolls out to you.
> - To use this feature, your environment must be in a region with GPU (graphics processing unit) capacity, or your tenant must have the **Move data across regions** checkbox selected.  Learn more: [Turn on copilots and generative AI features](/power-platform/admin/geographical-availability-copilot)
> - To use this feature, the browser language must be US English.
> - This capability is powered by [Azure OpenAI Service](/azure/cognitive-services/openai/overview).
> - This capability may be subject to usage limits or capacity throttling.
> - Copilot isn't supported and won't work for environments that have customer-managed key (CMK) or have lockbox.
> - Preview features aren’t meant for production use and may have restricted functionality. These features are available before an official release so that customers can get early access and provide feedback.
> - This feature is designed for galleries that use SharePoint as their sole data source. More data sources will be added to have this capability in the future. SharePoint effectively only supports Search, Filter, and Sort. When this feature is extended to other data sources, this feature will still only support Search, Filter, and Sort.
> - For more information about the preview, go to our [preview terms](https://go.microsoft.com/fwlink/?linkid=2189520).

## Use this feature

1. Select an item in the gallery. 
2. The option to **Sort, filter, and search with Copilot** should appear. Select that option. 
3. Write your desired sort, filter, or search query into the text box or select one of the suggested queries.  
     > [!Note] 
     > You must enter the text in English. This feature only supports the English language at this time. 
4. Select the **Send** icon. 
5. Copilot updates the gallery for you. Review the filters applied. The following options are available: 
    - If you want to remove any filters you have applied, select the **x** on the tag displaying the filter you want to remove. 
    - To clear all applied filters, select the trash icon button. 
    - If you're satisfied with the filters that are applied to the gallery, select **Keep it**.  You can always go back and remove or add more filters. 
  
## Turn off gallery filtering in web player

You can turn off gallery filtering for an app or an environment using a PowerShell cmdlet.  

> [!NOTE]
> - When using PowerShell cmdlets, you must use the latest Power Apps admin PowerShell module version. More information: [Get started using the Power Apps admin module](/powershell/powerapps/get-started-powerapps-admin)
> - If an admin has turned off this feature at the environment-level, this feature isn't available for any apps in that environment.
> - The PowerShell cmdlets may take up to two hours to take effect.
> - This feature is not yet available and is expected to begin rollout as on-by-default in early June.  However, if you turn the feature off before the release, the feature should be turned off when it rolls out to you.

### Turn off gallery filtering for an app

You can use a PowerShell cmdlet to turn off this setting for an app.

To turn off for an app using PowerShell:

```powershell
Set-PowerAppSettings -AppName 'AppName' -CanvasGalleryFilteringCopilotEnabled $false
```

### Turn off gallery filtering for an environment

To turn off gallery filtering for a specific environment, use the following cmdlet.

```powershell
Set-AdminPowerAppEnvironmentCopilotSettings -EnvironmentName 'EnvironmentName' -CanvasAppGalleryFilterCopilotEnabled $false
```
   
## Known issue

- This feature can't be turned off on a per-tenant basis.  It can only be turned off by following the information in [Turn off gallery filtering in web player](#turn-off-gallery-filtering-in-web-player).
