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
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404445"
---
# <a name="required-functionality-for-transport-providers"></a>Funcionalidad necesaria para proveedores de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Todos los proveedores de transporte MAPI deben:
  
- Siga las instrucciones generales para trabajar con MAPI y otros proveedores de servicios. Para obtener más información, vea [Mapi Application Development](mapi-application-development.md) and MAPI Service [Providers](mapi-service-providers.md).
    
- Haga que su DLL del proveedor de transporte exponga a MAPI [su función de inicialización XPProviderInit.](xpproviderinit.md) 
    
- Exponer a MAPI su implementación de [las interfaces IXPProvider : IUnknown](ixpprovideriunknown.md) e [IXPLogon : IUnknown.](ixplogoniunknown.md) 
    
- Exponer a MAPI y aplicaciones cliente su implementación de la [interfaz IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Para obtener más información acerca de la implementación de **IMAPIStatus,** vea [Status Object Implementation](status-object-implementation.md). 
    
- Implementar un cuadro de diálogo de hoja de propiedades para la configuración. Para obtener más información acerca de la implementación de hojas de propiedades, vea [Property Sheet Implementation](property-sheet-implementation.md).
    

