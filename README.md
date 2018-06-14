# Ejecutar-codigo-cuando-se-reactiva-el-app-fuera-el-app-delegate-swift

```

override func viewDidLoad() {
        super.viewDidLoad()

        NotificationCenter.default.addObserver(self, selector: #selector(willEnterForeground(_:)), name: .UIApplicationWillEnterForeground, object: nil)

    }

    func willEnterForeground(_ notification: NSNotification!) {
        // do whatever you want when the app is brought back to the foreground
    }

    deinit {
        // make sure to remove the observer when this view controller is dismissed/deallocated

        NotificationCenter.default.removeObserver(self)
    }
    
    ```
