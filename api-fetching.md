# Choosing @furiosa/swag for Type-Safe API Generation

## Context

As our application grows, ensuring type safety in API interactions is crucial for preventing runtime errors and streamlining development workflows. We need a solution that allows us to generate type-safe functions or React hooks based on our API specifications from Swagger. Additionally, we want a reliable API fetcher to handle HTTP requests. After reviewing various options, we aim to select tools that optimally integrate with our stack and enhance our development process.

## Options Considered

### 1. @furiosa/swag

**Pros:**

- Automatically generates type-safe APIs as functions or React hooks from Swagger specifications, significantly reducing the risk of errors in API interactions.
- Promotes consistent API usage across the application and minimizes boilerplate code, making for a more efficient development process.
- Enhances collaboration within the team by providing clear typings, which helps developers understand how to interact with API endpoints effectively.
- Maintains a single source of truth for API specifications, ensuring that frontend implementations stay aligned with the backend.

**Cons:**

- Requires an initial investment in setting up the Swagger specification and integrating the package into the existing codebase.
- Dependency on external specifications may introduce challenges if the Swagger definitions are not kept up to date.

### 2. Other Alternatives (e.g., Manual Type Definitions)

- **Manual Type Definitions**

  - **Pros**: Full control over types and API calls; no additional dependencies.
  - **Cons**: Time-consuming, prone to human error, and difficult to maintain as APIs evolve.

## Decision

We have decided to implement **@furiosa/swag** for generating type-safe APIs in our application, using **Axios** as the API fetcher for handling HTTP requests.

## Rationale

1. **Type Safety**: By generating type-safe APIs, we significantly reduce the chances of runtime errors related to incorrect API interactions, leading to a more robust application.

2. **Efficiency**: The ability to create functional or hook-based API calls directly from our Swagger definitions streamlines our development process and reduces boilerplate code, allowing our team to focus on building features.

3. **Consistent API Handling**: Integrating Axios as the API fetcher allows us to leverage its rich feature set, including interceptors, request/response transformations, and cancellation capabilities, which complement the type-safe API generation from @furiosa/swag.

4. **Consistency**: Using a single tool for API generation maintains consistency in how APIs are consumed across different parts of the application, facilitating better team collaboration and understanding.

5. **Clear Documentation**: The generated types provide clear documentation and API contracts, making it easier for developers to understand how to interact with the backend services effectively.

## Consequences

1. **Initial Setup**: We will need to allocate time for setting up Swagger specifications and integrating @furiosa/swag with Axios, which may require adjustments to our existing development workflow.

2. **Dependency Management**: Incorporating these packages introduces additional dependencies that we must manage and keep updated. It will be essential to monitor changes and maintain compatibility with evolving API specifications.

3. **Documentation Practices**: We will establish guidelines for maintaining and updating Swagger definitions to ensure that the generated APIs remain accurate and reflect the current state of the backend services.

## Conclusion

In conclusion, we have chosen **@furiosa/swag** as our solution for generating type-safe APIs from Swagger specifications, using **Axios** for API fetching. This decision enhances our development workflow by providing clear, maintainable, and type-safe API interactions. By integrating @furiosa/swag and Axios into our stack, we are positioning our application for improved reliability and developer productivity as we scale.
