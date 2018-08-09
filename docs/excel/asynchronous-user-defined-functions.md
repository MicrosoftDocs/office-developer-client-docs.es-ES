---
title: Funciones asincrónicas definidas por el usuario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b64dfd4308da4efb5e94010fe1dc9d758a1199c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815509"
---
# <a name="asynchronous-user-defined-functions"></a>Funciones asincrónicas definidas por el usuario

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 puede llamar a funciones definidas por el usuario de forma asincrónica. Llamar a funciones de forma asincrónica puede mejorar el rendimiento al permitir que varios cálculos ejecutar al mismo tiempo. Al ejecutar funciones definidas por el usuario en un clúster de cálculo, llamar a funciones de forma asincrónica permite que varios equipos que se usará para realizar los cálculos.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>Cuándo se deben usar funciones asincrónicas definidas por el usuario

Algunas funciones definidas por el usuario deben esperar a recursos externos. Mientras esperan, se bloquea el subproceso de cálculo de Excel. En Excel 2013, las funciones definidas por el usuario pueden ejecutar de forma asincrónica. Esto libera el subproceso de cálculo para ejecutar otros cálculos mientras espera a que la función definida por el usuario.
  
En Excel 2007, los programadores podrían ejecutar varias funciones definidas por el usuario al mismo tiempo mediante el aumento del número de subprocesos usados en los nuevos cálculos de varios subprocesos. Este método no tiene inconvenientes principalmente debido a que el número de subprocesos es una configuración de ámbito de una aplicación y no se puede controlar en el nivel de una sola función o un complemento.
  
Los programadores deben utilizar llamadas a la función definida por el usuario asincrónicas cuando la función debe esperar a recursos externos. Por ejemplo, una función que envía una solicitud SOAP a través de Internet debe esperar a la red entregar la solicitud, el servidor remoto para completar la solicitud y la red para devolver el resultado. En este caso, no hay ningún significativo los sistemas que se producen y Excel puede continuar con otros cálculos.
  
Los programadores también pueden utilizar funciones definidas por el usuario asincrónicas cuando una función es enviar solicitudes a un clúster de cálculo. En este caso, no es sólo la latencia de red que esperar, pero el clúster puede ejecutar llamadas independientes en servidores independientes. Si no se espera para que cada llamada a fin, pueden se pueden superponer las llamadas para mejorar el rendimiento. En algunos casos, esta mejora es significativa.
  
> [!NOTE]
> Funciones definidas por el usuario no pueden estar registradas como asincrónicos y seguras en clúster. 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>Escribir una función definida por el usuario asincrónica

Funciones asincrónicas definidas por el usuario deben realizar un seguimiento de un controlador y usar ese identificador al que le informa de Excel que se ha completado la llamada de función. Una función definida por el usuario asincrónica se divide en dos partes. La primera parte es el punto de entrada UDF estándar, que se iniciará una operación asincrónica en segundo lugar, independiente. Las devoluciones de llamada en Excel deben realizarse durante el punto de entrada UDF. La primera parte inicial de la función, a continuación, devolverá el control de su subproceso de cálculo en Excel, que seguirá cálculo. Una vez finalizada la segunda operación asincrónica, debe devolver la llamada en Excel y proporcionar a Excel con su resultado. 
  
> [!NOTE]
> Los argumentos que se pasan a la FDU que son necesarias para la parte asincrónica la función debe ser profunda copiado debido a que Excel libera estos argumentos cuando devuelve el punto de entrada UDF. 
  
Excel proporciona un conjunto de eventos que un complemento en el XLL puede utilizar con el fin de administrar el ciclo de vida de llamadas asincrónicas de UDF. Estos eventos indican que Excel ha finalizado con cálculos o que se ha cancelado el cálculo.
  
### <a name="declaring-an-asynchronous-function"></a>Declaración de una función asincrónica

Debe declarar funciones asincrónicas definidas por el usuario como asincrónica cuando se registren. Esto se realiza mediante la adición de un parámetro que apunta a una estructura XLOPER12, representado por "X" en la cadena de tipo de registro, en cualquier lugar en la lista de parámetros de una UDF. Excel utiliza este parámetro para pasar el identificador de llamada asincrónica. El complemento de XLL debe pasar el identificador de llamada asincrónica y el resultado de la función vuelva a Excel cuando esté listo el resultado. Además, el tipo de valor devuelto de la UDF debe ser **void**, designado por ">" como el primer carácter de la cadena de tipo. El tipo de valor devuelto es void debido a que la parte sincrónica de UDF no devuelve un valor a Excel. En su lugar, el complemento XLL devuelve un valor de forma asincrónica a través de una devolución de llamada. 
  
Puede declarar funciones asincrónicas como seguros para subprocesos y, a continuación, se usa el elemento sincrónico de las UDF en un nuevo cálculo multiproceso. 
  
En el ejemplo de código siguiente se muestra una función de definidas por el usuario asincrónica registrada mediante el uso de "\>px" como la cadena de tipo de registro:
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>Devolución de valores

Cuando el resultado de la llamada asincrónica está listo, el complemento XLL devuelve el resultado a Excel mediante la realización de una devolución de llamada de tipo [xlAsyncReturn](xlasyncreturn.md).
  
**xlAsyncReturn** es la devolución de llamada sólo que puede usar en subprocesos de cálculo que no sean durante la actualización. Por lo tanto, la parte asincrónica de una UDF asincrónica no debe realizar otras devoluciones de llamada. 
  
### <a name="handling-events"></a>Controlar eventos

Iniciar en Excel 2010, XLL pueden recibir eventos diseñados para administrar el ciclo de vida de la función asincrónica. Para obtener más información, vea [Controlar eventos](handling-events.md).
  
## <a name="see-also"></a>Vea también

- [Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

