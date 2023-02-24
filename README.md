# UIViewController Lifecycle

In iOS each one can create views using storyboards, xibs or programmatically (ViewCode).
Independent from the approach, one need to understand when the view is created, loaded, appeared or destroyed so improves could be implemented for user interface.

Therefore, understanding all lifecycle methods not only helps in code, but also enables creativity implementing advanced user interfaces.

## UIViewController

It manages an `UIKit` app interface, and a single root `UIView`. Such a root view may itself contain any number of subviews. User interactions with such view hierarchy are handled by your _view controller_, which coordenates with other objects of your app as needed.

So a view controller's main responsabilities inclue the following:

- Updating the contents of the views, usually in response to changes to the underlying data
- Responding to user interactions with views
- Resizing views and managing the layout of the overall interface
- Coordenation with other objects in your app. This could include other view controllers as well

## View lifecycle methods

1. `loadViewIfNeeded()`
   1. Loads the view controller’s view from its storyboard file, or creates the view as needed based on the established rules.
2. `loadView()`
   1. Should never be called directly. The view controller calls this method when its view property is requested but is currently nil. This method loads or creates a view and assigns it to the view property.
   2. If the view controller does not have an associated nib file, this method creates a plain UIView object instead.
   3. You can override this method in order to create your views manually. If you choose to do so, assign the root view of your view hierarchy to the view property. The views you create should be unique instances and should not be shared with any other view controller object. Your custom implementation of this method should not call super
   4. [Link](https://developer.apple.com/documentation/uikit/uiviewcontroller/1621454-loadview) to full documentation
3. `viewDidLoad()`
   1. This method is called after the view controller has loaded its view hierarchy into memory. This method is called regardless of whether the view hierarchy was loaded from a nib file or created programmatically in the loadView() method. 
   2. You usually override this method to perform additional initialization on views that were loaded from nib files.
4. `viewWillAppear(_ animated: Bool)`
   1. Prepare the views for appearing on screen
5. `viewWillLayoutSubviews()`
6. `viewDidLayoutSubviews()`
7. `viewDidAppear(_ animated: Bool)`
8. `viewWillDisappear(_ animated: Bool)`
   1. Should be used to save changes or other state information
9. `viewDidDisappear(_ animated: Bool)`

