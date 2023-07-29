# Readings: Navigation Properties and Routing
## Notes on Navigation Properties and Routing:

### Why this topic matters in this module:
Navigation properties and routing are crucial concepts in web development, especially in the context of MVC and Core frameworks. Understanding routing enables developers to create clean, user-friendly URLs and efficiently handle incoming requests. It plays a significant role in building accessible and search engine-friendly websites. On the other hand, navigation properties are vital for navigating between related entities in databases, contributing to efficient data retrieval and relationships in an application.

### Routing within MVC:
Routing in MVC refers to the process of matching incoming URLs to specific actions within controllers. It allows developers to define custom URL patterns and map them to controller methods. Routing is essential for creating user-friendly and SEO-friendly URLs, making websites more accessible and improving search engine rankings. Key points about routing within MVC include:
- Routes are defined in the RouteConfig file for traditional ASP.NET MVC or in the Startup.cs file for ASP.NET Core MVC applications.
- Routes consist of a URL pattern and a corresponding controller action.
- Route parameters can be used to pass data from the URL to the controller action.
- Default routes are often set up to handle the homepage and fallback scenarios.

### Routing within Core:
ASP.NET Core follows a similar routing concept as traditional ASP.NET MVC, but with some differences. ASP.NET Core provides a more flexible and powerful routing system that integrates well with middleware and supports attribute-based routing. Key points about routing within Core include:
- Routing in ASP.NET Core is defined in the Startup.cs file using the `UseEndpoints` method.
- Attribute routing allows developers to define routes directly on the controller actions using attributes like `[Route]`.
- The `MapControllerRoute` method is used to define conventional routes.
- ASP.NET Core supports constraint-based routing to restrict the type of data that can be passed in the URL parameters.
- Routing can be combined with middleware for additional functionality in the request handling pipeline.

## Things I want to know more about:
- How can I handle routing for complex scenarios where URLs need to match specific patterns with multiple parameters?
- What are the best practices for designing navigation properties and handling related entities in databases with large datasets?

