---
title: Descargar estado de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338342"
---
# <a name="download-table-state"></a>Descargar estado de tabla

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de la tabla de descarga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Estructura de datos relacionada:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|Desde este estado:  <br/> |[Sincronizar el estado de contenido](synchronize-contents-state.md) <br/> |
|A este estado:  <br/> |Sincronizar el estado de contenido  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que sale de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Descripción

Este estado inicia la descarga de una carpeta. Durante este estado, Outlook inicializa la estructura de datos **de DNTBL** asociada con información sobre la carpeta. El cliente descarga el contenido de la carpeta y actualiza la carpeta en el almacén local con nuevos contenidos, modificaciones o eliminaciones del servidor. El proceso de descarga adopta Microsoft Exchange sincronización incremental de cambios (ICS). Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Cuando finaliza este estado, el almacén local vuelve al estado de sincronización de contenido.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

