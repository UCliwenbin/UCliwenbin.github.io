---
title: iOS-打包iPAi详解
date: 2024-01-13 21:05:15
tags:
---
## iOS-打包iPAi详解

```java
- (NSString *)convertPageIdFromPageId:(NSString *)fromPageId {
    NSString *trackingVCName = NSStringFromClass([self.item.viewController class]);
    if ([trackingVCName isEqualToString:@"HBNormalRouterPlanViewController"]) {
        if ([fromPageId isEqualToString:@"page_home"]) {
            return @"page_smart_route_detail";
        }
    }
    if ([trackingVCName isEqualToString:@"HBAppointRouterPlanViewController"]) {
        return @"page_smart_route_assign";
    }
    return fromPageId;
}
```