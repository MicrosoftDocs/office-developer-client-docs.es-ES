---
title: Agrupar y restringir tablas en proveedores de almacenamiento de mensajes
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
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a>Agrupar y restringir tablas en proveedores de almacenamiento de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Con frecuencia, las aplicaciones cliente permiten a los usuarios controlar el modo en que se muestran los contenidos de una carpeta. Normalmente, un usuario puede elegir que los mensajes se agrupen de acuerdo con el valor de una o más propiedades del mensaje, o puede optar por excluir los mensajes que cumplan determinados criterios. Esto se realiza mediante la interfaz [IMAPITable: IUnknown](imapitableiunknown.md) . Las aplicaciones cliente pueden restringir las filas devueltas de la tabla a los criterios especificados por el usuario. Por lo tanto, un proveedor de almacén de mensajes debe implementar los siguientes métodos **IMAPITable** . 
  
|Método IMAPITable * * * *|**Descripción**|
|:-----|:-----|
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |Devuelve las filas de la tabla que coinciden con los criterios especificados.  <br/> |
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |Devuelve el conjunto de columnas de una tabla o el conjunto de columnas que se usan actualmente.  <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> |Devuelve una o más filas de una tabla, comenzando por una posición determinada.  <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |Aplica una restricción a una tabla para que las llamadas posteriores a **FindRow** devuelvan solo las filas que coinciden con la restricción.  <br/> |
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |Especifica qué columnas se deben devolver cuando se recuperan filas de la tabla.  <br/> |
   
Las restricciones pueden ser complejas de implementar; para obtener más información, consulte [acerca de las restricciones](about-restrictions.md). Para obtener más información acerca de la implementación de tablas, consulte [MAPI tables](mapi-tables.md).
  
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

