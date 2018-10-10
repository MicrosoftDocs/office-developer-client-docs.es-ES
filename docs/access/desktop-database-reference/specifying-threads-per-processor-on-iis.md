---
title: Especificar subprocesos por procesador en IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483916"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Especificar subprocesos por procesador en IIS


**Se aplica a**: Access 2013 | Office 2013

Cuando se usa RDS con Internet Information Services 4.0 o una versión posterior, el número de subprocesos creados por procesador se puede controlar manipulando el Registro en el servidor web. El número de subprocesos por procesador puede afectar al rendimiento en una situación de tráfico elevado o en situaciones de poco tráfico con tamaños de consultas grandes. El usuario debería experimentar para obtener los mejores resultados.

El método utilizado para determinar y cambiar el valor predeterminado de esta configuración depende de la configuración del servidor de IIS 4.0.

Con MDAC 2.1.2.4202.3 (GA), o una versión posterior, instalado en el servidor de IIS, RDS utiliza el mismo agrupamiento de subprocesos para Servicios de componentes (o Microsoft Transaction Services, si está utilizando NT de Windows) que las secuencias de comandos ASP. El valor predeterminado del número de subprocesos por procesador es 10. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor:

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

donde *MaxPoolThreads* es un REG\_DWORD. *MaxPoolThreads* no aparece en el registro hasta que se agrega específicamente. Los valores válidos varían entre 5 y un máximo recomendado de 20. Si el valor especificado por la clave del registro es mayor que el valor de la clave *PoolThreadLimit* (que se encuentra en la misma ruta de acceso), se usa el valor de *PoolThreadLimit* .

Como alternativa, si MDAC 2.1 2.1.1.3711.11 (GA), o una versión anterior, está instalado en el servidor IIS, el valor predeterminado para el número de subprocesos por procesador es 6. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor IIS:

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

donde *ADCThreads* es un REG\_DWORD. *ADCThreads* no aparece en el registro hasta que se agrega específicamente. El intervalo de valores válido es de 1 a 50. Si el valor especificado por la clave del Registro es mayor que 50, entonces se utiliza el valor máximo (50).

