---
title: Descargar estado de la jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384860"
---
# <a name="download-hierarchy-state"></a>Descargar estado de la jerarquía

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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
  
Outlook inicializa la estructura de datos **DNHIER** asociada con un puntero a la jerarquía. El cliente de descargas de la jerarquía e inserta nuevas carpetas o modificaciones realizadas a las carpetas en el almacén local. El proceso de descarga adopta la sincronización de cambio Incremental (ICS) de Microsoft Exchange. Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Cuando finaliza este estado, el almacén local se devuelve en el estado de sincronización.
  
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

