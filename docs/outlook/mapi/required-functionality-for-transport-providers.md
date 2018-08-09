---
title: Funcionalidad necesaria para proveedores de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: eb5d70c31f28df16593fb020f13124ea217476ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820527"
---
# <a name="required-functionality-for-transport-providers"></a>Funcionalidad necesaria para proveedores de transporte

  
  
**Hace referencia a**: Outlook 
  
Cada proveedor de transporte MAPI debe:
  
- Siga las instrucciones generales para trabajar con MAPI y otros proveedores de servicios. Para obtener más información, vea [El desarrollo de aplicaciones MAPI](mapi-application-development.md) y [Proveedores de servicios de MAPI](mapi-service-providers.md).
    
- Tienen su función de inicialización [XPProviderInit](xpproviderinit.md) de su proveedor de transporte exponen DLL a MAPI. 
    
- Exponer a MAPI en su implementación de la [IXPProvider: IUnknown](ixpprovideriunknown.md) y [IXPLogon: IUnknown](ixplogoniunknown.md) interfaces. 
    
- Exponer las aplicaciones MAPI y cliente de su implementación de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz. Para obtener más información acerca de cómo implementar **IMAPIStatus**, vea [Implementación de objeto de estado](status-object-implementation.md). 
    
- Implementar un cuadro de diálogo de la hoja de propiedad para la configuración. Para obtener más información acerca de cómo implementar las hojas de propiedades, vea [Implementación de la hoja de propiedad](property-sheet-implementation.md).
    

