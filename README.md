# Swift-Tableview-Practice
I'm making a tutorial soon soooooooo just practicing

### Step 1
We gotta get rid of these storyboards. Please. XCode devs made it a nightmare to run storyboard based projects.
- Create new iOS project and select user interface as storyboard and not SwiftUI
- Delete the Storyboard file
- Remove the Main Interface from the General Tab
- Delete storyboard file from info.pilst. Keep drilling starting Application Scene Manifest until you find it
- Set your root VC from the scenedelete.swift file. your code should look like:
```
func scene(_ scene: UIScene, willConnectTo session: UISceneSession, options connectionOptions: UIScene.ConnectionOptions) {
    guard let windowScene = (scene as? UIWindowScene) else { return }
    window = UIWindow(frame: windowScene.coordinateSpace.bounds)
    window?.windowScene = windowScene
    window?.rootViewController = ViewController()
    window?.makeKeyAndVisible()
}
```
- Run to test 


### Step 2