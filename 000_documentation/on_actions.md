本文档列出了所有可用于兼容的`on_action`接口。



## 坍塌液脏弹轰炸

当星球被**坍塌液脏弹**姿态轰炸到**0人口**时，若触发星球被彻底毁灭的效果，将先后触发以下`on_action`：

```pdx
# This = country (轰炸者)
# From = planet
on_planet_bombarded_to_collapse_bombarder = {}
```

```pdx
# This = country (行星所有者)
# From = planet
# FromFrom = fleet (轰炸者)
on_planet_bombarded_to_collapse_victim = {}
```

> 有关坍塌液脏弹的说明，参阅[bombardment.md](bombardment.md)



## 巨像武器：终末辉光

```pdx
# this/root = planet (终末辉光发射的目标)
# from = fleet (发射者，即巨像)
on_destroy_planet_with_PLANET_KILLER_GF_COLLAPSE_ENDING_FLASH = {}
```



## OGAS线程占用溢出

当OGAS线程的占用数超过可用数时触发，该`on_action`触发的时间在实际占用溢出的**5天**后。

```pdx
# This = country
# From = any
on_OGAS_used_threads_over_cap = {}
```

注意：`from`域是任意的，通常由触发源指定，代表导致占用溢出的源头域，例如，建造自动化星球导致的占用溢出。

使用`scripted_effect`来检查OGAS线程占用是否溢出：

```pdx
# this = country
GF_check_OGAS_threads_over_cap_effect = { from = <scope> }
```

注意，必须指定`from`，用于代表导致占用溢出的源头。

> 有关OGAS线程的说明，参阅[OGAS.md](OGAS.md)

