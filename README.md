**NOTICE**

The distributedschedule_safwk_lite repository is renamed systemabilitymgr_safwk_lite since August 2022. The distributedschedule_safwk_lite repository is archived and no longer maintained.

To obtain the latest code, go to [**systemabilitymgr\_safwk_lite**](https://gitee.com/openharmony/systemabilitymgr_safwk_lite).

# safwk\_lite<a name="ZH-CN_TOPIC_0000001081445008"></a>


## Introduction<a name="section11660541593"></a>

The  **safwk\_lite**  module provides an empty process for running basic services.

## Architecture<a name="section342962219551"></a>

**Figure 1** Service-oriented architecture


![](figures/en-us_image_0000001128146921.png)


## Directory Structure<a name="section1464106163817"></a>

The following table describes the directory structure of the Distributed Scheduler.

**Table 1**  Directory structure of the major source code

<a name="table43531856201716"></a>
<table><thead align="left"><tr id="row20416556201718"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p10416456121716"><a name="p10416456121716"></a><a name="p10416456121716"></a>Directory</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p1841645631717"><a name="p1841645631717"></a><a name="p1841645631717"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row104169564177"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p17416125614179"><a name="p17416125614179"></a><a name="p17416125614179"></a>safwk_lite</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p04163569170"><a name="p04163569170"></a><a name="p04163569170"></a>Implementation of the foundation process</p>
</td>
</tr>
</tbody>
</table>

The source code directory structure of the  **safwk\_lite**  module is as follows:

```
├── BUILD.gn
├── readme.md
├── LICENSE
├── src
    └── main.c
```

## Usage<a name="section10729231131110"></a>

Add a service to the foundation process.

After writing the service based on the service template, add the dependencies to the  **BUILD.gn**  file.

```
deps = [
  "${aafwk_lite_path}/services/abilitymgr_lite:abilityms",
  "${appexecfwk_lite_path}/services/bundlemgr_lite:bundlems",
  "//base/hiviewdfx/hilog_lite/frameworks/featured:hilog_shared",
  "//base/security/permission_lite/services/ipc_auth:ipc_auth_target",
  "//base/security/permission_lite/services/pms:pms_target",
  "//foundation/ability/dmsfwk_lite:dtbschedmgr",
  "//foundation/distributedschedule/samgr_lite/samgr_server:server",
]
```

## Repositories Involved<a name="section176111311166"></a>

safwk

[distributedschedule\_safwk](https://gitee.com/openharmony/distributedschedule_safwk)

[distributedschedule\_samgr](https://gitee.com/openharmony/distributedschedule_samgr)

[**distributedschedule\_safwk\_lite**](https://gitee.com/openharmony/distributedschedule_safwk_lite)

[distributedschedule\_samgr\_lite](https://gitee.com/openharmony/distributedschedule_samgr_lite)