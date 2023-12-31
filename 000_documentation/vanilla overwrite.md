本文档记录了所有覆盖的原版条目。



## 陆军

|        `key`        |                     说明                     |
| :-----------------: | :------------------------------------------: |
|   `assault_army`    | 禁止拥有**仿生自律人形**特质的物种生成该陆军 |
|    `slave_army`     | 禁止拥有**仿生自律人形**特质的物种生成该陆军 |
|    `clone_army`     | 禁止拥有**仿生自律人形**特质的物种生成该陆军 |
|   `psionic_army`    | 禁止拥有**仿生自律人形**特质的物种生成该陆军 |
| `gene_warrior_army` | 禁止拥有**仿生自律人形**特质的物种生成该陆军 |
|    `undead_army`    | 禁止拥有**仿生自律人形**特质的物种生成该陆军 |
|  `occupation_army`  | 禁止拥有**仿生自律人形**特质的物种生成该陆军 |

文件：

+ `common/armies/y_assult_armies.txt`
+ `common/armies/y_occupation_armies.txt`



## 飞升

|           `key`           |                   说明                   |
| :-----------------------: | :--------------------------------------: |
| `ap_engineered_evolution` | 禁止拥有**联合政府**政体的帝国使用该飞升 |
|  `ap_the_flesh_is_weak`   | 禁止拥有**联合政府**政体的帝国使用该飞升 |
| `ap_synthetic_evolution`  | 禁止拥有**联合政府**政体的帝国使用该飞升 |
|   `ap_mind_over_matter`   | 禁止拥有**联合政府**政体的帝国使用该飞升 |

文件：

+ `common/ascenion_perks/y_ascension_perks.txt`



## 经济类型

|      `key`       |              说明               |
| :--------------: | :-----------------------------: |
| `megastructures` | 生成全部类型的`add`与`mult`修正 |

文件：

+ `common/economic_categories/99_GF_common_categories_overrite.txt`



### 全局规则

|                  `key`                  |                             说明                             |
| :-------------------------------------: | :----------------------------------------------------------: |
|      `species_can_live_on_planet`       | 允许拥有**仿生自律人形**特质的物种殖民**机械星球**，允许**机械物种**殖民**神秘的机械星球** |
|     `can_generate_leader_from_pop`      |                  **人形**人口产生领袖的规则                  |
| `can_generate_military_leader_from_pop` |                **人形**人口产生军事领袖的规则                |
|       `can_species_be_assembled`        |        允许拥有**仿生自律人形**特质的物种被组装的规则        |
|       `can_build_branch_offices`        |   拥有**格里芬与克鲁格安全承包商**国民理念时，允许开设分部   |
|      `can_support_branch_offices`       | 禁止在拥有**格里芬与克鲁格安全承包商**国民理念的帝国境内开设分部 |
|        `can_crossbreed_species`         |            禁止拥有**仿生自律人形**特质的物种杂交            |
|        `can_fill_specialist_job`        |   拥有**仿生自律人形**特质的人口能够担任**专家岗位**的规则   |
|          `can_fill_ruler_job`           |  拥有**仿生自律人形**特质的人口能够担任**统治者岗位**的规则  |
|           `can_trade_leader`            | **联合政府**政体的帝国与**子网类型附庸**交易**机械领袖**的规则 |

文件：

+ `common/game_rules/y_game_rules.txt`



## 封装条件

|               `key`               |                            说明                            |
| :-------------------------------: | :--------------------------------------------------------: |
|           `is_megacorp`           | 拥有**格里芬与克鲁格安全承包商**国民理念的帝国被认为是巨企 |
|     `is_special_colony_type`      |            **自动化星球**被认为是特殊殖民地类型            |
|  `entertainer_job_check_trigger`  |  拥有**仿生自律人形**特质的人口能够担任**娱乐岗位**的条件  |
| `battle_thrall_job_check_trigger` |  拥有**仿生自律人形**特质的人口能够担任**暴力岗位**的条件  |
|        `can_set_ai_policy`        |   禁止**联合政府**与**子网类型附庸**使用**人工智能**政策   |

文件：

+ `common/scripted_triggers/y_scripted_triggers.txt`



## 科技

|            `key`            |                   说明                   |
| :-------------------------: | :--------------------------------------: |
|   `tech_robotic_workers`    | 禁止拥有**联合政府**政体的帝国研究该科技 |
|    `tech_droid_workers`     | 禁止拥有**联合政府**政体的帝国研究该科技 |
|  `tech_synthetic_workers`   | 禁止拥有**联合政府**政体的帝国研究该科技 |
|  `tech_synthetic_leaders`   | 禁止拥有**联合政府**政体的帝国研究该科技 |
|     `tech_robomodding`      | 禁止拥有**联合政府**政体的帝国研究该科技 |
| `tech_robomodding_points_1` | 禁止拥有**联合政府**政体的帝国研究该科技 |
| `tech_robomodding_points_2` | 禁止拥有**联合政府**政体的帝国研究该科技 |

文件：

+ `common/technology/y_eng_tech.txt`
+ `common/technology/y_synthetic_dawn_tech.txt`



## 其他

|                      文件                       |             `key`             |               说明               |
| :---------------------------------------------: | :---------------------------: | :------------------------------: |
| `gfx/models/planets/y_bombardment_entity.asset` | `orbital_bombardment_effects` | 添加**坍塌液脏弹**轰炸姿态的特效 |

