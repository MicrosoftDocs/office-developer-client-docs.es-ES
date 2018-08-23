---
title: Mostrar una tabla de contenido de carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51c88e8c062a409db305e893b82f43d8c8ac7094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580799"
---
# <a name="displaying-a-folder-contents-table"></a>Mostrar una tabla de contenido de carpeta

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En la tabla de contenido de una carpeta contiene información de resumen sobre todos sus mensajes. Información de resumen acerca de los mensajes entrantes nuevo aparece en la tabla de contenido de la carpeta de recepción para la clase de mensaje. Para que esta información esté disponible para los usuarios, recuperar la tabla y mostrar las columnas y filas según corresponda.
  
**Para mostrar una tabla de contenido de carpeta**
  
1. Llame a [IMsgStore::OpenEntry](imsgstore-openentry.md), pasando el identificador de entrada de la carpeta que contiene la tabla.
    
2. Llamar al método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para abrir su tabla de contenido. 
    
3. Limitar la vista de la tabla de contenido si así lo desea mediante una llamada al método [IMAPITable::SetColumns](imapitable-setcolumns.md) de la tabla para especificar columnas en particular. 
    
4. Limitar la vista de la tabla de contenido si así lo desea mediante una llamada al método [IMAPITable:: Restrict](imapitable-restrict.md) de la tabla para filtrar filas determinadas. Si, por ejemplo, que desea mostrar sólo los mensajes con una clase de mensaje específica que tienen aún se leerá: 
    
    1. Crear una restricción de propiedad en una estructura [SPropertyRestriction](spropertyrestriction.md) que coincida con la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) con la clase de mensaje que desee. 
        
    2. Crear una restricción de máscara de bits en una estructura [SBitMaskRestriction](sbitmaskrestriction.md) que usa **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como la etiqueta de propiedad y el valor MSGFLAG_UNREAD como la máscara.
        
    3. Crear una restricción de una estructura de [SAndRestriction](sandrestriction.md) que se une a las restricciones de propiedad y la máscara de bits. 
    
5. Ordenar la tabla de contenido si así lo desea mediante una llamada al método de [SortTable](imapitable-sorttable.md) de la tabla. 
    
6. Llamar a [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla de contenido para su procesamiento. 
    

