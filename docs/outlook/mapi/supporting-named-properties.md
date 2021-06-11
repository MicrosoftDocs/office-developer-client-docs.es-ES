---
title: Compatibilidad con propiedades con nombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434329"
---
# <a name="supporting-named-properties"></a>Compatibilidad con propiedades con nombre

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Se requiere compatibilidad con propiedades con nombre para: 
  
- Proveedores de libreta de direcciones que permiten copiar entradas de otros proveedores en sus contenedores.
    
- Proveedores de almacén de mensajes que se pueden usar para crear tipos de mensajes arbitrarios.
    
La compatibilidad con propiedades con nombre es opcional para todos los demás proveedores de servicios. Los proveedores de servicios que admiten propiedades con nombre deben implementar la asignación de nombre a identificador en los [métodos IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Los clientes llaman a **GetNamesFromIDs** para recuperar los nombres correspondientes de uno o varios identificadores de propiedad en el intervalo de más de 0x8000 y **GetIDsFromNames** para crear o recuperar los identificadores de uno o varios nombres. 
  
Los proveedores de servicios que no admiten propiedades con nombre deben:
  
- No se pueden llamar a [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer propiedades con identificadores de 0x8000 o superiores al devolver MAPI_E_UNEXPECTED_ID la matriz [SPropProblem.](spropproblem.md) 
    
- Devuelve MAPI_E_NO_SUPPORT de los [métodos IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
    

