---
title: Hide from search engines
description: Search engines like Google constantly crawl the internet in search of new data. When your site is being crawled, your store's robots.txt file blocks page content that might otherwise reduce the effectiveness of your SEO strategy by stealing PageRank.
---

The simplest way to hide a page from search engines is to add a meta robots tag in the `<head>` section of your HTML. This tells search engine crawlers not to index ("No index") or follow links ("No follow") on the page.

## Using a custom metafield 

::badge
:icon{name="i-lucide-badge-check"} Recommended
::

::warning
Adding the `seo.hidden` metafield hides the product, collection, page, or blog post from sitemaps, search engines, and your [online store search](https://help.shopify.com/en/manual/online-store/storefront-search){target="_blank"}.
::

::tip
No developer is required to add this metafield.
::

This adds the following meta tag to the `<head>` section of your page:

```html
<meta name="robots" content="noindex,nofollow">
```

::steps{level="4"}

#### From your Shopify admin, go to Settings > Metafields and metaobjects.

::note{to="https://admin.shopify.com/settings/custom_data"}
Go to Metafields and metaobjects in the Shopify admin.
::

#### Under Metafield definitions, select the eligible resource type (Products, Collections, Pages, or Blog posts) that you want to hide.

#### Click or tap Add definition.

#### Set the following fields:

- Give the metafield a **Name** such as :kbd{value="SEO Hidden"}.
- Set **Namespace and key** to `seo.hidden`.
- Optional: Give a brief description, such as :kbd{value="Hides the resource from search engines when value is 1"}.

#### Configure the custom field values by doing the following actions:

- Click or tap :icon{name="i-lucide-circle-plus"} **Select type** and then select **Integer**.
- Select **One value**.
- In the **Validations** section, set the **Maximum value** to be `1`.

#### Click Save.

#### In your Shopify admin, navigate to the product, collection, page, or blog post that you want to hide from search engines.

#### In the Metafields section, set the value of the SEO Hidden metafield to 1.

#### Click Save.

::

::note{to="https://help.shopify.com/en/manual/promoting-marketing/seo/hide-a-page-from-search-engines#custom-metafields"}
Learn more about how to hide a page or product using a custom metafield in the Shopify documentation.
::


## Using metatags

::warning
Do not add this code yourself, but ask your developer to add it to your theme.liquid file. Otherwise it will be overwritten when the developer releases a new version of the theme.
::

You can hide pages that aren't included in your `robots.txt.liquid` file by customizing the `<head>` section of your store's `theme.liquid` layout file. You need to include some metatag code to stop the indexing of particular pages.

::note{to="https://help.shopify.com/en/manual/promoting-marketing/seo/hide-a-page-from-search-engines#metatags"}
Learn more about how to hide a page or product using metatags in the Shopify documentation.
::
