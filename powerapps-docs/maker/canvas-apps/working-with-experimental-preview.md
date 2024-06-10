---
title: Understand New, Preview, Experimental, and Retired features in canvas apps
description: Learn about New, Preview, Experimental, and Retired features.
author: gregli-msft

ms.topic: conceptual
ms.custom: canvas
ms.reviewer: mkaur
ms.date: 06/06/2024
ms.subservice: canvas-maker
ms.author: gregli
search.audienceType: 
  - maker
contributors:
  - mduelae
  - gregli-msft
---
# Understand New, Preview, Experimental, and Retired features in canvas apps

With every release, we make changes and add features to make Power Apps Studio the best tool to fit your needs. We move the product forward. 

At the same time, keeping your apps running smoothly is our top priority. Despite our best efforts, any change or improvement may unintentionally introduce a side effect, and your app might not work exactly the way it did before.

To help balance improvement against impact on existing apps, we take features through a progression of stages. This allows you a chance to try out the feature and give us feedback, and for us to slowly roll out the feature starting with a small audience. This article describes this process and how you can control your exposure to features that are under development.

At each stage, the number of people who use the feature increases, helping us to validate that the feature is what you need and that we're not introducing unintended side effects.

**Your feedback is critical to this process.**  Please post your feedback in the [Power Apps Community Forum](https://powerusers.microsoft.com/t5/PowerApps-Community/ct-p/PowerApps1).

How long does a feature remain in each stage? This varies from feature to feature. We look at many factors, including the number of apps that use the feature, the number of issues reported, and how urgently the feature is needed. Features can remain in a stage for weeks to many months.  We may also skip some stages if we don't believe it would be helpful.

## New

**New** features have been recently added to the product. They are generally available and fully supported.  You can use **New** features with confidence.

In general, **New** features are enabled by default when creating a new app. When a **New** feature is first introduced, it may not be enabled in all regions initially, allowing us time to deploy and gather telemetry on usage and any problems. If you run into a problem with a feature, the switch can be used as a workaround to disable it until we can correct the problem.

Eventually, **New** features are no longer "new". If there is no breaking change, the switch will be removed and the feature will be turned on for all apps. If there is a breaking change, the old behavior will be available in **Retired**.

**New** features are fully documented in the [Power Apps documentation](./getting-started.md).

## Preview

Enable **Preview** features if you'd like to test a soon to be released feature before it is enabled for everyone.

**Preview** features are well on their way to being a valued part of the product. But, they are not generally available yet and are not fully supported, instead offered under the [preview terms of service](https://aka.ms/pa-preview-terms). **Preview** features should not be used in production. 

In general, **Preview** features are not enabled by default when creating a new app. You should only enable a **Preview** feature for testing purposes and to provide feedback before the feature becomes generally available. This is the last stop for feedback before the feature is finalized. 

Eventually **Preview** features graduate to **New**.

**Preview** features are usually documented in the [Power Apps documentation](./getting-started.md).  Sometimes the documentation may lag in which case the [Power Apps community forum](https://powerusers.microsoft.com/t5/PowerApps-Community/ct-p/PowerApps1) or [Power Apps blog](https://powerapps.microsoft.com/blog/) may be a good source of information.

## Experimental

Enable **Experimental** features if you're an early adopter, see something useful to you, and would like to help test the feature. 

**Experimental** features are in an early-stage preview that is true to the name "experiment". This feature may significantly change or be completely removed at any time. These features are very far from being generally available, are not fully supported, and are offered under the [preview terms of service](https://aka.ms/pa-preview-terms). **Experimental** features should not be used in production. 

**Experimental** features are never enabled by default when creating a new app. You should only enable an **Experimental** feature for testing purposes and to provide feedback. If you don't know what the feature is referring to or its possible impact, you likely should not turn it on. 

Eventually **Experimental** features either graduate to **Preview** or are removed from the product.

**Experimental** features typically are *not* documented. The short description in the **App settings** pane might be the only information about them. Use the [Power Apps community forum](https://powerusers.microsoft.com/t5/PowerApps-Community/ct-p/PowerApps1) or [Power Apps blog](https://powerapps.microsoft.com/blog/) for more information.

## Retired

Sometimes a feature needs to be retired or deprecated.  Often this occurs when there is a new, better way to accomplish a task.  Unpopular features are also pruned too as all features require some overhead to keep up with product changes around them.

**Retired** features are generally available and fully supported. They are being retired because another feature has superseded their behavior or usage of the feature has been low.

**Retired** features are usually not enabled when creating a new app. They are provided for existing apps that still depend on the old behavior.

**Retired** features will eventually be removed from the product after enough time and notice has been provided to makers.

**Retired** features are fully documented in the [Power Apps documentation](./getting-started.md).

## Defaults

In general, when creating a _new_ app:

- **New switches are On.**  These features are generally available, ready for wide circulation, have been documented, and are fully supported. One day, the option to turn off these features may be removed and they'll become a permanent part of the product. Most often, the old behavior before the feature was introduced moves to **Retired**.
- **Preview switches can be enabled for testing and feedback.**  These features will one day ship, are almost ready for wide circulation, have been documented, but are under the preview terms of service. They are not ready for production yet. Most of these features will move to **New** one day.
- **Experimental switches are Off.**  These features should only be used with caution, they can be changed or removed at any time. These features are under the preview terms of service and are not ready for production. Some of these features will graduate to **Preview** and some will be removed from the product.
- **Retired switches are Off.**  These features are generally available, are fully document, and are fully supported. They one day will be removed from the product, often offering behavior that has been superseded by another feature.  Documentation will explain the alternatives to using these older features.

As _existing_ apps go through their lifecycle, you may want to adjust these switches to take advantage of new features or to remove a dependency on a feature that will be retired.  Turning **New** switches On and **Retired** switches Off brings existing apps into alignment with new apps and the future of the product.

## Controlling which features are enabled

Experimental and preview features are listed in the app's **Settings** > **Updates**.  From within the app, select **Settings**, and then select **Updates**. Select **New**, **Preview**, **Experimental**, or **Retired** features using the available tabs.

![Advanced settings for canvas app.](media/working-with-experimental/advanced-settings.png "Advanced settings for canvas app")

Each feature has a toggle switch.  **Off** means that the feature is disabled.  

In some cases, you might need to close and reopen the app after you change a setting.  The feature description should indicate when you must perform this step.

At the top of the **Advanced settings** panel, you can find settings for fully shipped features that aren't preview or experimental and that you can completely depend on. 

These settings are specific to each app, so changing a toggle switch affects only the app that's currently open. If you create an app, these switches revert to their default settings for that app.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
