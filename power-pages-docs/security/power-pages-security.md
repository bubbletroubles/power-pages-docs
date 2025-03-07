---
title: Power Pages security
description: Learn how to secure the websites you create with Microsoft Power Pages.
ms.date: 11/08/2023
ms.topic: overview
author: nickdoelman
ms.author: kkendrick
ms.reviewer: kkendrick
contributors:
    - nickdoelman
    - ProfessorKendrick
ms.custom: bap-template
---

# Power Pages security

An important consideration when you build public-facing websites is how to make sure that only the correct stakeholders can access critical business data. To make sure your business information is properly protected, Power Pages has a robust security model that encompasses the following key components:

- [Site visibility](#site-visibility)
- [Authenticated users](#authenticated-users)
- [Web roles](#web-roles)
- [Table permissions](#table-permissions)
- [Page permissions](#page-permissions)
- [HTTPS Headers](#https-headers)

## Site visibility

The site visibility setting controls who can access the sites you create in Power Pages. By default, all Power Pages sites are available to users who are internal to your organization. The extra layer of security that Microsoft Entra authentication provides helps to prevent accidental leaks of partially developed website data and designs.

When your website is ready to go live, change the site visibility to public. The public setting makes the site accessible to everyone over the Internet anonymously or to users authenticated through identity providers. 

More information: [Site visibility in Power Pages](site-visibility.md)

## Authenticated users

Microsoft Dataverse contact records represent Power Pages users. Users can get access to your site through authentication. You can integrate Power Pages with authentication providers like Azure AD B2C, Microsoft, and LinkedIn. Authenticated users can be assigned web roles that provide specific access to information on the site. 

More information: [Overview of authentication in Power Pages](authentication/index.md)

## Web roles

Web roles allow users to perform special actions or access protected content and data on the site. Web roles link to users, table permissions, and page permissions. Because users can be assigned multiple web roles, they can get cumulative access to site resources.

All authenticated users, or contacts, are automatically assigned to the Authenticated Users web role. Anonymous, or unauthenticated, users can visit a site and get access to assets through the Anonymous Users web role. 

More information: [Create and assign web roles](create-web-roles.md)

## Table permissions

Access to Dataverse information through [lists](../getting-started/add-list.md), [forms](../getting-started/add-form.md), [Liquid](../configure/liquid-overview.md), and the [Web API](../configure/web-api-overview.md) is protected by table permissions. You can configure table permissions to allow different levels of access and privileges to Dataverse records. Table permissions are associated with web roles to provide appropriate access to users. 

More information: [Configure table permissions](table-permissions.md)

## Page permissions

Page permissions that are associated with web roles to allow access can protect content and components on individual pages. 

More information: [Set page permissions](page-security.md)

## HTTPS Headers

The cross-origin resource sharing (CORS) protocol consists of a set of headers that indicates whether a response can be shared with another domain. You can configure CORS support in Power Pages using the Portal Management app by adding and configuring the site settings. 

More information: [HTTP headers](site-checker-security.md#http-headers)

## More website security

You can integrate Power Pages sites with any web application firewall infrastructure, such as Azure Front Door, to provide extra protection against common web application attacks. 

More information: [Set up Azure Front Door with Power Pages sites](/power-apps/maker/portals/azure-front-door)

## Deep dive: architecture and security

The following white papers allow you to explore Power Pages architecture and security at a deeper level.

| White paper | Description | Date |
| - | - | - |
| [Power Pages Architecture white paper](/power-pages/guidance/white-papers/architecture) | This white paper provides a comprehensive view of the capabilities of the Power Pages platform. It describes the architectural elements that enable Power Pages to scale, offer high reliability and availability, and protect business data to offer enterprise-grade compliance and security. | October 2022 |
| [Power Pages Security white paper](/power-pages/guidance/white-papers/security) | This white paper describes how Power Pages offers enterprise-grade security and the tools and capabilities it offers for administrators and makers to harden security for their external applications. | October 2022 |

### See also

[Power Platform security](/power-platform/admin/security/)  
[Azure security](/azure/security/)
