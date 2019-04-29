---
title: Funciones asincrónicas definidas por el usuario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7fdf3bd09914981865c911fd65a78d044ad582f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412313"
---
# <a name="asynchronous-user-defined-functions"></a>Funciones asincrónicas definidas por el usuario

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 puede llamar a funciones definidas por el usuario de forma asincrónica. Llamar a las funciones de forma asincrónica puede mejorar el rendimiento al permitir que se ejecuten varios cálculos a la vez. Al ejecutar funciones definidas por el usuario en un clúster de cálculo, llamar a funciones asincrónicamente permite usar varios equipos para realizar los cálculos.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Cuándo se deben usar las funciones asincrónicas definidas por el usuario

Algunas funciones definidas por el usuario deben esperar recursos externos. Mientras esperan, se bloquea el subproceso de cálculo de Excel. En Excel 2013, las funciones definidas por el usuario pueden ejecutarse de forma asincrónica. Esto libera el subproceso de cálculo para que ejecute otros cálculos mientras la función definida por el usuario espera.
  
En Excel 2007, los programadores podían ejecutar varias funciones definidas por el usuario al mismo tiempo, aumentando el número de subprocesos que se usaban en los cálculos de varios subprocesos. Este método tiene inconvenientes principalmente porque el número de subprocesos es una configuración de ámbito de una aplicación y no puede controlarse en el nivel de una sola función o de un complemento.
  
Los programadores deben usar llamadas a funciones asincrónicas definidas por el usuario cuando la función debe esperar los recursos externos. Por ejemplo, una función que envía una solicitud SOAP a través de Internet debe esperar a que la red entregue la solicitud, al servidor remoto para completar la solicitud y a la red para que devuelva el resultado. En este caso, no se produce ninguna informática significativa y Excel puede continuar con otros cálculos.
  
Los programadores también pueden usar funciones asincrónicas definidas por el usuario cuando una función envía solicitudes a un clúster de cálculo. En este caso, no solo hay que esperar la latencia de red, pero el clúster puede ejecutar llamadas independientes en servidores independientes. Al no esperar a que termine cada llamada, las llamadas se pueden superponer para mejorar el rendimiento. En algunos casos, esta mejora es importante.
  
> [!NOTE]
> Las funciones definidas por el usuario no se pueden registrar como seguras tanto asincrónicas como de clúster. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Escritura de una función asincrónica definida por el usuario

Las funciones asincrónicas definidas por el usuario deben realizar un seguimiento de un controlador y usar dicho controlador cuando se informa a Excel de que la llamada a la función ha finalizado. Una función asincrónica definida por el usuario se divide en dos partes. La primera parte es el punto de entrada UDF estándar, que iniciará una segunda operación asincrónica independiente. Las deVoluciones de llamada en Excel deben realizarse durante el punto de entrada de UDF. La primera parte que se inicia de la función devolverá el control de su subproceso de cálculo a Excel, que continuará el cálculo. Una vez completada la segunda operación asincrónica, debe volver a llamar a Excel y proporcionar a Excel el resultado. 
  
> [!NOTE]
> Cualquier argumento que se pasa a la UDF que necesita la parte asincrónica la función debe copiarse en profundidad porque Excel libera estos argumentos cuando se devuelve el punto de entrada de la FDU. 
  
Excel proporciona un conjunto de eventos que un complemento XLL puede usar para administrar el ciclo de vida de las llamadas a UDF asincrónicas. Estos eventos indican que Excel ha finalizado con cálculos o que se ha cancelado el cálculo.
  
### <a name="declaring-an-asynchronous-function"></a>Declaración de una función asincrónica

Debe declarar las funciones definidas por el usuario asincrónicas como asincrónicas cuando se registran. Esto se lleva a cabo agregando un parámetro que apunta a una estructura XLOPER12, representada por "X" en la cadena de tipo de registro, en cualquier lugar de la lista de parámetros de UDF. Excel usa este parámetro para pasar el controlador de llamadas asincrónicas. El complemento XLL debe pasar el controlador de la llamada asincrónica y el resultado de la función de vuelta a Excel cuando el resultado está listo. Además, el tipo de valor devuelto de UDF debe ser **void**, designado por ">" como el primer carácter de la cadena de tipo. El tipo de valor devuelto es void porque la parte sincrónica del UDF no devuelve un valor a Excel. En su lugar, el complemento XLL devuelve un valor de forma asincrónica a través de una devolución de llamada. 
  
Puede declarar las funciones asincrónicas como seguras para subprocesos y, a continuación, se usa la parte sincrónica de UDF en un recálculo multiproceso. 
  
El siguiente ejemplo de código muestra una función definida por el usuario asincrónica registrada mediante "\>QX" como la cadena de tipo de registro:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Devolver valores

Cuando el resultado de la llamada asincrónica está listo, el complemento XLL devuelve el resultado a Excel realizando una devolución de llamada de tipo [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn** es la única devolución de llamada que puede usar en los subprocesos que no son de cálculo durante la actualización. Por lo tanto, la parte asincrónica de una UDF asincrónica no debe realizar ninguna otra devolución de llamada. 
  
### <a name="handling-events"></a>Administración de eventos

A partir de Excel 2010, los XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica. Para obtener más información, vea [controlar eventos](handling-events.md).
  
## <a name="see-also"></a>Ver también

- [Desarrollar archivos XLL de Excel](developing-excel-xlls.md)

