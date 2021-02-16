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
  
Dado que los métodos de interfaz son virtuales, no es posible saber, como llamador, el conjunto completo de valores que se pueden devolver desde cualquier llamada. Una implementación de un método puede devolver cinco valores; otro podría devolver ocho. Las entradas de referencia de la documentación mapi enumera algunos valores que se pueden devolver para cada método; estos son los valores que el cliente o el proveedor de servicios pueden comprobar y controlar porque tienen significados especiales. Se pueden devolver otros valores, pero como no son significativos, el código especial para controlar esos valores no es necesario. Una comprobación simple de éxito o fracaso es adecuada.
  
Algunos de los métodos de interfaz devuelven advertencias. Si un método al que llama el cliente o el proveedor de servicios puede devolver una advertencia, use la macro **HR_FAILED** para probar el valor devuelto en lugar de comprobar cero o distinto de cero. Las advertencias, aunque distintas de cero, difieren de los códigos de error en que no tienen el conjunto de bits altos. Si el cliente o el proveedor de servicios no usa la macro, es probable que una advertencia se pueda confundir con un error. 
  
Aunque la mayoría de los métodos y funciones de interfaz devuelven valores HRESULT, algunas funciones devuelven valores largos sin signo. Además, algunos métodos usados en el entorno MAPI provienen de COM y devuelven valores de error COM en lugar de valores de error MAPI. Tenga en cuenta las siguientes directrices al realizar llamadas:
  
- Nunca confíe ni use los valores devueltos de **IUnknown::AddRef** o **IUnknown::Release**. Estos valores devueltos son solo para fines de diagnóstico. 
    
- **IUnknown::QueryInterface** siempre devuelve errores COM genéricos en los que la FACILITY_NULL o FACILITY_RPC, en lugar de errores MAPI. 
    
- Todos los demás métodos de interfaz devuelven errores de interfaz MAPI con una FACILITY_ITF o FACILITY_RPC o FACILITY_NULL error.
    
Cuando se realiza una llamada a un método MAPI no compatible, se puede devolver uno de los cuatro errores posibles: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

