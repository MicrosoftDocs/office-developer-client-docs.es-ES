---
title: Admitir búsquedas en proveedores de almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30a3fe28-31ca-4eb8-9353-f75f6d339dc7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 545047e90346b0f8e4a88eabcb20573f663f6d02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425389"
---
# <a name="supporting-searches-in-message-store-providers"></a>Admitir búsquedas en proveedores de almacén de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente suelen tener algunos componentes de interfaz de usuario dedicados a buscar mensajes en un almacén de mensajes. Los criterios de búsqueda se especifican en la interfaz [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md) mediante los métodos [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) e [IMAPIContainer::GetSearchCriteria.](imapicontainer-getsearchcriteria.md) 
  
Los clientes usan la propiedad PR_FINDER_ENTRYID **del** objeto de almacén de mensajes ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) para identificar la carpeta raíz del almacén de mensajes que contiene carpetas para los resultados de búsqueda. La carpeta de resultados de búsqueda suele ser una carpeta en el nivel superior del almacén de mensajes que no forma parte del árbol de carpetas IPM y, por lo tanto, está oculta.
  
Si el proveedor del almacén de mensajes usa una carpeta de resultados de búsqueda permanente o crea una cuando un cliente abre el identificador de entrada almacenado en la **propiedad PR_FINDER_ENTRYID** es un detalle de implementación. Es algo más fácil para el proveedor del almacén de mensajes usar una carpeta permanente que se crea cuando se crea el almacén de mensajes, ya que hacerlo evita la complicación de comprobar el identificador de entrada siempre que se abra cualquier carpeta para ver si se va a crear una carpeta de resultados de búsqueda. Sin embargo, no todos los proveedores de almacén de mensajes pueden hacerlo; En particular, los almacenes o almacenes de mensajes de solo lectura que proporcionan una interfaz MAPI a una base de datos heredada a menudo no están permitidos o no pueden crear una carpeta de resultados de búsqueda permanente en el mecanismo de almacenamiento subyacente. 
  
## <a name="see-also"></a>Vea también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

