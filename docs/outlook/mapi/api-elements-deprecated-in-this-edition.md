---
title: Elementos de la API que se dejan de usar en esta edición
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: c70e89efba585183d2019bbda49102ecd14b9e20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816430"
---
# <a name="api-elements-deprecated-in-this-edition"></a>Elementos de la API que se dejan de usar en esta edición

  
  
**Hace referencia a**: Outlook 
  
Los siguientes elementos de la API están en desuso en Microsoft Outlook 2013. Ya no son compatibles y no se debe usar en los nuevos proyectos.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Tipo de proyectos de mensaje y opciones de destinatario

Los siguientes elementos de la API están en desuso en esta versión debido a un mensaje obsoleto y opciones de destinatario:
  
- **IXPLogon::RegisterOptions**: subsistema MAPI ya no se llama a este método para establecer los valores predeterminados para las opciones de mensaje y el destinatario de un proveedor de transporte.
    
- **OPTIONDATA**: esta estructura de datos que admiten las propiedades para las opciones de mensaje y el destinatario está obsoleta. El subsistema MAPI ya no se llama a **IXPLogon::RegisterOptions** para obtener las opciones destinatarios que es compatible con un proveedor de transporte para un tipo de dirección concreto o un mensaje. 
    
- **OPTIONCALLBACK**: este prototipo de función, que un proveedor de transporte se usa para declarar una función de devolución de llamada y que, a su vez, el subsistema MAPI se utiliza para resolver las propiedades del proveedor, es obsoleto. El subsistema MAPI ya no se llama a **IXPLogon::RegisterOptions** o usa cualquier función de devolución de llamada devuelto por el proveedor de transporte. 
    
- **MessageOptions**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para mostrar las propiedades o permiten a los usuarios establecer propiedades que controlan un tipo concreto de mensaje y la dirección. El método siempre devuelve MAPI_E_NOT_FOUND, lo que indica que no hay ninguna opción de mensaje para el mensaje concreto.
    
- **IMAPISession::QueryDefaultMessageOpt**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para recuperar las propiedades que controlan las opciones de mensajes para un tipo de dirección concreto. El método ya no devuelve un puntero a una matriz de valores de propiedad.
    
- **IAddrBook::RecipOptions**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para mostrar las propiedades o permiten a los usuarios establecer las propiedades que el procesamiento de control para un destinatario de un tipo de dirección concreto. El método siempre devuelve MAPI_W_ERRORS_RETURNED, que indica que no hay ninguna opción de destinatario para el destinatario determinado.
    
- **IAddrBook::QueryDefaultRecipOpt**: proveedores MAPI de cliente y el servicio ya no deben llamar a este método para recuperar las propiedades que controlan las opciones de destinatarios para un tipo de dirección concreto. El método ya no devuelve un puntero a una matriz de valores de propiedad.
    
## <a name="see-also"></a>Vea también



[Introducción a la referencia MAPI de Outlook](getting-started-with-the-outlook-mapi-reference.md)

