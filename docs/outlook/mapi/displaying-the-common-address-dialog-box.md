---
title: Mostrar el cuadro de diálogo Dirección común
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436907"
---
# <a name="displaying-the-common-address-dialog-box"></a>Mostrar el cuadro de diálogo Dirección común

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El cuadro de diálogo de direcciones comunes MAPI se puede usar para diversas tareas de direccionamiento, como la construcción de una lista de destinatarios. Para mostrar este cuadro de diálogo, llame a **IAddrBook::Address**. Dependiendo de cuáles de los parámetros se establezcan y cómo se establezcan, puede limitar la presentación a las entradas de un tipo determinado de un contenedor determinado.
  
 **Para limitar el cuadro de diálogo de dirección a mostrar solo las entradas de la libreta de direcciones personal (PAB)**
  
1. Llame [a IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada del PAB. 
    
2. Cree una restricción de propiedad que use RELOP_EQ para el miembro **retablo** de la estructura [SPropertyRestriction](spropertyrestriction.md) y **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como el **miembro ulPropTag.** Si usa **PR_ENTRYID**, pase el identificador de entrada recuperado de **GetPAB**. Si usa **PR_AB_PROVIDER_ID**, pase el valor incluido en la MSPAB. Archivo de encabezado H. **PR_AB_PROVIDER_ID** es el identificador único del PAB diseñado por MAPI. 
    
3. Llame [a IAddrBook::Address](iaddrbook-address.md) con el parámetro  _lpHierRestriction_ que señale a la restricción de propiedad. 
    

