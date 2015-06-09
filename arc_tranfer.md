使用 __bridge_transfer(),
从 Core Foundation 传递所有权给 Objective-C;
使用 CFBridgingRetain(),从 Objective-C 传递所有权给 Core Foundation;
使用__brideg,表示临时使用某种类型,不改变对象的所有权

__bridge_transfer:给予 ARC 所有权,arc管理；
__bridge_retained:解除 ARC 所有权，arc 不在管理，自己手动管理；