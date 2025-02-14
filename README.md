# Overview

This repository contains a Postman collection designed to execute tests for the API created as part of this project - [Simple Books API](https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md).

The tests cover all endpoints available in the above API and use fundamental methods such as GET, POST, PATCH, and DELETE.

---

# Features

- The collection starts by testing the `status` endpoint to ensure the API is operational before proceeding with further endpoint tests.
- If the `status` endpoint returns a `200` status code in the response, the collection variable `status` is set to `up`; otherwise, it is set to `down`.
- Each subsequent endpoint is preceded by a pre-request script that retrieves the value of the `status` collection variable. If `status` is `down`, the next request is automatically skipped.
- The base part of the tested API URL is stored as a collection variable to avoid code duplication.
- Thanks to Postman's `set` and `get` collection variable functionality, critical and dynamic values such as `access token` and `order id` are shared and accessible between requests that require them.
- The `submit order` endpoint uses the `book id` value to process an order. To prevent issues where the selected `book id` refers to a book with `available: false`, making it impossible to proceed with further tests on `update order` and `delete order`, a pre-request script ensures that a `book id` is selected from an available book.
- Endpoints that return complex objects in the response are validated using `JSON schema`. Additionally, tests cover aspects such as returned data types, array lengths, specific values of object fields, response time, and status codes.

---

# How It Works

Click the button below to directly fork the collection into your Postman workspace:

[<img src="https://run.pstmn.io/button.svg" alt="Run In Postman" style="width: 128px; height: 32px;">](https://app.getpostman.com/run-collection/41712630-f3d86ee5-43bd-46d5-93aa-79aaf6eec8a6?action=collection%2Ffork&source=rip_markdown&collection-url=entityId%3D41712630-f3d86ee5-43bd-46d5-93aa-79aaf6eec8a6%26entityType%3Dcollection%26workspaceId%3Dd9cdcdc2-d5c7-4cc7-a540-c63787101561)

---

# Contact

For questions or feedback, please contact [mjaroszewski1979.](https://github.com/mjaroszewski1979)


![caption](https://github.com/mjaroszewski1979/postman_book_store/blob/main/postman_image.jpg)

