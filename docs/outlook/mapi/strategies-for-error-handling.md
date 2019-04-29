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
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424150"
---
# <a name="strategies-for-error-handling"></a>Estrategias para el control de errores

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como los métodos de interfaz son virtuales, no es posible saber, como autor de la llamada, el conjunto completo de valores que se pueden devolver desde una llamada. Una implementación de un método puede devolver cinco valores; otro puede devolver ocho. Las entradas de referencia de la lista de documentación de MAPI son algunos valores que se pueden devolver para cada método; Estos son los valores que su cliente o proveedor de servicios puede comprobar y controlar porque tienen significados especiales. Se pueden devolver otros valores, pero dado que no son significativos, el código especial para controlarlos no es necesario. Una comprobación sencilla de los éxitos o errores es adecuada.
  
Algunos de los métodos de la interfaz devuelven advertencias. Si un método que su cliente o proveedor de servicios llama puede devolver una advertencia, use la macro **HR_FAILED** para probar el valor devuelto en lugar de una comprobación de cero o distinto de cero. Las advertencias, aunque no son cero, difieren de los códigos de error en que no tienen el bit alto establecido. Si su cliente o proveedor de servicios no usa la macro, es probable que una advertencia se confunda con un error. 
  
Aunque la mayoría de los métodos y funciones de la interfaz devuelven valores HRESULT, algunas funciones devuelven valores largos sin signo. Además, algunos métodos utilizados en el entorno MAPI proceden de COM y devuelven valores de error de COM en lugar de valores de error de MAPI. Al realizar llamadas, tenga en cuenta las siguientes directrices:
  
- Nunca se basa o utiliza los valores devueltos de **IUnknown:: AddRef** o **IUnknown:: Release**. Estos valores devueltos son solo para fines de diagnóstico. 
    
- **IUnknown:: QueryInterface** siempre devuelve errores com genéricos donde la instalación es FACILITY_NULL o FACILITY_RPC, en lugar de errores de MAPI. 
    
- Todos los demás métodos de interfaz devuelven errores de interfaz MAPI con una instalación de FACILITY_ITF, o FACILITY_RPC o FACILITY_NULL.
    
Cuando se realiza una llamada a un método MAPI no admitido, se puede devolver uno de los cuatro posibles errores: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

