Student Course Portal - Phase 2: Services, State & Testing
The second phase transitions from UI/UX into enterprise-grade architecture, focusing on data persistence, complex routing, NgRx state management, and quality assurance through unit testing.


Hands-On 06: Dependency Injection & Services
Singleton Pattern: Created a CourseService provided in root to ensure a single source of truth for course data.
Service Composition: Injected CourseService into EnrollmentService to demonstrate how Angular handles hierarchical dependencies.
State Sharing: Shared data seamlessly between the Dashboard and Course list without complex parent-child chains.


Hands-On 07: Advanced Routing & Guards
Navigation: Implemented dynamic routing (/courses/:id) and query parameters for search functionality.
Performance: Configured Lazy Loading for the Enrollment feature module to reduce the initial bundle size.
Security:
AuthGuard: Protected the profile and enrollment pages.
UnsavedChangesGuard: A CanDeactivate guard to warn users if they try to leave a dirty form.


Hands-On 08: API Integration (RxJS)
HttpClient: Replaced mock arrays with real HTTP calls to a JSON Server.
RxJS Power:
Used pipe() with map, tap, and catchError for robust data streams.
Implemented switchMap to cancel obsolete requests and retry() for handling intermittent network failures.
Interceptors: Created an AuthInterceptor to automatically attach Bearer tokens to every request and a global LoadingInterceptor for a unified UI spinner.


Hands-On 09: NgRx State Management
Redux Pattern: Migrated local service state to a global NgRx Store.
Workflow: Defined Actions for loading, Reducers for immutable state updates, and Memoized Selectors for high-performance data retrieval.
Effects: Handled asynchronous API side-effects using @ngrx/effects, keeping components purely focused on the UI.


Hands-On 10: Unit Testing (Jasmine/Karma)
Component Testing: Wrote tests for CourseCardComponent to verify @Input rendering and @Output event emission.
Service Testing: Used HttpClientTestingModule and HttpTestingController to mock API responses and verify error handling logic.
State Testing: Utilized provideMockStore to test components in different states (Loading vs. Data vs. Error) without needing the full NgRx setup.


Key Takeaway
"Implementing NgRx was a turning point. It decoupled the UI from the business logic, making the application state predictable and easy to debug using Redux DevTools. Combining this with a 90%+ test coverage ensures the app remains stable as it scales."