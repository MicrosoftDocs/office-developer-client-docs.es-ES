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
  
Microsoft Excel 2013 puede llamar a funciones definidas por el usuario de forma asincrónica. Las funciones de llamada de forma asincrónica pueden mejorar el rendimiento al permitir que varios cálculos se ejecuten al mismo tiempo. Al ejecutar funciones definidas por el usuario en un clúster de cálculo, llamar a funciones asincrónicamente permite usar varios equipos para realizar los cálculos.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Cuándo usar funciones asincrónicas definidas por el usuario

Algunas funciones definidas por el usuario deben esperar recursos externos. Mientras esperan, se bloquea el Excel de cálculo. En Excel 2013, las funciones definidas por el usuario pueden ejecutarse de forma asincrónica. Esto libera el subproceso de cálculo para ejecutar otros cálculos mientras espera la función definida por el usuario.
  
En Excel 2007, los programadores podían ejecutar varias funciones definidas por el usuario al mismo tiempo al aumentar el número de subprocesos usados en las recálculos de varios subprocesos. Este método tiene inconvenientes principalmente porque el número de subprocesos es una configuración con ámbito para una aplicación y no se puede controlar en el nivel de una sola función o un complemento.
  
Los programadores deben usar llamadas de función asincrónicas definidas por el usuario cuando la función debe esperar recursos externos. Por ejemplo, una función que envía una solicitud SOAP a través de Internet debe esperar a que la red entregue la solicitud, el servidor remoto para completar la solicitud y la red para devolver el resultado. En este caso, no se produce ninguna informática significativa y Excel puede continuar con otros cálculos.
  
Los programadores también pueden usar funciones asincrónicas definidas por el usuario cuando una función envía solicitudes a un clúster de cálculo. En este caso, no solo hay que esperar la latencia de red, sino que el clúster puede ejecutar llamadas independientes en servidores independientes. Al no esperar a que finalice cada llamada, las llamadas se pueden superponer para mejorar el rendimiento. En algunos casos, esta mejora es significativa.
  
> [!NOTE]
> Las funciones definidas por el usuario no se pueden registrar como asincrónicas y seguras para clústeres. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Escritura de una función asincrónica definida por el usuario

Las funciones asincrónicas definidas por el usuario deben realizar un seguimiento de un identificador y usarlo al informar Excel que la llamada de función ha finalizado. Una función asincrónica definida por el usuario se divide en dos partes. La primera parte es el punto de entrada UDF estándar, que iniciará una segunda operación asincrónica independiente. Las devoluciones de llamada Excel deben realizarse durante el punto de entrada udf. La primera parte de inicio de la función devolverá el control de su subproceso de cálculo a Excel, que continuará el cálculo. Una vez completada la segunda operación asincrónica, debe volver a llamar a Excel y proporcionar Excel su resultado. 
  
> [!NOTE]
> Los argumentos pasados a la UDF que sean necesarios para la parte asincrónica, la función debe copiarse en profundidad porque Excel libera estos argumentos cuando devuelve el punto de entrada UDF. 
  
Excel proporciona un conjunto de eventos que un complemento XLL puede usar para administrar el ciclo de vida de las llamadas UDF asincrónicas. Estos eventos indican que Excel ha terminado con los cálculos o que el cálculo se ha cancelado.
  
### <a name="declaring-an-asynchronous-function"></a>Declarar una función asincrónica

Debe declarar funciones asincrónicas definidas por el usuario como asincrónicas cuando se registren. Esto se realiza agregando un parámetro que apunta a una estructura XLOPER12, representada por "X" en la cadena de tipo de registro, en cualquier lugar de la lista de parámetros UDF. Excel este parámetro para pasar el identificador de llamada asincrónica. El complemento XLL debe pasar el identificador de llamada asincrónica y el resultado de la función de nuevo a Excel cuando el resultado esté listo. Además, el tipo devuelto de la UDF debe ser **void**, designado por ">" como el primer carácter de la cadena de tipo. El tipo devuelto es void porque la parte sincrónica de la UDF no devuelve un valor a Excel. En su lugar, el complemento XLL devuelve un valor de forma asincrónica a través de una devolución de llamada. 
  
Puede declarar funciones asincrónicas como seguras para subprocesos y, a continuación, la parte sincrónica de la UDF se usa en una actualización multiproceso. 
  
En el siguiente ejemplo de código se muestra una función asincrónica definida por el usuario registrada mediante \> "QX" como cadena de tipo de registro:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Devolver valores

Cuando el resultado de la llamada asincrónica está listo, el complemento XLL devuelve el resultado a Excel realizando una devolución de llamada de tipo [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn es** la única devolución de llamada que puedes usar en subprocesos que no son de cálculo durante el recálculo. Por lo tanto, la parte asincrónica de una UDF asincrónica no debe realizar ninguna otra devolución de llamada. 
  
### <a name="handling-events"></a>Administración de eventos

A partir Excel 2010, los XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica. Para obtener más información, vea [Handling Events](handling-events.md).
  
## <a name="see-also"></a>Vea también

- [Desarrollar archivos XLL de Excel](developing-excel-xlls.md)

