---
title: Admitir búsquedas en proveedores de almacenamiento de mensajes
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
# <a name="supporting-searches-in-message-store-providers"></a>Admitir búsquedas en proveedores de almacenamiento de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente con frecuencia tienen algunos componentes de la interfaz de usuario dedicados a la búsqueda de mensajes en un almacén de mensajes. Los criterios de búsqueda se especifican en la interfaz [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) por medio de los métodos [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) y [IMAPIContainer:: GetSearchCriteria](imapicontainer-getsearchcriteria.md) . 
  
Los clientes usan la propiedad **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) del objeto de almacén de mensajes para identificar la carpeta raíz del almacén de mensajes que contiene carpetas para los resultados de la búsqueda. La carpeta de resultados de búsqueda suele ser una carpeta en el nivel superior del almacén de mensajes que no forma parte del árbol de carpetas IPM y que, por lo tanto, está oculta.
  
Si su proveedor de almacenamiento de mensajes utiliza una carpeta de resultados de búsqueda permanente o crea una cuando un cliente abre el identificador de entrada almacenado en la propiedad **PR_FINDER_ENTRYID** es un detalle de implementación. Es algo más sencillo para su proveedor de almacenamiento de mensajes usar una carpeta permanente que se crea cuando se crea el almacén de mensajes, porque al hacerlo se evita la complicación de comprobar el identificador de entrada siempre que se abra cualquier carpeta para ver si se crea una carpeta de resultados de búsqueda. Sin embargo, no todos los proveedores de almacenamiento de mensajes pueden hacerlo; en concreto, los almacenes de mensajes de solo lectura o los almacenes que proporcionan una interfaz MAPI a una base de datos heredada a menudo no se permiten o no pueden crear una carpeta de resultados de búsqueda permanente en el mecanismo de almacenamiento subyacente. 
  
## <a name="see-also"></a>Ver también



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

