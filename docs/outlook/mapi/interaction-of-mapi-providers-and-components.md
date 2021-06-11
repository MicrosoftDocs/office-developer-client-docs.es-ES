---
title: Interacción de los proveedores y componentes MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434665"
---
# <a name="interaction-of-mapi-providers-and-components"></a>Interacción de los proveedores y componentes MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de servicios MAPI de cualquier tipo deben seguir determinadas directrices para trabajar con otros componentes MAPI. Cada proveedor de servicios debe:
  
- Use el proveedor y los objetos de inicio de sesión adecuados para la inicialización.
    
- Devuelve una tabla de distribución de puntos de entrada del proveedor al sistema de mensajería tras la inicialización.
    
- Registre una fila de tabla de estado MAPI para cada recurso propiedad del proveedor y llame al método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) en el momento adecuado. 
    
- Use el [método IMAPISupport::NewUID](imapisupport-newuid.md) para obtener identificadores únicos (UID) válidos. 
    
- Admite las interfaces MAPI comunes en objetos que devuelve.
    
- Use las funciones de asignación de memoria MAPI para asignar la memoria devuelta a las aplicaciones cliente y liberar la memoria asignada por otras partes del subsistema MAPI.
    
- Mantenga una sección de perfil, si es necesario, para almacenar credenciales en el sistema de mensajería subyacente.
    
- Use el [método IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar las funciones de preprocesamiento de mensajes. 
    
- Incluya los archivos de encabezado adecuados (incluido mapispi.h) que definen constantes comunes, estructuras, interfaces y valores devueltos.
    
- Siga las convenciones de formato de dirección para tipos de direcciones comunes.
    

