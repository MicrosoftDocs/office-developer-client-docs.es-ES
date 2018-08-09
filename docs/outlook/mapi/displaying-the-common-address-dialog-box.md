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
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816715"
---
# <a name="displaying-the-common-address-dialog-box"></a>Mostrar el cuadro de diálogo Dirección común

  
  
**Hace referencia a**: Outlook 
  
El cuadro de diálogo dirección común de MAPI puede usarse para una variedad de hacer frente a tareas como la construcción de una lista de destinatarios. Para mostrar este cuadro de diálogo, llame a **IAddrBook::Address**. Dependiendo de cuál de los muchos parámetros que defina y cómo establecer, puede limitar la presentación a las entradas de un tipo determinado de un contenedor determinado.
  
 **Para limitar el cuadro de diálogo dirección para mostrar sólo las entradas de (PAB) de la libreta de direcciones personales**
  
1. Llame a [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la Libreta personal de direcciones. 
    
2. Crear una restricción de propiedad que usa RELOP_EQ para el miembro **relop** de la estructura de [SPropertyRestriction](spropertyrestriction.md) y **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como el miembro de **ulPropTag** . Si utiliza la **entrada del objeto**, pase el identificador de entrada recuperado de **GetPAB**. Si usa **PR_AB_PROVIDER_ID**, pase el valor incluido en el MSPAB. Archivo de encabezado H. **PR_AB_PROVIDER_ID** es el identificador único para el archivo PAB diseñado por MAPI. 
    
3. Llame al método [IAddrBook::Address](iaddrbook-address.md) con el parámetro _lpHierRestriction_ que señala a la restricción de propiedad. 
    

