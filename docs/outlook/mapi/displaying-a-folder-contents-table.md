---
title: Mostrar una tabla de contenido de la carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412397"
---
# <a name="displaying-a-folder-contents-table"></a>Mostrar una tabla de contenido de la carpeta

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La tabla de contenido de una carpeta contiene información de resumen sobre todos sus mensajes. La información de resumen sobre los nuevos mensajes entrantes aparece en la tabla de contenido de la carpeta de recepción para la clase de mensaje. Para que esta información esté disponible para los usuarios, recupere la tabla y muestre las columnas y las filas según corresponda.
  
**Para mostrar una tabla de contenido de la carpeta**
  
1. Llame a [IMsgStore:: OpenEntry](imsgstore-openentry.md)y pase el identificador de entrada de la carpeta que contiene la tabla.
    
2. Llame al método [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la carpeta para abrir su tabla de contenido. 
    
3. Limite la vista de la tabla de contenido si lo desea, llamando al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la tabla para especificar determinadas columnas. 
    
4. Limite la vista de la tabla de contenido si lo desea, llamando al método [IMAPITable:: Restrict](imapitable-restrict.md) para filtrar determinadas filas. Si, por ejemplo, desea mostrar solo los mensajes con una clase de mensaje específica que todavía se ha leído: 
    
    1. Cree una restricción de propiedad en una estructura [SPropertyRestriction](spropertyrestriction.md) que coincida con la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) con la clase de mensaje deseada. 
        
    2. Cree una restricción de máscara de subred en una estructura [SBitMaskRestriction](sbitmaskrestriction.md) que use **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) como etiqueta de propiedad y el valor MSGFLAG_UNREAD como máscara.
        
    3. Cree una restricción en una estructura [SAndRestriction](sandrestriction.md) que combine las restricciones de propiedad y máscara de la máscara. 
    
5. Ordene la tabla de contenido si lo desea mediante una llamada al método [IMAPITable:: SortTable](imapitable-sorttable.md) de la tabla. 
    
6. Llame al [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas las filas de la tabla de contenido para su procesamiento. 
    

