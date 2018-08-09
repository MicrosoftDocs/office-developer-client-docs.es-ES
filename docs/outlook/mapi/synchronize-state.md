---
title: Estado de sincronización
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820829"
---
# <a name="synchronize-state"></a>Estado de sincronización

  
  
**Hace referencia a**: Outlook 
  
 En este tema se describe qué ocurre durante el estado de sincronización de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC** <br/> |
|Estructura de datos relacionados:  <br/> |**[SYNC](sync.md)** <br/> |
|Desde este estado:  <br/> |[Estado de inactividad](idle-state.md) <br/> |
|En este estado:  <br/> |[Estado de la jerarquía de descarga](download-hierarchy-state.md), [sincronizar el estado del contenido](synchronize-contents-state.md), [cargar el estado de la jerarquía](upload-hierarchy-state.md)o estado inactivo  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia la sincronización. Puede realizar la transición de un almacén local a una carga o un estado de la descarga desde aquí. Por ejemplo, puede mover un almacén local en el estado de la jerarquía de cargar para cargar una jerarquía de carpetas en el servidor, o puede realizar una sincronización completa por primera carga la jerarquía y, a continuación, descarga la jerarquía desde el servidor.
  
Durante este estado, Outlook inicializa la estructura de datos de **sincronización** asociada con la ruta de acceso en el almacén local, por lo que Outlook ve modificaciones durante otros Estados. 
  
El cliente establece el [in] los miembros de **sincronización**, que indica cómo controlar otros Estados de Outlook. Por ejemplo, el cliente puede establecer *ulFlags* en **UPS_UPLOAD_ONLY** y **UPS_THESE_FOLDERS** y se cargará *pel* a una lista de identificadores de entrada de las carpetas para indicar a Outlook que sólo estas carpetas. Cuando finaliza este estado, el almacén local vuelve al estado inactivo. 
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

