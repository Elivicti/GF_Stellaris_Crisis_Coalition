## flag 标识

### flag命名规则

|     前缀      |       类型       |            说明            |
| :-----------: | :--------------: | :------------------------: |
|   `flag_GF`   |  `country_flag`  |                            |
|  `flag_p_GF`  |  `planet_flag`   |                            |
|  `flag_s_GF`  |   `star_flag`    |                            |
| `flag_pop_GF` |    `pop_flag`    |                            |
| `flag_sit_GF` | `situation_flag` |                            |
|  `flag_l_GF`  |  `leader_flag`   |  对于`OGAS`领袖，存在特例  |
|  `flag_g_GF`  |  `global_flag`   |                            |
|     `tmp`     |      `any`       | 临时`flag`，一般用完即移除 |

### 具有特殊功能的flag

|                       `flag`                       |      类型      |                           功能说明                           |
| :------------------------------------------------: | :------------: | :----------------------------------------------------------: |
|               `flag_GF_ogas_leader`                | `leader_flag`  |                       `OGAS`领袖的标识                       |
|        `flag_GF_ogas_subnet_leader_@subnet`        | `leader_flag`  | **子网类型**附庸的`OGAS`领袖的标识，`@subnet`为该领袖所属帝国的`id` |
|                `flag_GF_ogas_owner`                | `country_flag` |         `OGAS`的拥有者，通常为**联合政府**政体的帝国         |
|               `flag_GF_ogas_country`               | `country_flag` |                     `OGAS`通讯国家的标识                     |
|             `flag_GF_can_contact_OGAS`             | `country_flag` |                    允许与`OGAS`通讯的标识                    |
|             `flag_can_research_$TECH$`             | `country_flag` |                  允许研究`$TECH$`科技的标识                  |
|           `flag_GF_commonwealth_vassal`            | `country_flag` |           由**联合政府**政体的帝国所释放的星区附庸           |
|    `flag_GF_commonwealth_vassal_OGAS_subnet_1`     | `country_flag` |                  **子网类型**附庸标识：一级                  |
|    `flag_GF_commonwealth_vassal_OGAS_subnet_3`     | `country_flag` |                  **子网类型**附庸标识：二级                  |
|    `flag_GF_commonwealth_vassal_OGAS_subnet_3`     | `country_flag` |                  **子网类型**附庸标识：三级                  |
|             `flag_GF_GAVIRUL_species`              | `species_flag` |                 作为受到遗迹影响的物种的标识                 |
| `flag_p_GF_capture_bombardment_capture_inhibitor`  | `planet_flag`  |           禁止**协议同归**轨道轰炸捕获该星球的人口           |
| `flag_p_GF_planet_cannot_be_bombarded_to_collapse` | `planet_flag`  |   禁止**坍塌液脏弹**轨道轰炸将该星球轰炸为**坍塌死寂星球**   |
|         `flag_p_GF_is_habitat_type_planet`         | `planet_flag`  |       该星球在**坍塌液脏弹**轨道轰炸中将被认定为居住站       |

对于`OGAS`相关的内容，更详细的描述见：[OGAS.md](./OGAS.md)

对于研究科技的标识，更详细的描述见：[technologies.md](./technologies.md)

对于轨道轰炸的内容，更详细的描述见：[bombardment.md](./bombardment.md)

### 事件/特殊项目完成标识

|                         `flag`                          |      类型      |                            说明                            |
| :-----------------------------------------------------: | :------------: | :--------------------------------------------------------: |
|            `flag_GF_collapse_relic_surveyed`            | `country_flag` |               探索完所有的**『遗迹』**考古点               |
|           `flag_GF_gavirul_project_completed`           | `country_flag` |               完成**特殊项目**`GAVIRUL`计划                |
|         `flag_GF_relic_orb_mainframe_alpha_get`         | `country_flag` | 完成**受难之路**事件链后，获得遗珍**神秘的球形主机阿尔法** |
| `flag_GF_artifact_analyse_orb_mainframe_alpha_finished` | `country_flag` |    完成对**神秘的球形主机阿尔法**的研究，允许开启该遗珍    |

`GAVIRUL`计划完成后，拥有`flag_GF_GAVIRUL_species`标识的物种将允许通过**基因修饰**获得**坍塌辐射完全免疫**特质。



## global_event_target 全局目标

|            名称            |  域类型   |                             说明                             |
| :------------------------: | :-------: | :----------------------------------------------------------: |
|     `GF_ogas_country`      | `country` |                        `OGAS`通讯国家                        |
|      `GF_ogas_owner`       | `country` |           `OGAS`的拥有者，通常为联合政府政体的帝国           |
|      `GF_ogas_leader`      | `leader`  |                          `OGAS`领袖                          |
| `GF_doll_species_template` | `species` | 人形物种的模板，每年选定特质数最多的一个，用于会生成人形人口的事件中 |
|      `GF_home_world`       | `planet`  |            联合政府政体帝国的母星，通常为**地球**            |
| `aggressive_elid_country`  | `country` |              `ELID`进攻事件中，`ELID`所属的帝国              |
| `aggressive_elid_species`  | `species` |              `ELID`进攻事件中，`ELID`使用的物种              |







