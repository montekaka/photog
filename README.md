# photog
One Month iOS tutorial

## Day 3
Follow instruction from parse.com

## Day 4

```swift
    func application(application: UIApplication, didFinishLaunchingWithOptions launchOptions: [NSObject: AnyObject]?) -> Bool {
        // Override point for customization after application launch.
        self.setupParse()
        
        self.window = UIWindow(frame: UIScreen.mainScreen().bounds)
        
        if PFUser.currentUser() == nil{
            // TODO: present the main UI
            println("User does not exist")
        }
        else{
            // TODO: Present UI for logging in or creating an account
            println("We have an user")
        }
        
        return true
    }
    
func setupParse(){
        Parse.setApplicationId(_applicationID_, clientKey:_clientKey_)
}
```

Create a StartViewController file inherts from UIViewController with a xib file, and then add the following code
```swift
var startViewController = StartViewController(nibName:"StartViewController", bundle:nil)

if PFUser.currentUser() == nil{
    // TODO: present the main UI
    navigationController.viewControllers = [startViewController]
}
else{
    // TODO: Present UI for logging in or creating an account
    println("We have an user")
}
    self.window!.rootViewController = navigationController
    self.window!.makeKeyAndVisible()    
```

## Day 5
Adding buttons to the login screen
