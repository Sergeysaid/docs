---
title: Setting up Visual Studio subscriptions with GitHub Enterprise
intro: 'Your team''s subscription to {% data variables.product.prodname_vs %} can also provide access to {% data variables.product.prodname_enterprise %}.'
versions:
  ghec: '*'
type: how_to
topics:
  - Enterprise
  - Licensing
shortTitle: Configurar
---

## About setup of {% data variables.product.prodname_vss_ghe %}

{% data reusables.enterprise-accounts.vss-ghe-description %} Para obter mais informações, consulte "[Sobre o {% data variables.product.prodname_vss_ghe %}de](/billing/managing-licenses-for-visual-studio-subscriptions-with-github-enterprise/about-visual-studio-subscriptions-with-github-enterprise)."

This guide shows you how your team can get {% data variables.product.prodname_vs %} subscribers licensed and started with {% data variables.product.prodname_enterprise %}.

## Roles for {% data variables.product.prodname_vss_ghe %}

Before setting up {% data variables.product.prodname_vss_ghe %}, it's important to understand the roles for this combined offering.

| Role                         | Serviço                                               | Descrição                                                                                                                                   | Mais informações                                                                                                                                  |
|:---------------------------- |:----------------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------- |:------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Subscriptions admin**      | {% data variables.product.prodname_vs %} subscription | Person who assigns licenses for {% data variables.product.prodname_vs %} subscription                                                       | [Overview of admin responsibilities](https://docs.microsoft.com/en-us/visualstudio/subscriptions/admin-responsibilities) in Microsoft Docs        |
| **Subscriber**               | {% data variables.product.prodname_vs %} subscription | Person who uses a license for {% data variables.product.prodname_vs %} subscription                                                         | [Visual Studio Subscriptions documentation](https://docs.microsoft.com/en-us/visualstudio/subscriptions/) in Microsoft Docs                       |
| **Proprietário corporativo** | {% data variables.product.prodname_dotcom %}          | Person who has a user account that's an administrator of an enterprise on {% data variables.product.product_location %}                     | "[Funções em uma empresa](/admin/user-management/managing-users-in-your-enterprise/roles-in-an-enterprise#enterprise-owner)"                      |
| **Organization owner**       | {% data variables.product.prodname_dotcom %}          | Person who has a user account that's an owner of an organization in your team's enterprise on {% data variables.product.product_location %} | "[Roles in an organization](/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization#organization-owners)" |
| **Integrante da empresa**    | {% data variables.product.prodname_dotcom %}          | Person who has a user account that's a member of an enterprise on {% data variables.product.product_location %}                             | "[Funções em uma empresa](/admin/user-management/managing-users-in-your-enterprise/roles-in-an-enterprise#enterprise-members)"                    |

## Pré-requisitos

- Your team's {% data variables.product.prodname_vs %} subscription must include {% data variables.product.prodname_enterprise %}. For more information, see [{% data variables.product.prodname_vs %} Subscriptions and Benefits](https://visualstudio.microsoft.com/subscriptions/) on the {% data variables.product.prodname_vs %} website and [Overview of admin responsibilities](https://docs.microsoft.com/en-us/visualstudio/subscriptions/admin-responsibilities) in Microsoft Docs.

 - Your team must have an enterprise on {% data variables.product.product_location %}. If you're not sure whether your team has an enterprise, contact your {% data variables.product.prodname_dotcom %} administrator. If you're not sure who on your team is responsible for {% data variables.product.prodname_dotcom %}, contact {% data variables.contact.contact_enterprise_sales %}. Para obter mais informações, consulte "[Sobre contas corporativas](/admin/overview/about-enterprise-accounts)".

## Configurar o {% data variables.product.prodname_vss_ghe %}

To set up {% data variables.product.prodname_vss_ghe %}, members of your team must complete the following tasks.

One person may be able to complete the tasks because the person has all of the roles, but you may need to coordinate the tasks with multiple people. For more information, see "[Roles for {% data variables.product.prodname_vss_ghe %}](#roles-for-visual-studio-subscriptions-with-github-enterprise)."

1. An [enterprise owner](#roles-for-visual-studio-subscriptions-with-github-enterprise) must create at least one organization in your enterprise on {% data variables.product.product_location %}. Para obter mais informações, consulte "[Adicionando organizações à sua empresa](/admin/user-management/managing-organizations-in-your-enterprise/adding-organizations-to-your-enterprise)".

1. The [subscription admin](#roles-for-visual-studio-subscriptions-with-github-enterprise) must assign a license for {% data variables.product.prodname_vs %} to a [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) in {% data variables.product.prodname_vss_admin_portal_with_url %}. For more information, see [Overview of the {% data variables.product.prodname_vs %} Subscriptions Administrator Portal](https://docs.microsoft.com/en-us/visualstudio/subscriptions/using-admin-portal) and [Assign {% data variables.product.prodname_vs %} Licenses in the {% data variables.product.prodname_vs %} Subscriptions Administration Portal](https://docs.microsoft.com/en-us/visualstudio/subscriptions/assign-license) in Microsoft Docs.

1. Optionally, if the [subscription admin](#roles-for-visual-studio-subscriptions-with-github-enterprise) assigned licenses to [subscribers](#roles-for-visual-studio-subscriptions-with-github-enterprise) in {% data variables.product.prodname_vs %} before adding {% data variables.product.prodname_enterprise %} to the subscription, the [subscription admin](#roles-for-visual-studio-subscriptions-with-github-enterprise) can move the [subscribers](#roles-for-visual-studio-subscriptions-with-github-enterprise) to the combined offering in the {% data variables.product.prodname_vs %} administration portal. For more information, see [Manage {% data variables.product.prodname_vs %} subscriptions with {% data variables.product.prodname_enterprise %}](https://docs.microsoft.com/en-us/visualstudio/subscriptions/assign-github#moving-to-visual-studio-with-github-enterprise) in Microsoft Docs.

1. If the [subscription admin](#roles-for-visual-studio-subscriptions-with-github-enterprise) has not disabled email notifications, the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) will receive two confirmation emails. For more information, see [{% data variables.product.prodname_vs %} subscriptions with {% data variables.product.prodname_enterprise %}](https://docs.microsoft.com/en-us/visualstudio/subscriptions/access-github#what-is-the-visual-studio-subscription-with-github-enterprise-setup-process) in Microsoft Docs.

1. An [organization owner](#roles-for-visual-studio-subscriptions-with-github-enterprise) must invite the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) to the organization on {% data variables.product.product_location %} from step 1. The [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) can accept the invitation with an existing user account on {% data variables.product.prodname_dotcom_the_website %} or create a new account. After the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) joins the organization, the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) becomes an [enterprise member](#roles-for-visual-studio-subscriptions-with-github-enterprise). For more information, see "[Inviting users to join your organization](/organizations/managing-membership-in-your-organization/inviting-users-to-join-your-organization)."

   {% tip %}

   **Dicas**:

   - While not required, we recommend that the [organization owner](#roles-for-visual-studio-subscriptions-with-github-enterprise) sends an invitation to the same email address used for the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise)'s User Primary Name (UPN). When the email address on {% data variables.product.product_location %} matches the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise)'s UPN, you can ensure that another [enterprise member](#roles-for-visual-studio-subscriptions-with-github-enterprise) does not claim the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise)'s license.
   - If the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) accepts the invitation to the organization with an existing user account on {% data variables.product.product_location %}, we recommend that the [subscriber](#roles-for-visual-studio-subscriptions-with-github-enterprise) add the email address they use for {% data variables.product.prodname_vs %} to their user account on {% data variables.product.product_location %}. For more information, see "[Adding an email address to your {% data variables.product.prodname_dotcom %} account](/account-and-profile/setting-up-and-managing-your-github-user-account/managing-email-preferences/adding-an-email-address-to-your-github-account)."
   - If the [organization owner](#roles-for-visual-studio-subscriptions-with-github-enterprise) must invite a large number of [subscribers](#roles-for-visual-studio-subscriptions-with-github-enterprise), a script may make the process faster. For more information, see [the sample PowerShell script](https://github.com/github/platform-samples/blob/master/api/powershell/invite_members_to_org.ps1) in the `github/platform-samples` repository.

    {% endtip %}

After {% data variables.product.prodname_vss_ghe %} is set up for [subscribers](#roles-for-visual-studio-subscriptions-with-github-enterprise) on your team, [enterprise owners](#roles-for-visual-studio-subscriptions-with-github-enterprise) can review licensing information on {% data variables.product.product_location %}. Para obter mais informações, consulte "[Exibir a assinatura e o uso de sua conta corporativa](/billing/managing-billing-for-your-github-account/viewing-the-subscription-and-usage-for-your-enterprise-account)".

## Leia mais

- "[Getting started with {% data variables.product.prodname_ghe_cloud %}](/get-started/onboarding/getting-started-with-github-enterprise-cloud)"