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
ms.openlocfilehash: f206623103f810b2868502aea7c6804cd306f022
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573197"
---
# <a name="supporting-searches-in-message-store-providers"></a>Admitir búsquedas en proveedores de almacenamiento de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Con frecuencia, las aplicaciones cliente presentan algunos componentes de la interfaz de usuario dedicados a la búsqueda de mensajes en un almacén de mensajes. Criterios de búsqueda se especifican en el [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) interfaz por medio de los métodos [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) y [IMAPIContainer::GetSearchCriteria](imapicontainer-getsearchcriteria.md) . 
  
Los clientes utilizan la propiedad de **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) del objeto de almacén de mensajes para identificar la carpeta raíz en el almacén de mensajes que contiene carpetas para los resultados de búsqueda. La carpeta de resultados de búsqueda a menudo es una carpeta en el nivel superior del almacén de mensajes que no forma parte del árbol de carpetas IPM y, por lo tanto, oculto.
  
Si su proveedor de almacén de mensajes utiliza una carpeta de resultados de búsqueda permanente o crea uno cuando un cliente abre el identificador de entrada que se almacenan en la propiedad **PR_FINDER_ENTRYID** es un detalle de implementación. Es algo más fácil de su proveedor de almacén de mensajes para usar una carpeta permanente que se crea cuando se crea el almacén de mensajes, ya que si lo hace por lo que evita la complejidad de comprobar el identificador de entrada siempre que se abre cualquier carpeta para ver si va a crear un carpeta de resultados de búsqueda. Sin embargo, no todos los proveedores de almacén de mensajes pueden hacer; en particular, almacenes de mensaje de sólo lectura o que proporcionan una interfaz de MAPI para una base de datos heredado a menudo no se permiten o no puede crear una carpeta de resultados de búsqueda permanente en el mecanismo de almacenamiento subyacente. 
  
## <a name="see-also"></a>Recursos adicionales



[Caracter�sticas de almac�n de mensajes](message-store-features.md)

