---
title: Agrupación y restricción de tablas en proveedores de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428987"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Agrupación y restricción de tablas en proveedores de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Con frecuencia, las aplicaciones cliente permiten a los usuarios tener cierto control sobre cómo se muestra el contenido de una carpeta. Normalmente, un usuario puede elegir que los mensajes se a agrupan según el valor de una o más propiedades de mensaje, o puede optar por excluir los mensajes que coinciden con ciertos criterios. Esto se realiza mediante la interfaz [IMAPITable : IUnknown.](imapitableiunknown.md) Las aplicaciones cliente pueden restringir las filas devueltas de la tabla a los criterios que especifique el usuario. Por lo tanto, un proveedor de almacenamiento de mensajes debe implementar los **siguientes métodos IMAPITable.** 
  
|Método IMAPITable**|**Descripción**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Devuelve filas de tabla que coinciden con los criterios especificados.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Devuelve el conjunto de columnas de una tabla o el conjunto de columnas usadas actualmente.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Devuelve una o más filas de una tabla, empezando desde una posición determinada.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Aplica una restricción a una tabla para que las llamadas posteriores a **FindRow** devuelvan solo las filas que coincidan con la restricción.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Especifica qué columnas se deben devolver cuando se recuperan filas de la tabla.  <br/> |
   
Las restricciones pueden ser complejas de implementar; para obtener más información, vea [Acerca de las restricciones](about-restrictions.md). Para obtener más información acerca de la implementación de tablas, vea [Tablas MAPI](mapi-tables.md).
  
## <a name="see-also"></a>Consulte también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

