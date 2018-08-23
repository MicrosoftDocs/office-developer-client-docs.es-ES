---
title: Descargar estado de la tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e75407f62a7e6440f6c8dca8c1d2c76843048da4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595401"
---
# <a name="download-table-state"></a>Descargar estado de la tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe qué ocurre durante el estado de la tabla de descarga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Estructura de datos relacionados:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|Desde este estado:  <br/> |[Sincronizar el estado del contenido](synchronize-contents-state.md) <br/> |
|En este estado:  <br/> |Sincronizar el estado del contenido  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia la descarga de una carpeta. Durante este estado, Outlook inicializa la estructura de datos **DNTBL** asociada con información acerca de la carpeta. El cliente descarga el contenido de la carpeta y actualiza la carpeta en el almacén local con contenido nuevo, modificaciones o eliminaciones desde el servidor. El proceso de descarga adopta la sincronización de cambio Incremental (ICS) de Microsoft Exchange. Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
Cuando finaliza este estado, se devuelve el almacén local en el estado del contenido de sincronizar.
  
## <a name="see-also"></a>Recursos adicionales



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

