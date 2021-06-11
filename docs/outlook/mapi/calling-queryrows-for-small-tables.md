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
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404179"
---
# <a name="calling-queryrows-for-small-tables"></a>Llamar a QueryRows para tablas pequeñas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al recuperar filas de una tabla pequeña, llama a [IMAPITable::QueryRows](imapitable-queryrows.md) en lugar de crear primero una restricción. Crear una restricción afecta al rendimiento porque el proveedor primero debe crear una tabla, buscar las filas coincidentes en la tabla original y, a continuación, copiar las filas en la nueva tabla. Si el número total de filas de la tabla es menor que 100, probablemente sea más eficaz leer todas las filas y, a continuación, llamar a [IMAPITable::FindRow](imapitable-findrow.md) para buscar la fila adecuada. Esta es una estrategia especialmente buena si esta información solo se necesita ocasionalmente. 
  
El tiempo adecuado para usar una restricción es cuando la información restringida o filtrada se usará durante un período de tiempo más largo o se usará con frecuencia. Por ejemplo, si siempre necesita una vista con mensajes no leídos, entonces una restricción es la llamada adecuada para usar.
  

