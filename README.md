# itommey-test
Test Fullstack
# nodejs-expressjs-reactjs

### Backend task
The **backend** side will manage `product`, with REST over HTTP API request:
1. Create Web Server App using `Express.js` or `Hapi` to handle product data
2. Backend side should use SQL database engine such: `Postgres/SQL Server/MySQL` wrapped with **ORM**
3. For **ORM** library, please use `Sequelize/Knex` for `migration`, `seeding`, and `data processing` (CRUD). Prevent using sql script directly!
4. Create `migration` for product schema with fields: 
    * id: `BIGINT`
    * name: `VARCHAR`
    * qty: `INT`
    * picture: `TEXT` with Base64 value
    * expiredAt: `DATE` YYYY-MM-DD
    * isActive: `BOOLEAN`
5. Don't forget to `seed` it with some initial data.
6. HTTP response and request body payload should formated in **JSON** format
7. Describe your endpoint as a **REST**, this is available endpoints for manage product:
    * Add product: `/POST` `/product`
    * Get products: `/GET` `/product`
    * Get product by id: `/GET` `/product/:id`
    * Remove product by id: `/DELETE` `/product/:id`
    * Update product by id: `/PUT` `/product/:id`
6. With **REST** specification:
    * For getting product should returned with `true` value in `isActive` field
    * Filtering product by specific criteria, sorter and pagination product is optional.
    * While deleting product, we use "soft delete" with set `isActive` field to `false`
    * Post a product always set `isActive` value to `true`
    * Updating product should block `isActive` value from body payloads
7. Endpoint of logging activity, unit testing, and `Swagger` API docs are optional
8. Write clean and effective code for example: proper project structure, exception handling, parameterize config, etc.
9. Push your work to your **GitHub** repository, make sure your repository accessible to public.

### Frontend task
1. Create Web App using `ReactJS` to handle product management
2. State management is MUST! Please using `Redux` or `Mobx` for state management
3. Use this API specification rule:
    * The `id` field cannot be updated once the product created
    * For getting product please using `table` element, `datatable` library is prefered for show the products
    * Filtering product by specific criteria, sorter and pagination product is optional
    * Post a product always send `isActive` value to `true`
    * We prefer deleting product using "soft delete" mechanism, with send `isActive` field to `false` value
4. Update product UI will show big **modal dialog** with `form` element specifications:
    * `id` field should disabled `input` element
    * `name` field is `input` element with type=text
    * `qty` field is  `input` element with type=number
    * `picture` field should rendered as an `img` element with base64 value
    * `expiredAt` field should use `date picker` element
    * `isActive` field should use `checkbox` element
5. Also add delete handler in your app
6. Before call `/PUT` or `/DELETE` APIs, add small **modal dialog** just for user confirmation
7. You can use **MVC/MVVM/MVP** design pattern
8. Make your ui element responsive relative to screen size or device type
9. Write clean and effective code for example: proper project structure, ui element, data binding, exception handling, parameterize config, etc.
10. Push your work to your **GitHub** repository, make sure your repository accessible to public.
