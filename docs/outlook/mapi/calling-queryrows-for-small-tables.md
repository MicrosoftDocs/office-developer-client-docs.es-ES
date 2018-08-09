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
ms.openlocfilehash: 40533470681182719f5009b048e3b173b92ef290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816498"
---
# <a name="calling-queryrows-for-small-tables"></a>Llamar a QueryRows para tablas pequeñas

  
  
**Hace referencia a**: Outlook 
  
Al recuperar filas de una tabla pequeña, llame a [IMAPITable:: QueryRows](imapitable-queryrows.md) en lugar de crear primero una restricción. Creación de una restricción afecta al rendimiento debido a que el proveedor debe crear primero una tabla, busque las filas coincidentes en la tabla original y, a continuación, copie las filas a la nueva tabla. Si el número total de filas de la tabla es menor que 100, es probablemente más eficaces leer todas las filas y, a continuación, llame al [elemento IMAPITable:: FindRow](imapitable-findrow.md) para buscar la fila apropiada. Ésta es una estrategia especialmente buena si esta información es necesaria sólo ocasionalmente. 
  
El momento apropiado para usar una restricción es cuando la información restringida o filtrada se utiliza durante un período de tiempo más largo o se usa con frecuencia. Por ejemplo, si necesita siempre una vista con mensajes no leídos, la llamada correcta a usar es una restricción.
  

