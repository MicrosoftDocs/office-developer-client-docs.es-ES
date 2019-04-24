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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337096"
---
# <a name="displaying-the-common-address-dialog-box"></a>Mostrar el cuadro de diálogo Dirección común

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El cuadro de diálogo Dirección común de MAPI se puede usar para varias tareas de direccionamiento, como la creación de una lista de destinatarios. Para mostrar este cuadro de diálogo, llame a **IAddrBook:: Address**. Según el número de parámetros que establezca y el modo en que los establezca, puede limitar la visualización a las entradas de un tipo determinado desde un determinado contenedor.
  
 **Para limitar el cuadro de diálogo de la dirección a mostrar solo las entradas de la libreta personal de direcciones (PAB)**
  
1. Llame a [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la PAB. 
    
2. Cree una restricción de propiedad que use RELOP_EQ para el miembro **RELOP** de la estructura [SPropertyRestriction](spropertyrestriction.md) y **** bien el elemento ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como el miembro **ulPropTag** . Si usa el **** valor, pase el identificador de entrada recuperado de **GetPAB**. Si usa **PR_AB_PROVIDER_ID**, pase el valor incluido en MSPAB. H archivo de encabezado. **PR_AB_PROVIDER_ID** es el identificador único de la PAB diseñado por MAPI. 
    
3. Llamar a [IAddrBook:: Address](iaddrbook-address.md) con el parámetro _lpHierRestriction_ que apunte a la restricción de propiedad. 
    

