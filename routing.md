# Routing Library for Web Application

## Context

Our team is developing a new web application that requires a robust and flexible routing solution. We are evaluating two options: React Router and TanStack Router. Both libraries offer routing capabilities for React applications, but they differ in terms of features, flexibility, and performance.

## Considered Options

1. **React Router**
2. **TanStack Router**

### React Router

- **Pros:**

  - **Mature and Widely Used:** React Router is a well-established library with a large user base.
  - **Comprehensive Documentation:** The documentation is extensive and provides many examples.
  - **Integration:** Easy integration with other React libraries and tools.

- **Cons:**
  - **Complex API:** The API can be complex and sometimes counterintuitive for certain use cases.
  - **Performance Overhead:** Slightly higher performance overhead due to its comprehensive feature set.
  - **Less Flexibility:** Limited flexibility compared to newer alternatives like TanStack Router.

### TanStack Router

- **Pros:**

  - **Performance:** Offers better performance due to its lightweight and optimized implementation.
  - **Flexibility:** More flexible and customizable, allowing developers to tailor routing behavior to their needs.
  - **Modern Features:** Includes modern features and patterns that align well with contemporary React development practices.
  - **Active Development:** Actively maintained and regularly updated with new features and improvements.

- **Cons:**
  - **Smaller Community:** Smaller community and ecosystem compared to React Router.
  - **Learning Curve:** Steeper learning curve due to its flexibility and different approach compared to traditional routers.
  - **Documentation:** While improving, the documentation is not as comprehensive as React Router.

## Decision

After careful evaluation, we have decided to use TanStack Router for our web application's routing needs.

## Criteria for Evaluation

- Ease of Use and Learning Curve
- Performance
- Flexibility and Extensibility
- Community and Ecosystem
- Documentation and Support

### Ease of Use and Learning Curve

React Router has a gentler learning curve due to its widespread usage and comprehensive documentation. However, TanStack Router, while initially more challenging, offers greater long-term benefits in terms of flexibility and modern development practices.

### Performance

TanStack Router has shown to be more performant due to its lightweight nature and optimized design, making it a better choice for high-performance applications.

### Flexibility and Extensibility

TanStack Router excels in flexibility, providing more options for customization and extension, which is crucial for our application's complex routing requirements.

### Community and Ecosystem

React Router has a larger community and ecosystem, but TanStack Router's active development and modern approach are promising. The smaller community is a trade-off we are willing to accept for the benefits offered.

### Documentation and Support

React Router's documentation is more extensive, but TanStack Router's documentation is improving rapidly. Given the active development and responsiveness of the maintainers, we are confident in receiving adequate support.

## Consequences

### Positive

- Improved performance and flexibility in routing.
- Ability to leverage modern React features and patterns.
- Better customization options for our specific use cases.

### Negative

- Initial learning curve and adaptation period.
- Potential challenges due to a smaller community and ecosystem.

## Actions

- Schedule training sessions for the team to get familiar with TanStack Router.
- Update the project's documentation to reflect the new routing library.
- Start refactoring the existing codebase to integrate TanStack Router.

## Conclusion

We have decided to adopt TanStack Router for our web application. Despite its smaller community and steeper learning curve, its superior performance, flexibility, and alignment with modern React development practices make it the best choice for our needs. We believe that investing time in learning and adopting TanStack Router will provide long-term benefits for our application.

## Links

[tanstack router](https://tanstack.com/router/latest)
[react router](https://reactrouter.com/en/main)
