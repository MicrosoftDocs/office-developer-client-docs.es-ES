---
title: Estrategias para el control de errores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b0ec3ada71a3e604ea71c5d386f1ff0466132081
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594092"
---
# <a name="strategies-for-error-handling"></a>Estrategias para el control de errores

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Debido a que los métodos de interfaz son virtuales, no es posible saber, como autor de la llamada, el conjunto completo de valores que se pueden devolver desde una llamada de prueba. Una implementación de un método podría devolver cinco valores; otro podría devolver ocho. Lista de las entradas de referencia en la documentación de MAPI unos valores que se pueden devolver para cada método; Estos son los valores que su proveedor de servicio o cliente puede comprobar y controlar porque tienen un significado especial. Se pueden devolver otros valores pero, debido a que no están significativas, no es necesario un código especial para controlar estos. Una comprobación sencilla para el éxito o el fracaso es la adecuada.
  
Algunos de los métodos de interfaz devuelven advertencias. Si un método que llama su proveedor de servicio o cliente puede devolver una advertencia, use la macro **HR_FAILED** para probar el valor devuelto en lugar de una comprobación para cero o distinto de cero. Advertencias, aunque no es cero, difieren de los códigos de error en que no tienen establecido el bit alto. Si su proveedor de cliente o servicio no usa la macro, es probable que podría confundir con una advertencia para un error. 
  
Aunque la mayoría de los métodos de interfaz y las funciones devuelven valores HRESULT, algunas funciones devuelven valores de tipo long sin signo. Además, algunos métodos que se usan en el entorno de MAPI proceden de COM y devuelven los valores de error de COM en lugar de los valores de error MAPI. Tenga en cuenta las siguientes instrucciones al realizar llamadas:
  
- Nunca se basan en o usar los valores devueltos de **IUnknown:: AddRef** o **IUnknown:: Release**. Estos valores devueltos son solo con fines de diagnóstico. 
    
- **IUnknown:: QueryInterface** siempre devuelve errores de COM genéricos donde la instalación es FACILITY_NULL o FACILITY_RPC, en lugar de los errores de MAPI. 
    
- Todos los otros métodos de interfaz devolución errores de interfaz MAPI con una instalación de FACILITY_ITF o FACILITY_RPC o FACILITY_NULL.
    
Cuando se realiza una llamada a un método MAPI no compatible, se puede devolver una de cuatro posibles errores: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

