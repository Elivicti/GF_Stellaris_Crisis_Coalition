## 允许研究科技的条件

对于MOD中的每一个科技，均有一个`flag_can_research_$TECH$`标识与之唯一对应，其中`$TECH$`为该科技的`key`。

在这些科技的`potential`中，均定义有以下内容：

```pdx
GF_can_research_tech_trigger = { TECH = <科技key> }
```

其中`GF_can_research_tech_trigger`为`scripted_trigger`，定义如下：

```pdx
# this = country
GF_can_research_tech_trigger = {
	OR = {
		has_authority = GF_auth_commonwealth
		has_country_flag = flag_can_research_$TECH$
	}
}
```

它检查一个帝国是否拥有**联合政府**政体，或是否拥有`flag_can_research_$TECH$`标识，对于任何非**联合政府**政体的帝国来说，想要研究某项科技，就必须拥有与这个科技对应的可研究标识。

需要注意的是，有些科技并非只有`GF_can_research_tech_trigger`的检查，通常这些科技需要完成某些事件才能获得，例如，`GF_tech_collapse_relic_tech`的`potential`定义如下：

```pdx
GF_can_research_tech_trigger = { TECH = GF_tech_collapse_relic_tech }
has_country_flag = flag_GF_collapse_relic_surveyed
```

这表明`GF_tech_collapse_relic_tech`还需要探索完所有的**『遗迹』**考古点才能够研究。

> 有关特殊flag的更多内容参见：[flags & global_event_target.md](./flags & global_event_target.md)



### 基础人形科技

MOD中定义了一组基础人形科技，研究完成后，将可以拥有人形相关的功能，例如建造**人形组装厂**和**42Lab**等。当子**网类型附庸**到达二级时，将允许该帝国研究基础人形科技，当该帝国脱离其宗主后，将移除该帝国使用人形相关科技所提供功能的能力（科技一旦研究就无法移除了）。

要判断一个帝国是否可以研究基础人形科技，可以使用`GF_can_research_basic_doll_tech_trigger = yes`。

要允许非**联合政府**政体帝国研究基础人形科技，可以使用`GF_set_can_research_basic_doll_tech = yes`。

要移除非**联合政府**政体帝国研究研究基础人形科技的允许条件，可以使用`GF_set_cannot_research_basic_doll_tech = yes`。



### 快捷设置

要允许非**联合政府**政体帝国研究某项科技，可以使用`GF_set_can_research_tech`：

````pdx
GF_set_can_research_tech = { TECH = <科技key> }
````

要移除非**联合政府**政体帝国研究某项科技的允许条件，可以使用`GF_set_cannot_research_tech`：

```pdx
GF_set_cannot_research_tech = { TECH = <科技key> }
```



