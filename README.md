## Codility Lessons Solutions in Swift 3
Hey, just for  fun. Some solutions for [Codility](https://codility.com/programmers/) lesson for my reference or may benefit to others

#### Lesson 3 - FrogJmp
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

#### Lesson 3 - PermMissingElem
```swift
public func solution(_ A : inout [Int]) -> Int {
    
    let n = A.count + 1 // total elements including missing number
    
    // https://math.stackexchange.com/questions/2260/proof-for-formula-for-sum-of-sequence-123-ldotsn
    let sumN = n * (n + 1) / 2 // well know formula to get sums of sequence number from 1 .. N
    
    let sumA = A.reduce(0, +)
    
    return sumN - sumA // subtract and the balance is missing number
}

```

