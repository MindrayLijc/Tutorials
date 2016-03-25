---
title: Localizing your SAPUI5 app
description: Learn how to support multiple languages in your app using the SAP Translation Hub, and how to manually add a language-locale combination.
tags: [tutorial:product/hcp, tutorial:product/sapui5_web_ide, tutorial:product/mobile, tutorial:product/sap_ui5]
---

## Prerequisites
 - **Proficiency:** Intermediate
 - **Tutorials:** [Commit your project files to your HCP Git repository](http://go.sap.com/developer/tutorials/hcp-webide-commit-git.html)

## Next Steps
 - An Open Data Protocol (OData) primer (coming soon)

## Details

### You will learn

In the fourth tutorial of Mobile Guide #2, you extracted strings from the application into the internationalization (i18n) bundle of UI5. In subsequent tutorials, you continued this practice by placing all strings in the messageBundle.properties file.

When loading an app, SAPUI5 will check the container’s (in this case your browser’s) language/local settings, then attempt to load the most specific locale resource bundle file, with graceful degradation down to a “catchall” case. For example, with a Swiss German-based browser, and no explicit language-related URL parameters, the SAPUI5 runtime will attempt to load the following files in this order:
### Time to Complete
**20 min**

---

1. Log into your [HCP account](https://account.hanatrial.ondemand.com), click on the **Account** tab and confirm that the Enable beta features check box is selected. If not, click the **Edit** button, check the box, and click Save.

    >This step is required because the SAP Translation Hub service is currently in beta release.


    ![Open Translation Hub page](mob3-3_3b.png)
    :---------------| :-------------
    Application Name            |  `northwind` (See note below)
    Branch                      |  `Master`
    Path to Properties File     |  `i18n/messageBundle.properties`
    Target Languages            | Click on the menu and check: `Dutch, French, German, Spanish`
    Domain                      | `Basis`


    ![git password](mob3-3_5b.png)


    ![Git pane](mob3-3_10a.png)

   Login in with your HCP credentials when prompted. You will see a progress indicator on the Pull button as the new `messageBundle_xx.properties` files are added to your project folder.

    ![Git pane](mob3-3_10b.png)


   The green dot next to the files indicates that the version in your project is identical to the version in your Git repository.
    label_CurrentInventoryValue=Aktuelle Lagerbestand

15. Deploy your app to HCP (following the same procedure as in an earlier [tutorial](http://go.sap.com/developer/tutorials/hcp-deploy-mobile-web-app.html) and open the new, active version of the app.

    - If your standard application URL looks like this:
        - `https://northwind-p12345678trial.dispatcher.hanatrial.ondemand.com/`
    - You can view the German strings by specifying:
        - `https://northwind-p12345678trial.dispatcher.hanatrial.ondemand.com/?sap-ui-language=de`
    - Swiss German strings by specifying:
        - `https://northwind-p12345678trial.dispatcher.hanatrial.ondemand.com/?sap-ui-language=de_CH`
    - Spanish strings by specifying:
        - `https://northwind-p12345678trial.dispatcher.hanatrial.ondemand.com/?sap-ui-language=es`


17. As described in the introduction for this tutorial, when a user opens your app URL, the app will check the language and locale settings on the device, then load the appropriate strings file.


## Next Steps
 - An Open Data Protocol (OData) primer (coming soon)