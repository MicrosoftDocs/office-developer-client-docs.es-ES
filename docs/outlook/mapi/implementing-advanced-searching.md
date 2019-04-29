---
title: Implementación de búsquedas avanzadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407392"
---
# <a name="implementing-advanced-searching"></a>Implementación de búsquedas avanzadas

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos contenedores de libretas de direcciones admiten una capacidad de búsqueda avanzada que permite a los clientes buscar en propiedades distintas de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Para admitir búsquedas avanzadas, el proveedor debe implementar un contenedor especial al que se pueda tener acceso a través de la propiedad **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de los otros contenedores. **PR_SEARCH** contiene un objeto Container que proporciona acceso a una tabla de presentación que describe el cuadro de diálogo usado para escribir y editar los criterios de búsqueda avanzada. 
  
 **Para admitir la búsqueda avanzada**
  
1. Defina una propiedad para cada uno de los criterios de búsqueda.
    
2. En la sección de código del método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) del contenedor que controla la propiedad **PR_SEARCH** : 
    
1. Compruebe que el cliente está solicitando la interfaz **IMAPIContainer** . Si se solicita una interfaz inapropiada, se produce un error y se devuelve MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Cree un nuevo objeto Search que admita la interfaz **IMAPIContainer** . 
    
3. En este momento, se realizará una llamada al método **IMAPIProp:: OpenProperty** del contenedor de búsqueda para recuperar su propiedad **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). El proveedor debe proporcionar una tabla de presentación, normalmente a través de una llamada a [BuildDisplayTable](builddisplaytable.md), que describe el cuadro de diálogo búsqueda avanzada del contenedor.
    
4. MAPI muestra el cuadro de diálogo de búsqueda, lo que permite al usuario especificar los criterios adecuados. Cuando el usuario ha terminado, MAPI llama al método [IMAPIProp:: SetProps](imapiprop-setprops.md) del contenedor para almacenar los criterios de búsqueda. 
    
5. Se realizará una llamada para solicitar la tabla de contenido del contenedor de búsqueda. ReLlene la tabla Contents con todas las entradas del contenedor que coinciden con los criterios.
    

