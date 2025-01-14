---
lang: en
title: 'API docs: rest-crud.definecrudrestcontroller'
keywords: LoopBack 4.0, LoopBack 4
sidebar: lb4_sidebar
permalink: /doc/en/lb4/apidocs.rest-crud.definecrudrestcontroller.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/rest-crud](./rest-crud.md) &gt; [defineCrudRestController](./rest-crud.definecrudrestcontroller.md)

## defineCrudRestController() function

Create (define) a CRUD Controller class for the given model.

Example usage:

```ts
const CrudRestController = defineCrudRestController<
  Product,
  typeof Product.prototype.id,
  'id'
>(Product, {basePath: '/products'});

class ProductController extends CrudRestController {
  constructor() {
   super(repo);
  }
}

app.controller(ProductController);

```

<b>Signature:</b>

```typescript
export declare function defineCrudRestController<T extends Entity, IdType, IdName extends keyof T, Relations extends object = {}>(modelCtor: typeof Entity & {
    prototype: T & {
        [key in IdName]: IdType;
    };
}, options: CrudRestControllerOptions): CrudRestControllerCtor<T, IdType, IdName, Relations>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  modelCtor | <code>typeof Entity &amp; {</code><br/><code>    prototype: T &amp; {</code><br/><code>        [key in IdName]: IdType;</code><br/><code>    };</code><br/><code>}</code> |  |
|  options | <code>CrudRestControllerOptions</code> |  |

<b>Returns:</b>

`CrudRestControllerCtor<T, IdType, IdName, Relations>`


