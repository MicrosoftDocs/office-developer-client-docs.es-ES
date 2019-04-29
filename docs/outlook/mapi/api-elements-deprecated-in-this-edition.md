---
title: Elementos de la API en desuso en esta edición
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
# <a name="api-elements-deprecated-in-this-edition"></a>Elementos de la API en desuso en esta edición

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los siguientes elementos de la API están en desuso en Microsoft Outlook 2013. Ya no se admiten y no se deben usar en nuevos proyectos.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Desuso de las opciones de mensajes y destinatarios

Los siguientes elementos de la API están en desuso en esta versión debido a las opciones obsoletas de los mensajes y los destinatarios:
  
- **IXPLogon:: RegisterOptions**: el subsistema MAPI ya no llama a este método para establecer los valores predeterminados de las opciones de mensajes y destinatarios de un proveedor de transporte.
    
- **OPTIONDATA**: esta estructura de datos que admitía propiedades para las opciones de mensajes y destinatarios está obsoleta. El subsistema MAPI ya no llama a **IXPLogon:: RegisterOptions** para obtener las opciones de mensajes o destinatarios admitidas por un proveedor de transporte para un tipo de dirección en particular. 
    
- **OPTIONCALLBACK**: este prototipo de función, que un proveedor de transporte usó para declarar una función de devolución de llamada y que, a su vez, el subsistema MAPI usado para resolver las propiedades del proveedor, está obsoleto. El subsistema MAPI ya no llama a **IXPLogon:: RegisterOptions** o usa cualquier función de devolución de llamada devuelta por el proveedor de transporte. 
    
- **IMAPISession:: MessageOptions**: los proveedores de servicios y clientes MAPI ya no deben llamar a este método para mostrar las propiedades o permitir a los usuarios establecer las propiedades que controlan un mensaje y tipo de dirección determinados. El método siempre devuelve MAPI_E_NOT_FOUND, que indica que no hay opciones de mensaje para el mensaje en particular.
    
- **IMAPISession:: QueryDefaultMessageOpt**: los proveedores de servicios y clientes MAPI ya no deben llamar a este método para recuperar las propiedades que controlan las opciones de mensaje para un tipo de dirección determinado. El método ya no devuelve un puntero a una matriz de valores de propiedad.
    
- **IAddrBook:: RecipOptions**: los proveedores de servicios y clientes MAPI ya no deben llamar a este método para mostrar las propiedades o permitir a los usuarios establecer las propiedades que controlan el procesamiento de un destinatario de un tipo de dirección determinado. El método siempre devuelve MAPI_W_ERRORS_RETURNED, que indica que no hay opciones de destinatario para el destinatario en particular.
    
- **IAddrBook:: QueryDefaultRecipOpt**: los proveedores de servicios y clientes MAPI ya no deben llamar a este método para recuperar las propiedades que controlan las opciones de destinatario de un tipo de dirección en particular. El método ya no devuelve un puntero a una matriz de valores de propiedad.
    
## <a name="see-also"></a>Vea también



[Introducción a la Referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)

