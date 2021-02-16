---
title: Estado de sincronización
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414630"
---
# <a name="synchronize-state"></a>Estado de sincronización

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de sincronización de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC** <br/> |
|Estructura de datos relacionada:  <br/> |**[Sincronizar](sync.md)** <br/> |
|Desde este estado:  <br/> |[Estado inactivo](idle-state.md) <br/> |
|A este estado:  <br/> |[Descargar estado de jerarquía,](download-hierarchy-state.md) [estado de sincronización de contenido,](synchronize-contents-state.md)estado de carga de [jerarquía](upload-hierarchy-state.md)o estado inactivo  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que va de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Description

Este estado inicia la sincronización. Una tienda local puede pasar a un estado de carga o descarga desde aquí. Por ejemplo, un almacén local puede moverse al estado de la jerarquía de carga para cargar una jerarquía de carpetas en el servidor, o bien puede realizar una sincronización completa cargando primero la jerarquía y, a continuación, descargando la jerarquía desde el servidor.
  
Durante este estado, Outlook inicializa la estructura de datos **sync** asociada con la ruta de acceso al almacén local, para que Outlook vea modificaciones en otros estados. 
  
El cliente establece los miembros [entrada] de **SYNC**, que indica a Outlook cómo controlar otros estados. Por ejemplo, el cliente puede establecer  *ulFlags*  en **UPS_UPLOAD_ONLY** y **UPS_THESE_FOLDERS** y  *pel*  en una lista de identificadores de entrada de las carpetas para decir a Outlook que solo se cargarán estas carpetas. Cuando finaliza este estado, el almacén local vuelve al estado inactivo. 
  
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

