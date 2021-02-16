---
title: Descargar estado de jerarquía
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337012"
---
# <a name="download-hierarchy-state"></a>Descargar estado de jerarquía

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 En este tema se describe lo que sucede durante el estado de la jerarquía de descarga de la máquina de estado de replicación. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador de estado:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Estructura de datos relacionados:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Desde este estado:  <br/> |[Estado de sincronización](synchronize-state.md) <br/> |
|A este estado:  <br/> |Estado de sincronización  <br/> |
   
> [!NOTE]
> La máquina de estado de replicación es una máquina de estado determinista. Un cliente que va de un estado a otro debe volver al primero desde el segundo. 
  
## <a name="description"></a>Description

Este estado inicia la descarga de una jerarquía de árbol de carpetas de un servidor al almacén local. 
  
Outlook inicializa la estructura de **datos DNHIER** asociada con un puntero a la jerarquía. El cliente descarga la jerarquía e inserta nuevas carpetas o modificaciones en las carpetas del almacén local. El proceso de descarga adopta la sincronización de cambios incrementales (ICS) de Microsoft Exchange. Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Cuando finaliza este estado, el almacén local vuelve al estado de sincronización.
  
## <a name="see-also"></a>Consulte también



[Información sobre la API de replicación](about-the-replication-api.md)
  
[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

