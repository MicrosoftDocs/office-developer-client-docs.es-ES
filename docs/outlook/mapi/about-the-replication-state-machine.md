---
title: Información sobre la máquina de estados de replicación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf36c6cb-57b4-7b2b-e23d-e0bc8696de96
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a0644e4bf5c6847d61cc59e203d50f61ad142e84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416485"
---
# <a name="about-the-replication-state-machine"></a>Información sobre la máquina de estados de replicación

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene información general sobre la máquina de estado para Microsoft Outlook 2013 y la replicación de datos 2010 de Microsoft Outlook.
  
> [!NOTE]
> La API de replicación debe implementarse por completo de acuerdo con las instrucciones de este tema para ser útil o compatible. La API de replicación está disponible exclusivamente para replicar Outlook 2013 o Outlook 2010 cambios en y desde un servidor. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX y la máquina de Estados

Un cliente llama a **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, **[IOSTX:: SyncEnd](iostx-syncend.md)**, **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** y **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** en una secuencia para sincronizar las carpetas y elementos de Outlook 2013 o Outlook 2010 entre un almacén local y un servidor. La secuencia real de llamadas depende de los datos que se deben replicar (por ejemplo, una jerarquía de carpetas de Outlook 2013 o de Outlook 2010, una carpeta de Outlook 2013 o Outlook 2010, elementos de correo, elementos de calendario, etc.) y la dirección de sincronización (si cargar desde el almacén local al servidor o descargar del servidor al almacén local). A continuación se muestra una secuencia típica de llamadas: 
  
1. El cliente llama a **IOSTX:: SyncBeg** para comenzar la replicación, especificando un identificador de estado y un puntero a una dirección de una estructura de datos correspondiente. 
    
2. Outlook 2013 o Outlook 2010 asigna la estructura de datos e inicializa la estructura de datos con la información necesaria para el cliente. 
    
3. El cliente realiza la replicación, actualizando la estructura de datos para transmitir al almacén local la información necesaria sobre la replicación.
    
4. Después de realizar la replicación, el cliente llama a **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** y **IOSTX:: SyncEnd** para notificar al almacén local que se ha completado la replicación específica. 
    
> [!NOTE]
> El cliente siempre llama a **IOSTX:: SyncEnd** para finalizar una replicación que el cliente ha iniciado para un estado determinado. En función de los datos generales que el cliente necesita sincronizar, el cliente puede llamar al par de llamadas **IOSTX:: SyncBeg** y **IOSTX:: SyncEnd** más de una vez. 
  
## <a name="state-table"></a>Tabla de estado

> [!NOTE]
> En la siguiente tabla se enumeran todos los Estados válidos de la máquina de estado de replicación, junto con los identificadores de estado y las estructuras de datos correspondientes. En la columna **replicaDa datos** , el término "items" incluye correo, calendario, contacto, nota, diario y elementos de tarea. Cuando replique cambios del almacén local al servidor, use los identificadores de estado que especifican la "carga" y las estructuras de datos con el prefijo "arriba" (por ejemplo, **LR_SYNC_UPLOAD_HIERARCHY** y **[UPHIER](uphier.md)** ). Cuando replique cambios del servidor en el almacén local, use los identificadores de estado que especifican la "descarga" y las estructuras de datos con el prefijo "DN" (por ejemplo, **LR_SYNC_DOWNLOAD_HIERARCHY** y **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**State** <br/> |**Datos replicados** <br/> |**Identificador de estado** <br/> |**Estructura de datos** <br/> |
|[Estado inactivo](idle-state.md) <br/> | *Ninguno*  <br/> |**LR_SYNC_IDLE** <br/> | *Ninguno*  <br/> |
|[Estado de sincronización](synchronize-state.md) <br/> |Carpetas o elementos  <br/> |**LR_SYNC** <br/> |**[SINCRONIZÁNDOSE](sync.md)** <br/> |
|[Cargar estado de la jerarquía](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Cargar estado de la carpeta](upload-folder-state.md) <br/> |Folder  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Estado de sincronización de contenido](synchronize-contents-state.md) <br/> |Elementos  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Cargar estado de la tabla](upload-table-state.md) <br/> |Elementos  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Cargar estado del mensaje](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Cargar estado de lectura de estado](upload-read-status-state.md) <br/> |Elementos  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Cargar estado de eliminación de estado](upload-delete-status-state.md) <br/> |Elementos  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Descargar estado de jerarquía](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Descargar estado de la tabla](download-table-state.md) <br/> |Elementos  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Descargar estado del encabezado del mensaje](download-message-header-state.md) <br/> |Encabezado del mensaje  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Diagrama de transición de estado

En el siguiente diagrama se muestran las transiciones de estado que se producen al cargar o realizar una sincronización completa (descarga seguida de carga) de carpetas o contenido de carpetas (correo, calendario, contacto, nota, tarea o elementos del diario). 
  
@ @ @ @ @NEED INSERTAR UNA IMAGEN AQUÍ QUE NO APARECE @ @ @ @ @ @
  
## <a name="example-uploading-a-folder-hierarchy"></a>Ejemplo: carga de una jerarquía de carpetas

 Al cargar una jerarquía de carpetas, se lleva a cabo la siguiente secuencia de pasos: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Paso** <br/> |**Action** <br/> |**State** <br/> |**Estructura de datos relacionada** <br/> |
|1.  <br/> |El cliente inicia la carga de la jerarquía con **IOSTX:: SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 o Outlook 2010 rellena **UPHIER** con información para el cliente. Esto incluye la inicialización de los parámetros [out]: *iEnt* se establece en 0 y en un *céntimo* en el número de carpetas de la jerarquía que se deben cargar.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |El cliente hace la carga de jerarquía real. Por ejemplo, si el *cEnt* es 10, para cada una de las 10 carpetas, el cliente llama a **IOSTX:: SyncBeg**, especificando el identificador de estado adecuado y la estructura de datos para cargar una carpeta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 o Outlook 2010 rellena **UPFLD** inicializando sus parámetros [out], incluido el motivo de la carga de la carpeta, el puntero al objeto Folder y el identificador de entrada de la carpeta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |El cliente carga la carpeta especificada.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |El cliente notifica al almacén local de la finalización de la carga de la carpeta: tras el éxito, el cliente establece el parámetro [in] *ulFlags* en **UPFLD** con **UPF_OK**y, a continuación, llama a **IOSTX:: SetSyncResult (S_OK)** y **IOSTX:: SyncEnd **. Cuando se produce un error, el cliente no estableció *ulFlags* con la marca **UPF_OK** . Llama a **IOSTX:: SetSyncResult**, pasando el valor **HRESULT** y **IOSTX:: SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Si se establece **UPF_OK** , Outlook 2013 o Outlook 2010 borrarán la solicitud interna para cargar la carpeta. A continuación, independientemente del estado de *ulFlags* , se limpiará toda la información de contabilidad interna. Aunque todavía hay carpetas en la jerarquía para cargar (*iEnt* es todavía inferior a *ciento*), el cliente y outlook 2013 o Outlook 2010 repiten los pasos 3 a 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |El cliente notifica al almacén local de la finalización de la carga de la jerarquía: tras el éxito, el cliente establece el indicador [in] en **UPHIER** con **UPH_OK**y, a continuación, llama a **IOSTX:: SetSyncResult (S_OK)** y **IOSTX:: SyncEnd**. Cuando se produce un error, el cliente no establece la marca **UPH_OK** . Llama a **IOSTX:: SetSyncResult**, pasando el valor **HRESULT** y **IOSTX:: SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Si se establece **UPH_OK** , Outlook 2013 o Outlook 2010 borrarán la solicitud interna para cargar la jerarquía. A continuación, independientemente del estado de *ulFlags* , se limpiará toda la información de contabilidad interna.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Ver también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)

