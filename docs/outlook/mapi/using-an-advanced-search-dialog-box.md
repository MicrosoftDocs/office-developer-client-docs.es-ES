---
title: Uso de un cuadro de diálogo de búsqueda avanzada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437304"
---
# <a name="using-an-advanced-search-dialog-box"></a>Uso de un cuadro de diálogo de búsqueda avanzada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Algunos contenedores de libreta de direcciones admiten una capacidad de búsqueda avanzada que permite a los clientes buscar en propiedades que **no PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Los contenedores de libreta de direcciones que admiten búsquedas avanzadas tienen una propiedad de objeto de contenedor **denominada PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Este objeto contenedor proporciona acceso a una tabla para mostrar que describe el cuadro de diálogo de búsqueda, un cuadro de diálogo que se usa para escribir y editar los criterios de búsqueda avanzada.
  
 **Para realizar una búsqueda avanzada en un contenedor de libreta de direcciones**
  
1. Llame al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) del  contenedor, especificando PR_SEARCH para la etiqueta de propiedad y IID_IMAPIContainer para el identificador de interfaz. 
    
2. Llame al objeto de búsqueda 's **IMAPIProp::OpenProperty** método, **especificando PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) para la etiqueta de propiedad y IID_IMAPITable para el identificador de interfaz. 
    
3. Llame al método [IMAPIProp::SetProps](imapiprop-setprops.md) del objeto de búsqueda para establecer valores para las propiedades que se usarán en la búsqueda avanzada. 
    
4. Llame al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del objeto de búsqueda para guardar los criterios de búsqueda avanzada. 
    
Esta secuencia de llamadas da como resultado una restricción que está disponible cuando un cliente llama al método **GetSearchCriteria del objeto** de búsqueda. 
  

