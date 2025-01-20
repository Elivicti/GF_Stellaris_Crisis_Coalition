## OGAS领袖

OGAS是一个/类特殊领袖。

+ 对于**末日联合政府**，OGAS拥有标识`GF_ogas_leader`，而联合政府拥有标识`flag_GF_ogas_owner`
+ 对于**OGAS子网**，OGAS拥有标识`flag_GF_ogas_subnet_leader_@owner`

OGAS的**线程**由两个**国家域**的`scripted_modifier`实现：

+ `GF_OGAS_threads_add`：可用线程数
+ `GF_OGAS_threads_used_add`：线程占用数

要对OGAS的线程占用执行判断，可以使用`scripted_trigger`：

+ 检查占用是否超出可用线程：

	```pdx
	GF_OGAS_has_used_threads_over_cap = yes/no
	```

+ 检查是否还有可用线程：

	```pdx
	GF_OGAS_has_any_available_threads = yes/no
	```

+ 检查需要数量的可用线程数是否满足：

	```pdx
	GF_require_OGAS_has_available_threads = { amount = <int> }
	GF_require_OGAS_has_available_threads_with_trigger_icon = { amount = <int> }
	```

	这两个`scripted_trigger`将检查剩余的可用线程数是否**大于等于**`amount`。

	上述两个`scripted_trigger`判定失败时均会显示`custom_tooltip`，你需要定义对应的本地化键来显示文本（1~5已定义）：

	+ 前者：`GF_require_OGAS_has_available_threads_more_than_$amount$`
	+ 后者：`GF_require_OGAS_has_available_threads_more_than_$amount$_with_trigger_icon`

	注意：第二个`scripted_trigger`会额外显示一个`£trigger_no£`的图标。

线程占用溢出时（即占用数大于总可用数），将触发如下的`on_action`：

```pdx
# This = country
# From = any
on_OGAS_used_threads_over_cap = {}
```

> 详细说明参阅：[on_actions.md](on_actions.md)



## OGAS子网

OGAS子网是一个特殊的专家附庸类型，只有由**末日联合政府**释放的**星区附庸**可以使用。

当该类型的附庸达到**2级**专家特化等级时，该附庸的**政体**将会被更改为**OGAS子网**，统治者将会被更换为**OGAS**，并允许使用基础的人形科技。

对于由**末日联合政府**释放的**星区附庸**，该国家必定拥有标识`flag_GF_commonwealth_vassal`。



## OGAS通讯

OGAS通讯是一个特殊的机制，通过与名为**国家管理自动化系统**通讯，触发通讯事件来实现。

该名为**国家管理自动化系统**的国家拥有标识`flag_GF_ogas_country`和全局事件目标`event_target:GF_ogas_country`。

若要触发与**国家管理自动化系统**的通讯事件，国家首先应与**国家管理自动化系统**建立通讯，并拥有标识`flag_GF_can_contact_OGAS`。

然而，进一步的兼容接口并未开放，任何非**末日联合政府**政体的国家仅能触发子网附庸与OGAS通讯的事件。如果你需要兼容接口，请联系我们。







