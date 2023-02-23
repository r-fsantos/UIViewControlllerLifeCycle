# UIViewController Lifecycle

In iOS each one can create views using storyboards, xibs or programmatically (ViewCode).
Independent from the approach, one need to understand when the view is created, loaded, appeared or destroyed so improves could be implemented for user interface.

Therefore, understanding all lifecycle methods not only helps in code, but also enables creativity implementing advanced user interfaces.

## View lifecycle methods

1. `loadViewIfNeeded()`
2. `loadView()`
3. `viewDidLoad()`
4. `viewWillAppear(_ animated: Bool)`
5. `viewWillLayoutSubviews()`
6. `viewDidLayoutSubviews()`
7. `viewDidAppear(_ animated: Bool)`
8. `viewWillDisappear(_ animated: Bool)`
9. `viewDidDisappear(_ animated: Bool)`

