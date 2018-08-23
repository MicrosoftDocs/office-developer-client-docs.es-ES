---
title: Información sobre la máquina de estados de replicación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 30dd43a3ac9a315cd41919872b918bee639ca259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593056"
---
# <a name="about-the-replication-state-machine"></a>Información sobre la máquina de estados de replicación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene una visión general de la máquina de estado de la replicación de datos de Microsoft Outlook 2013 y Microsoft Outlook 2010.
  
> [!NOTE]
> La API de replicación debe implementarse totalmente según las instrucciones de este tema para que sea útil o son compatibles. La API de replicación está disponible exclusivamente para replicar cambios de 2013 de Outlook o Outlook 2010 a y desde un servidor. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX y la máquina de Estados

Un cliente llama a **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** y **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** en una secuencia para sincronizar las carpetas de Outlook 2013 o Outlook 2010 y los elementos entre un almacén local y un servidor. La secuencia de llamadas real depende de los datos que se deben replicar (por ejemplo, una jerarquía de carpetas de Outlook 2013 o Outlook 2010, un Outlook 2013 o carpeta de Outlook 2010, elementos de correo, elementos de calendario etc.) y la dirección de sincronización (si cargar desde el almacén local en el servidor, o descargar desde el servidor en el almacén local). Aquí es una secuencia típica de llamadas: 
  
1. El cliente llama a **IOSTX::SyncBeg** para comenzar la replicación, que especifica un identificador de estado y un puntero a una dirección de una estructura de datos correspondiente. 
    
2. 2013 de Outlook o Outlook 2010 asigna la estructura de datos e inicializa la estructura de datos con la información necesaria para el cliente. 
    
3. El cliente realiza la replicación, actualizar la estructura de datos para transmitir en el almacén local de toda la información necesaria acerca de la replicación.
    
4. Después de realizar la replicación, el cliente llama a **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** y **IOSTX::SyncEnd** para notificar el almacén local de la finalización de la replicación específica. 
    
> [!NOTE]
> El cliente llama siempre **IOSTX::SyncEnd** para finalizar una replicación que ha comenzado el cliente para un estado determinado. Según los datos generales que se debe sincronizar el cliente, el cliente puede llamar a la par de las llamadas **IOSTX::SyncBeg** y **IOSTX::SyncEnd** más de una vez. 
  
## <a name="state-table"></a>Tabla de Estados

> [!NOTE]
> En la siguiente tabla se enumera todos los estados válidos en la máquina de estado de replicación, junto con los identificadores de estado correspondiente y estructuras de datos. En la columna **Datos replicado** , el término "elementos" incluye correo, calendario, contactos, tenga en cuenta, diario y elementos de tarea. Al replicar los cambios en el almacén local en el servidor, use los identificadores de estado que se especifica "Cargar" y estructuras de datos con el prefijo "Seguridad" (por ejemplo, **LR_SYNC_UPLOAD_HIERARCHY** y **[UPHIER](uphier.md)** ). Al replicar los cambios desde el servidor en el almacén local, use los identificadores de estado que se especifica "Descargar" y estructuras de datos con el prefijo "DN" (por ejemplo, **LR_SYNC_DOWNLOAD_HIERARCHY** y **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Datos replicados** <br/> |**Identificador de estado** <br/> |**Estructura de datos** <br/> |
|[Estado de inactividad](idle-state.md) <br/> | *None*  <br/> |**LR_SYNC_IDLE** <br/> | *None*  <br/> |
|[Sincronizar estado](synchronize-state.md) <br/> |Las carpetas o elementos  <br/> |**LR_SYNC** <br/> |**[SYNC](sync.md)** <br/> |
|[Cargar el estado de la jerarquía](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Cargar el estado de la carpeta](upload-folder-state.md) <br/> |Folder  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Sincronizar el estado del contenido](synchronize-contents-state.md) <br/> |Items  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Cargar el estado de la tabla](upload-table-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Cargar el estado del mensaje](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Cargar el estado de lectura](upload-read-status-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Cargar Eliminar estado estado](upload-delete-status-state.md) <br/> |Items  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Estado de la jerarquía de descarga](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Estado de la tabla de descarga](download-table-state.md) <br/> |Items  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Estado del encabezado de mensaje de descarga](download-message-header-state.md) <br/> |Encabezado de mensaje  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Diagrama de transición de estado

El siguiente diagrama muestra las transiciones de estado que se producen al cargar o realizar una sincronización completa (descarga seguida de carga) de las carpetas o el contenido de las carpetas (correo, calendario, contactos, tenga en cuenta, tarea o los elementos del diario). 
  
@@@NEED A LA ILUSTRACIÓN DE INSERTAR AQUÍ QUE FALTA @@@
  
## <a name="example-uploading-a-folder-hierarchy"></a>Ejemplo: Carga de una jerarquía de carpetas

 Cuando se carga una jerarquía de carpetas, la siguiente secuencia de pasos lleva a cabo: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Paso** <br/> |**Acción** <br/> |**State** <br/> |**Estructura de datos relacionados** <br/> |
|1.  <br/> |El cliente inicia la carga de jerarquía con **IOSTX::SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |2013 de Outlook o Outlook 2010 **UPHIER** rellena con información para el cliente. Esto incluye la inicialización de los parámetros [out]: *iEnt* se establece en 0 y *cEnt* para el número de carpetas de la jerarquía que se debe cargar.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |El cliente realiza la carga de jerarquía real. Por ejemplo, si *cEnt* es 10, para cada una de las carpetas de 10, el cliente llama a **IOSTX::SyncBeg**, que especifica el identificador de estado apropiado y la estructura de datos para cargar una carpeta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |2013 de Outlook o Outlook 2010 rellena **UPFLD** inicializar sus parámetros [out], incluidos el motivo de la carga de la carpeta, el puntero al objeto de carpeta y el identificador de entrada de la carpeta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |El cliente de carga de la carpeta especificada.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |El cliente se lo comunica el almacén local de la finalización de la carga de carpeta: si tiene éxito, el cliente establece el [in] el parámetro *ulFlags* en **UPFLD** con **UPF_OK**y, a continuación, llama a **IOSTX::SetSyncResult (S_OK)** y **IOSTX::SyncEnd **. Al producirse un error, el cliente no debe establecer *ulFlags* con la marca **UPF_OK** . Se llama **IOSTX::SetSyncResult**, pasando el valor **HRESULT** y **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Si se establece **UPF_OK** , Outlook 2013 o Outlook 2010 borrará la solicitud interna para cargar la carpeta. A continuación, independientemente del estado de *ulFlags* , va a limpiar cualquier información de contabilidad interna. Mientras aún hay carpetas en la jerarquía para cargar (*iEnt* es aún menos *cEnt*), el cliente y 2013 de Outlook o Outlook 2010 Repita los pasos 3 a 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |El cliente se lo comunica el almacén local de la finalización de la carga de jerarquía: si tiene éxito, el cliente establece el [in] marcar en **UPHIER** con **UPH_OK**y, a continuación, llama a **IOSTX::SetSyncResult (S_OK)** y **IOSTX::SyncEnd**. Al producirse un error, el cliente no debe establecer la marca **UPH_OK** . Se llama **IOSTX::SetSyncResult**, pasando el valor **HRESULT** y **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Si se establece **UPH_OK** , Outlook 2013 o Outlook 2010 borrará la solicitud interna para cargar la jerarquía. A continuación, independientemente del estado de *ulFlags* , va a limpiar cualquier información de contabilidad interna.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

