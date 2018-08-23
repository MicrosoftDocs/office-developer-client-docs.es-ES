---
title: Implementar la búsqueda avanzada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0ba9958588c476ae330b0f4a413361e80d54667a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571972"
---
# <a name="implementing-advanced-searching"></a>Implementar la búsqueda avanzada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos contenedores de la libreta de direcciones compatible con una capacidad de búsqueda avanzada que permite a los clientes buscar en las propiedades que no sean **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Para admitir búsquedas avanzadas, su proveedor debe implementar un contenedor especial que es accesible a través de la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de los otros contenedores. **PR_SEARCH** contiene un objeto de contenedor que proporciona acceso a una tabla para mostrar que describe el cuadro de diálogo se usa para escribir y editar los criterios de búsqueda avanzada. 
  
 **Para admitir la búsqueda avanzada**
  
1. Definir una propiedad para cada uno de los criterios de búsqueda.
    
2. En la sección de código en método del contenedor de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) que controla la propiedad **PR_SEARCH** : 
    
1. Compruebe que el cliente está solicitando la interfaz **IMAPIContainer** . Si se solicita una interfaz inapropiada, se producirá un error y devolver MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Crear un nuevo objeto de búsqueda que admite la interfaz **IMAPIContainer** . 
    
3. En este momento, se realiza una llamada al método de **IMAPIProp::OpenProperty** del contenedor de la búsqueda para recuperar su propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). El proveedor debe proporcionar una tabla para mostrar, normalmente a través de una llamada a [BuildDisplayTable](builddisplaytable.md), que se describe el cuadro de diálogo de búsqueda avanzada del contenedor.
    
4. MAPI muestra el cuadro de diálogo Buscar, lo que permite al usuario que escriba los criterios adecuados. Cuando el usuario ha terminado, MAPI llama al método [IMAPIProp::SetProps](imapiprop-setprops.md) del contenedor para almacenar los criterios de búsqueda. 
    
5. Se realizará una llamada para solicitar la tabla de contenido del contenedor de la búsqueda. Rellenar la tabla de contenido con todas las entradas en el contenedor que coinciden con los criterios.
    

