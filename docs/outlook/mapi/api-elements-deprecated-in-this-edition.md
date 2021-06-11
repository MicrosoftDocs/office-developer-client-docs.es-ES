---
title: Elementos de API en desuso en esta edición
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436891"
---
# <a name="api-elements-deprecated-in-this-edition"></a>Elementos de API en desuso en esta edición

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los siguientes elementos api están en desuso en Microsoft Outlook 2013. Ya no se admiten y no se deben usar en nuevos proyectos.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Desuso de opciones de mensaje y destinatario

Los siguientes elementos de api están en desuso en esta versión debido a las opciones obsoletas de mensaje y destinatario:
  
- **IXPLogon::RegisterOptions:** el subsistema MAPI ya no llama a este método para establecer valores predeterminados para las opciones de mensaje y destinatario para un proveedor de transporte.
    
- **OPTIONDATA:** esta estructura de datos que admite propiedades para opciones de mensaje y destinatario está obsoleta. El subsistema MAPI ya no llama a **IXPLogon::RegisterOptions** para obtener cualquier opción de mensaje o destinatario que un proveedor de transporte admita para un tipo de dirección determinado. 
    
- **OPTIONCALLBACK**: este prototipo de función, que un proveedor de transporte usó para declarar una función de devolución de llamada y que, a su vez, el subsistema MAPI usado para resolver las propiedades del proveedor, está obsoleto. El subsistema MAPI ya no llama a **IXPLogon::RegisterOptions** ni usa ninguna función de devolución de llamada devuelta por el proveedor de transporte. 
    
- **IMAPISession::MessageOptions**: los proveedores de cliente y de servicio MAPI ya no deben llamar a este método para mostrar propiedades o permitir que los usuarios establezcan propiedades que controlan un tipo de mensaje y dirección determinados. El método siempre devuelve MAPI_E_NOT_FOUND, lo que indica que no hay opciones de mensaje para el mensaje en particular.
    
- **IMAPISession::QueryDefaultMessageOpt**: los proveedores de cliente y de servicio MAPI ya no deben llamar a este método para recuperar propiedades que controlan las opciones de mensaje para un tipo de dirección determinado. El método ya no devuelve un puntero a ninguna matriz de valores de propiedad.
    
- **IAddrBook::RecipOptions**: los proveedores de cliente y servicio MAPI ya no deben llamar a este método para mostrar propiedades o permitir que los usuarios establezcan propiedades que controlen el procesamiento de un destinatario de un tipo de dirección determinado. El método siempre devuelve MAPI_W_ERRORS_RETURNED, lo que indica que no hay opciones de destinatario para el destinatario en particular.
    
- **IAddrBook::QueryDefaultRecipOpt**: los proveedores de cliente y servicio MAPI ya no deben llamar a este método para recuperar propiedades que controlan las opciones de destinatarios de un tipo de dirección determinado. El método ya no devuelve un puntero a ninguna matriz de valores de propiedad.
    
## <a name="see-also"></a>Vea también



[Introducción a la Referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)

