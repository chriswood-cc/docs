## Delete tenants

This process deletes only one tenant. If you have other tenants that need to be removed, you will need to repeat these steps for each tenant. If you are an [enterprise customer](#for-enterprise-customers) or have a [paid subscription](#for-paid-subscription-customers), please review our caveats before proceeding.

::: warning
You **cannot** restore a deleted tenant and you cannot reuse a tenant name when creating new tenants.
:::

1. Log in to the [Dashboard](${manage_url}).
2. Click on your username in the top right corner to display the dropdown box.
3. Select **Settings** to open the **Tenant Settings** page.
4. On the **Tenant Settings** page, select the **Advanced** tab.
5. Scroll down to the **Danger Zone** at the bottom of the page, and click **Delete**.

### For enterprise customers

If you are an Enterprise customer, you may have multiple child tenants as part of your Auth0 contract. Rest assured that if you choose to delete such a tenant, this will have no impact on your agreement with Auth0. We recommend speaking with your Technical Account Manager if you have any concerns about your Enterprise agreement.

### For paid subscription customers

If you have a paid subscription with one or more child tenants, deleting the child tenant should have no impact on your subscription plan. This is because activity and usage on child tenants counts toward the master's tenant activity and usage limitations.