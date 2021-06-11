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
  
Este tema contiene información general sobre el equipo de estado para la Microsoft Outlook 2013 y Microsoft Outlook 2010 de datos.
  
> [!NOTE]
> La API de replicación debe implementarse completamente de acuerdo con las instrucciones de este tema para que sea útil o compatible. La API de replicación está disponible exclusivamente para replicar Outlook 2013 o Outlook 2010 cambios en y desde un servidor. 
  
## <a name="iostx-and-the-state-machine"></a>IOSTX y la máquina de estado

Un cliente llama a **[IOSTX::SyncBeg](iostx-syncbeg.md)**, **[IOSTX::SyncEnd](iostx-syncend.md)**, **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** y **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** en una secuencia para sincronizar carpetas y elementos de Outlook 2013 o Outlook 2010 entre un almacén local y un servidor. La secuencia real de llamadas depende de los datos que deben replicarse (por ejemplo, una jerarquía de carpetas de Outlook 2013 o Outlook 2010, una carpeta de Outlook 2013 o Outlook 2010, elementos de correo, elementos de calendario, entre otros) y la dirección de sincronización (ya sea la carga desde el almacén local al servidor o la descarga desde el servidor al almacén local). Esta es una secuencia típica de llamadas: 
  
1. El cliente llama **a IOSTX::SyncBeg** para iniciar la replicación, especificando un identificador de estado y un puntero a una dirección de una estructura de datos correspondiente. 
    
2. Outlook 2013 o Outlook 2010 asigna la estructura de datos e inicializa la estructura de datos con la información necesaria para el cliente. 
    
3. El cliente realiza la replicación, actualizando la estructura de datos para transmitir al almacén local toda la información necesaria sobre la replicación.
    
4. Después de realizar la replicación, el cliente llama a **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** y **IOSTX::SyncEnd** para notificar al almacén local la finalización de la replicación específica. 
    
> [!NOTE]
> El cliente siempre llama **a IOSTX::SyncEnd para** finalizar una replicación que el cliente ha comenzado para un estado determinado. Según los datos generales que el cliente necesita sincronizar, el cliente puede llamar al par de llamadas **IOSTX::SyncBeg** y **IOSTX::SyncEnd** más de una vez. 
  
## <a name="state-table"></a>Tabla de estado

> [!NOTE]
> En la tabla siguiente se enumeran todos los estados válidos de la máquina de estado de replicación, junto con los identificadores de estado y las estructuras de datos correspondientes. En la **columna Datos replicados,** el término "elementos" incluye elementos de correo, calendario, contacto, nota, diario y tarea. Al replicar los cambios del almacén local al servidor, use identificadores de estado que especifiquen "UPLOAD" y estructuras de datos con el prefijo "UP" (por ejemplo, **LR_SYNC_UPLOAD_HIERARCHY** **[y UPHIER](uphier.md)** ). Al replicar los cambios del servidor al almacén local, use identificadores de estado que especifiquen "DOWNLOAD" y estructuras de datos con el prefijo "DN" (por ejemplo, **LR_SYNC_DOWNLOAD_HIERARCHY** y **[DNHIER](dnhier.md)** ). 
  
|||||
|:-----|:-----|:-----|:-----|
|**Estado** <br/> |**Datos replicados** <br/> |**Identificador de estado** <br/> |**Estructura de datos** <br/> |
|[Estado inactivo](idle-state.md) <br/> | *Ninguna*  <br/> |**LR_SYNC_IDLE** <br/> | *Ninguna*  <br/> |
|[Estado de sincronización](synchronize-state.md) <br/> |Carpetas o elementos  <br/> |**LR_SYNC** <br/> |**[Sincronizar](sync.md)** <br/> |
|[Upload jerarquía](upload-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**[UPHIER](uphier.md)** <br/> |
|[Upload de carpeta](upload-folder-state.md) <br/> |Carpeta  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**[UPFLD](upfld.md)** <br/> |
|[Sincronizar el estado de contenido](synchronize-contents-state.md) <br/> |Elementos  <br/> |**LR_SYNC_CONTENTS** <br/> |**[SYNCCONT](synccont.md)** <br/> |
|[Upload de tabla](upload-table-state.md) <br/> |Elementos  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |**[UPTBL](uptbl.md)** <br/> |
|[Upload de mensaje](upload-message-state.md) <br/> |Item  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |**[UPMSG](upmsg.md)** <br/> |
|[Upload estado de lectura](upload-read-status-state.md) <br/> |Elementos  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |**[UPREAD](upread.md)** <br/> |
|[Upload estado de eliminación](upload-delete-status-state.md) <br/> |Elementos  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |**[UPDEL](updel.md)** <br/> |
|[Estado de jerarquía de descarga](download-hierarchy-state.md) <br/> |Folders  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |**[DNHIER](dnhier.md)** <br/> |
|[Estado de la tabla de descarga](download-table-state.md) <br/> |Elementos  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |**[DNTBL](dntbl.md)** <br/> |
|[Descargar estado de encabezado del mensaje](download-message-header-state.md) <br/> |Encabezado del mensaje  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
   
## <a name="state-transition-diagram"></a>Diagrama de transición de estado

El diagrama siguiente muestra las transiciones de estado que se producen al cargar o realizar una sincronización completa (descarga seguida de carga) de carpetas o contenido de carpetas (correo, calendario, contacto, nota, tarea o elementos de diario). 
  
@@@@@NEED INSERTAR ARTE AQUÍ QUE FALTA @@@@@@
  
## <a name="example-uploading-a-folder-hierarchy"></a>Ejemplo: Cargar una jerarquía de carpetas

 Al cargar una jerarquía de carpetas, se lleva a cabo la siguiente secuencia de pasos: 
  
|||||
|:-----|:-----|:-----|:-----|
|**Paso** <br/> |**Action** <br/> |**Estado** <br/> |**Estructura de datos relacionada** <br/> |
|1.  <br/> |El cliente inicia la carga de jerarquía **con IOSTX::SyncBeg**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|2.  <br/> |Outlook 2013 o Outlook 2010 rellena **UPHIER** con información para el cliente. Esto incluye inicializar los parámetros [out]:  *iEnt*  se establece en 0 y  *cEnt*  en el número de carpetas de la jerarquía que necesita cargarse.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|3.  <br/> |El cliente realiza la carga de jerarquía real. Por ejemplo, si  *cEnt*  es 10, para cada una de las 10 carpetas, el cliente llama a **IOSTX::SyncBeg,** especificando el identificador de estado y la estructura de datos adecuados para cargar una carpeta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|4.  <br/> |Outlook 2013 o Outlook 2010 rellena **UPFLD** inicializando sus parámetros [out], incluido el motivo de la carga de la carpeta, el puntero al objeto de carpeta y el identificador de entrada de la carpeta.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|5.  <br/> |El cliente carga la carpeta especificada.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|6.  <br/> |El cliente notifica al almacén local la finalización de la carga de carpetas: cuando se realiza correctamente, el cliente establece el parámetro  *[in] ulFlags*  en **UPFLD** con UPF_OK y, a continuación, llama **a** **IOSTX::SetSyncResult (S_OK)** y **IOSTX::SyncEnd**. Tras el error, el cliente no establecería  *ulFlags*  con la **UPF_OK** marca. Llama a **IOSTX::SetSyncResult**, pasando el valor **HRESULT** y **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|7.  <br/> |Si **UPF_OK,** Outlook 2013 o Outlook 2010 borrará la solicitud interna para cargar la carpeta. A continuación, independientemente del estado  *de ulFlags,*  limpiará cualquier información de contabilidad interna. Aunque todavía hay carpetas en la jerarquía que cargar (*iEnt* sigue siendo menor que *cEnt*), el cliente y Outlook 2013 o Outlook 2010 repiten los pasos del 3 al 7.  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |**UPFLD** <br/> |
|8.  <br/> |El cliente notifica al almacén local la finalización de la carga de la jerarquía: cuando se realiza correctamente, el cliente establece la marca [en] en **UPHIER** con UPH_OK y, a continuación, llama **a** **IOSTX::SetSyncResult (S_OK)** y **IOSTX::SyncEnd**. Tras el error, el cliente no establecería la **UPH_OK** marca. Llama a **IOSTX::SetSyncResult**, pasando el valor **HRESULT** y **IOSTX::SyncEnd**.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
|9.  <br/> |Si **UPH_OK,** Outlook 2013 o Outlook 2010 borrará la solicitud interna para cargar la jerarquía. A continuación, independientemente del estado  *de ulFlags,*  limpiará cualquier información de contabilidad interna.  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |**UPHIER** <br/> |
   
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[SYNCSTATE](syncstate.md)

