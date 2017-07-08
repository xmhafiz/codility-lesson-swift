## Codility Lessons Solutions in Swift 3
Hey, just for a fun. Some solutions for [Codility](https://codility.com/programmers/) lesson for my reference or may benefit to others

### Lesson 3 - FrogJmp
```swift
public func solution(_ X : Int, _ Y : Int, _ D : Int) -> Int {
    
    if X == Y { return 0 }
    
    var count = 0
    
    if (Y - X) % D == 0 {
        count = (Y - X) / D
    }
    else {
        count = (Y - X) / D + 1
    }
    
    return count
}
```


