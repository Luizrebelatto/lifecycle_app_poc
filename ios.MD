# IOS LifeCycle

### viewDidLoad

- when the view is loaded

```swift
import UIKit

class CounterViewController: UIViewController {

    private var count = 0
    private let label = UILabel()
    private let button = UIButton(type: .system)

    override func viewDidLoad() {
        super.viewDidLoad()
        print("viewDidLoad")

        view.backgroundColor = .white

        label.text = "Contador: 0"
        label.translatesAutoresizingMaskIntoConstraints = false

        button.setTitle("Incrementar", for: .normal)
        button.translatesAutoresizingMaskIntoConstraints = false
        button.addTarget(self, action: #selector(increment), for: .touchUpInside)

        view.addSubview(label)
        view.addSubview(button)

        NSLayoutConstraint.activate([
            label.centerXAnchor.constraint(equalTo: view.centerXAnchor),
            label.centerYAnchor.constraint(equalTo: view.centerYAnchor),

            button.topAnchor.constraint(equalTo: label.bottomAnchor, constant: 20),
            button.centerXAnchor.constraint(equalTo: view.centerXAnchor)
        ])
    }
}
```

### viewWillAppear

- Before the screen appears
- update interface
- reload api

```swift
override func viewWillAppear(_ animated: Bool) {
    super.viewWillAppear(animated)
    print("viewWillAppear")
}
```

### viewDidAppear

- after appear
- show warning on console
- init animations

```swift
override func viewWillAppear(_ animated: Bool) {
        super.viewWillAppear(animated)
        print("viewWillAppear")
    }
```
