---
description: Learn how to add login to your application using the SPA login flow.
toc: true
topics:
  - api-authentication
  - oidc
  - hybrid-flow
contentType: tutorial
useCase:
  - add-login
---
# Add Login Using the Single Page Application (SPA) Flow

<%= include('../../../_includes/_pipeline2') %>

::: note
This tutorial will help you add login to your single page appplication (SPA) using the SPA login flow. If you want to learn how the flow works and why you should use it, see [Single Page Login Flow](/flows/concepts/single-page-login-flow).
:::

Auth0 makes it easy to implement the Single Page Application Login Flow by using:

* [Auth0 SPA Quickstarts](/libraries): The easiest way to implement the SPA flow, which will do most of the heavy-lifting for you. Our [SPA Quickstarts](/quickstart/spa) will walk you through the process.
* Authentication API: If you prefer to roll your own solution, keep reading to learn how to call our API directly.

If you prefer to embed your own login pages within your SPA, you can implement our login widget (Lock UI) directly into your app with:

* [Lock v11 for Web](/libraries/lock/v11)

Following successful login, your application will have access to the user's [ID Token](/tokens/id-token) and [Access Token](/tokens/overview-access-tokens), as well as an authorization code that can be exchanged with Auth0 for an additional Access Token. The ID Token will contain basic user profile information, and the Access Token can be used to call the Auth0 /userinfo endpoint or your own protected APIs.

## Prerequisites

This tutorial can be used to add login to your SPA. If you want to learn to call your API from a SPA, see [Call My API Using an SPA](/flows/guides/single-page-login-flow/call-api-using-single-page-app).

**Before beginning this tutorial:**

* [Register your Application with Auth0](applications/spa)
    * Select an **Application Type** of **Single Page Web App**.
    * Add an **Allowed Callback URL** of **https://${account.namespace}/callback**.
    * Make sure your Application's **[Grant Types](/applications/application-grant-types#how-to-edit-the-application-s-grant_types-property)** include **Authorization Code** and **Implicit**.

## Steps

1. [Authorize the user](#authorize-the-user): Request the user's authorization and redirect back to your app.
1. [Parse the response from Auth0].(#parse-the-response-from-auth0): Parse the hash fragments in the URL used by Auth0 to redirect the user to get the Authorization Code, ID Token, and/or Access Token.
1. [Exchange the Authorization Code for an Access Token](#exchange-the-authorization-code-for-an-access-token): Exchange the Authorization Code with Auth0 for an Access Token that allows you to call your protected API.
1. [Refresh Tokens](#refresh-tokes): Use a refresh token to request new Access Tokens if the existing ones are expired.

Optional: [Explore Sample Use Cases](#sample-use-cases)

<%= include('./includes/authorize-user-add-login') %>

<%= include('./includes/parse-the-response-from-auth0') %>

<%= include('./includes/exchange-the-authorization-code-for-an-access-token') %>

<%= include('./includes/refresh-tokens') %>

<%= include('./includes/sample-use-cases-add-login') %>

## Keep Reading

::: next-steps
- [Why you should always use Access Tokens to secure APIs](/api-auth/why-use-access-tokens-to-secure-apis)
- [The OAuth 2.0 protocol](/protocols/oauth2)
- [The OpenID Connect protocol](/protocols/oidc)
- [Tokens used by Auth0](/tokens)
:::