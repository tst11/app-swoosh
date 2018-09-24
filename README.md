# app-swoosh

Custom styles in /Views/BorderButton.swift 

add new group Views, new file -> Cocoa Touch Class, subclass of uibutton, class BorderButton, next, create

```swift
//
//  BorderButton.swift
//  app-swoosh
//
//  Created by Tadas on 01/09/2018.
//  Copyright © 2018 Tadas. All rights reserved.
//

import UIKit

class BorderButton: UIButton {

    override func awakeFromNib() {
        super.awakeFromNib()
        layer.borderWidth = 2.0
        layer.borderColor = UIColor.white.cgColor
    }

}
```

Old style centering and positioning elements in ios:

```swift
class ViewController: UIViewController {
    @IBOutlet weak var swoosh: UIImageView!
    @IBOutlet weak var bgImg: UIImageView!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        swoosh.frame = CGRect(x: view.frame.size.width / 2 - swoosh.frame.size.width / 2, y: 50, width: swoosh.frame.size.width, height: swoosh.frame.size.height)
        
        bgImg.frame = view.frame
        
    }
}
```