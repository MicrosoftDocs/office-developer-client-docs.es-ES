---
title: Llamar a QueryRows para tablas pequeñas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589339"
---
# <a name="calling-queryrows-for-small-tables"></a>Llamar a QueryRows para tablas pequeñas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al recuperar filas de una tabla pequeña, llame a [IMAPITable:: QueryRows](imapitable-queryrows.md) en lugar de crear primero una restricción. Creación de una restricción afecta al rendimiento debido a que el proveedor debe crear primero una tabla, busque las filas coincidentes en la tabla original y, a continuación, copie las filas a la nueva tabla. Si el número total de filas de la tabla es menor que 100, es probablemente más eficaces leer todas las filas y, a continuación, llame al [elemento IMAPITable:: FindRow](imapitable-findrow.md) para buscar la fila apropiada. Ésta es una estrategia especialmente buena si esta información es necesaria sólo ocasionalmente. 
  
El momento apropiado para usar una restricción es cuando la información restringida o filtrada se utiliza durante un período de tiempo más largo o se usa con frecuencia. Por ejemplo, si necesita siempre una vista con mensajes no leídos, la llamada correcta a usar es una restricción.
  

