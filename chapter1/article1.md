# 我是有标题的哦

什么情况啊。。 难道给我注释掉了？？？？


```objectivec
+ (instancetype)shareInstance
{
    if (!_instance) {
        static dispatch_once_t onceToken;
        dispatch_once(&onceToken, ^{
            _instance = [[ZYLoginManager alloc] init];
        });
    }
    return _instance;
}

+ (instancetype)allocWithZone:(struct _NSZone *)zone
{
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        _instance = [super allocWithZone:zone];
        [[NSNotificationCenter defaultCenter] addObserver:_instance selector:@selector(loginSuccessNoti:) name:kZYLoginSuccessNotificationKey object:nil];
        [[NSNotificationCenter defaultCenter] addObserver:_instance selector:@selector(logoutSuccessNoti:) name:kZYLogoutSuccessNotificationKey object:nil];
    });
    return _instance;
}
```


```swift
var zy_viewController:UIViewController?{
        get{
            var next = self.next
            while next != nil {
                if next is UIViewController {
                    return next as! UIViewController?
                }
                next = next?.next
            }
            return nil
        }
    }
```

```objectivec

inline|auto|break|case|char|const

- (void)stopLoadingAnimation {
    if (_isAnimating) {
        [self.circleLayer removeAllAnimations];
    }
    _isAnimating = NO;
    [self.circleLayer setStrokeStart:0];
    [self.circleLayer setStrokeEnd:1];
    [self.circleLayer setStrokeColor:[(UIColor *)_colorArray.firstObject CGColor]];
}

- (NSArray*)prepareColorValues {
    NSMutableArray *cgColorArray = [[NSMutableArray alloc] init];
    for(UIColor *color in self.colorArray){
        [cgColorArray addObject:(id)color.CGColor];
    }
    return cgColorArray;
}

```
