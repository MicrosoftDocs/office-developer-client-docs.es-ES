---
title: Interacción de componentes y proveedores MAPI
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
# <a name="interaction-of-mapi-providers-and-components"></a>Interacción de componentes y proveedores MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los proveedores de servicios MAPI de cualquier tipo deben seguir ciertas instrucciones para trabajar con otros componentes de MAPI. Cada proveedor de servicios debe:
  
- Use el proveedor y los objetos de inicio de sesión adecuados para la inicialización.
    
- Devolver una tabla de distribución de puntos de entrada de proveedor al sistema de mensajería tras la inicialización.
    
- Registre una fila de tabla de estado de MAPI para cada recurso que posea el proveedor y llame al método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) en el momento adecuado. 
    
- Use el método [IMAPISupport:: NewUID](imapisupport-newuid.md) para obtener identificadores únicos válidos (UID). 
    
- Admite las interfaces MAPI comunes en los objetos que devuelve.
    
- Use las funciones de asignación de memoria MAPI para asignar la memoria devuelta a las aplicaciones cliente y para liberar la memoria asignada por otras partes del subsistema MAPI.
    
- Mantener una sección de perfil, si es necesario, para almacenar las credenciales en el sistema de mensajería subyacente.
    
- Use el método [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) para registrar las funciones de preprocesamiento de mensajes. 
    
- Incluya los archivos de encabezado apropiados (incluido mapispi. h) que definen constantes, estructuras, interfaces y valores devueltos comunes.
    
- Siga las convenciones de formato de dirección para tipos comunes de direcciones.
    

