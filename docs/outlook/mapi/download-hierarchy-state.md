---
title: Descargar estado de la jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e31a2a9c45a8896efbc43eb7f4b22f31f51e4013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816708"
---
# <a name="download-hierarchy-state"></a>Descargar estado de la jerarquía

  
  
**Hace referencia a**: Outlook 
  
 En este tema se describe qué ocurre durante el estado de la jerarquía de descarga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Estructura de datos relacionados:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Desde este estado:  <br/> |[Sincronizar estado](synchronize-state.md) <br/> |
|En este estado:  <br/> |Sincronizar estado  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente sale de un estado a otro finalmente debe volver a la primera desde el último. 
  
## <a name="description"></a>Descripción

Este estado inicia la descarga de una jerarquía de árbol de carpetas de un servidor en el almacén local. 
  
Outlook inicializa la estructura de datos **DNHIER** asociada con un puntero a la jerarquía. El cliente de descargas de la jerarquía e inserta nuevas carpetas o modificaciones realizadas a las carpetas en el almacén local. El proceso de descarga adopta la sincronización de cambio Incremental (ICS) de Microsoft Exchange. Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
Cuando finaliza este estado, el almacén local se devuelve en el estado de sincronización.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZACIÓN](syncstate.md)

