---
title: Azure Active Directory SSO integration with TASC (beta)
description: Learn how to configure single sign-on between Azure Active Directory and TASC (beta).
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: how-to
ms.date: 05/26/2023
ms.author: jeedes

---

# Azure Active Directory SSO integration with TASC (beta)

In this article, you'll learn how to integrate TASC (beta) with Azure Active Directory (Azure AD). TASC (beta) is a psychological testing platform for selection and career development, enabling HR professionals to make better talent decisions in beta environment. When you integrate TASC (beta) with Azure AD, you can:

* Control in Azure AD who has access to TASC (beta).
* Enable your users to be automatically signed-in to TASC (beta) with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

You'll configure and test Azure AD single sign-on for TASC (beta) in a test environment. TASC (beta) supports both **SP** and **IDP** initiated single sign-on and **Just In Time** user provisioning.

## Prerequisites

To integrate Azure Active Directory with TASC (beta), you need:

* An Azure AD user account. If you don't already have one, you can [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* One of the following roles: Global Administrator, Cloud Application Administrator, Application Administrator, or owner of the service principal.
* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* TASC (beta) single sign-on (SSO) enabled subscription.

## Add application and assign a test user

Before you begin the process of configuring single sign-on, you need to add the TASC (beta) application from the Azure AD gallery. You need a test user account to assign to the application and test the single sign-on configuration.

### Add TASC (beta) from the Azure AD gallery

Add TASC (beta) from the Azure AD application gallery to configure single sign-on with TASC (beta). For more information on how to add application from the gallery, see the [Quickstart: Add application from the gallery](../manage-apps/add-application-portal.md).

### Create and assign Azure AD test user

Follow the guidelines in the [create and assign a user account](../manage-apps/add-application-portal-assign-users.md) article to create a test user account in the Azure portal called B.Simon.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, and assign roles. The wizard also provides a link to the single sign-on configuration pane in the Azure portal. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides). 

## Configure Azure AD SSO

Complete the following steps to enable Azure AD single sign-on in the Azure portal.

1. In the Azure portal, on the **TASC (beta)** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** textbox, type a URL using the following pattern:
    `https://login.beta.tascnet.be/saml/<CustomerName>`

    b. In the **Reply URL** textbox, type a URL using the following pattern:
    `https://login.beta.tascnet.be/saml/<CustomerName>/acs`

1. If you wish to configure the application in **SP** initiated mode, then perform the following step:

    In the **Sign on URL** textbox, type a URL using the following pattern:
    `https://login.beta.tascnet.be/saml/<CustomerName>`

    > [!NOTE]
    > These values are not real. Update these values with the actual Identifier, Reply URL and Sign on URL. Contact [TASC (beta) support team](mailto:support@cebir.be) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

1. TASC (beta) application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

    ![Screenshot shows the image of attributes configuration.](common/default-attributes.png "Attributes")

1. In addition to above, TASC (beta) application expects few more attributes to be passed back in SAML response, which are shown below. These attributes are also pre populated but you can review them as per your requirements.

    | Name | Source Attribute|
    | ------------ | --------- |
    | groups | user.groups |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section, select copy button to copy **App Federation Metadata Url** and save it on your computer.

	![Screenshot shows the Certificate download link.](common/copy-metadataurl.png "Certificate")

## Configure TASC (beta) SSO

To configure single sign-on on **TASC (beta)** side, you need to send the **App Federation Metadata Url** to [TASC (beta) support team](mailto:support@cebir.be). They set this setting to have the SAML SSO connection set properly on both sides.

### Create TASC (beta) test user

In this section, a user called B.Simon is created in TASC (beta). TASC (beta) supports just-in-time user provisioning, which is enabled by default. There's no action item for you in this section. If a user doesn't already exist in TASC (beta), a new one is commonly created after authentication.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to TASC (beta) Sign-on URL where you can initiate the login flow.  

* Go to TASC (beta) Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the TASC (beta) for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the TASC (beta) tile in the My Apps, if configured in SP mode you would be redirected to the application sign-on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the TASC (beta) for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Additional resources

* [What is single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
* [Plan a single sign-on deployment](../manage-apps/plan-sso-deployment.md).

## Next steps

Once you configure TASC (beta) you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).