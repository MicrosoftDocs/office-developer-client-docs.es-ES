---
title: Especificación de subprocesos por procesador en IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308592"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Especificación de subprocesos por procesador en IIS


**Se aplica a:** Access 2013, Office 2013

Al usar RDS con Internet Information Services 4.0 o posterior, el número de subprocesos creados por procesador se puede controlar manipulando el Registro en el servidor web. El número de subprocesos por procesador puede afectar al rendimiento en una situación de tráfico elevado o en situaciones de poco tráfico con tamaños de consultas grandes. El usuario debería experimentar para obtener los mejores resultados.

El método utilizado para determinar y cambiar el valor predeterminado de esta configuración depende de la configuración del servidor de IIS 4.0.

Con MDAC 2.1.2.4202.3 (GA), o una versión posterior, instalado en el servidor de IIS, RDS utiliza el mismo agrupamiento de subprocesos para Servicios de componentes (o Microsoft Transaction Services, si está utilizando NT de Windows) que las secuencias de comandos ASP. El valor predeterminado del número de subprocesos por procesador es 10. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor:

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

donde *MaxPoolThreads* es un \_ REG DWORD. *MaxPoolThreads* no aparece en el Registro hasta que se agrega específicamente. Los valores válidos varían entre 5 y un máximo recomendado de 20. Si el valor especificado por la clave del Registro es mayor que el valor de la clave *PoolThreadLimit* (ubicada en la misma ruta de acceso), se utilizará el valor de *PoolThreadLimit*.

Como alternativa, si MDAC 2.1 2.1.1.3711.11 (GA), o una versión anterior, está instalado en el servidor IIS, el valor predeterminado para el número de subprocesos por procesador es 6. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor IIS:

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

donde *ADCThreads* es un \_ REG DWORD. *ADCThreads* no aparece en el Registro hasta que se agrega específicamente. El intervalo de valores válido es de 1 a 50. Si el valor especificado por la clave del Registro es mayor que 50, entonces se utiliza el valor máximo (50).

