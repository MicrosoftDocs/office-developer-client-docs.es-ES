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
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="311f3-102">Especificar subprocesos por procesador en IIS</span><span class="sxs-lookup"><span data-stu-id="311f3-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="311f3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="311f3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="311f3-p101">Cuando se usa RDS con Internet Information Services 4.0 o una versión posterior, el número de subprocesos creados por procesador se puede controlar manipulando el Registro en el servidor web. El número de subprocesos por procesador puede afectar al rendimiento en una situación de tráfico elevado o en situaciones de poco tráfico con tamaños de consultas grandes. El usuario debería experimentar para obtener los mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="311f3-p101">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server. The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes. The user should experiment for best results.</span></span>

<span data-ttu-id="311f3-107">El método utilizado para determinar y cambiar el valor predeterminado de esta configuración depende de la configuración del servidor de IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="311f3-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="311f3-p102">Con MDAC 2.1.2.4202.3 (GA), o una versión posterior, instalado en el servidor de IIS, RDS utiliza el mismo agrupamiento de subprocesos para Servicios de componentes (o Microsoft Transaction Services, si está utilizando NT de Windows) que las secuencias de comandos ASP. El valor predeterminado del número de subprocesos por procesador es 10. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor:</span><span class="sxs-lookup"><span data-stu-id="311f3-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="311f3-111">donde *MaxPoolThreads* es un REG\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="311f3-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="311f3-112">*MaxPoolThreads* no aparece en el registro hasta que se agrega específicamente.</span><span class="sxs-lookup"><span data-stu-id="311f3-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="311f3-113">Los valores válidos varían entre 5 y un máximo recomendado de 20.</span><span class="sxs-lookup"><span data-stu-id="311f3-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="311f3-114">Si el valor especificado por la clave del registro es mayor que el valor de la clave *PoolThreadLimit* (que se encuentra en la misma ruta de acceso), se usa el valor de *PoolThreadLimit* .</span><span class="sxs-lookup"><span data-stu-id="311f3-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="311f3-p104">Como alternativa, si MDAC 2.1 2.1.1.3711.11 (GA), o una versión anterior, está instalado en el servidor IIS, el valor predeterminado para el número de subprocesos por procesador es 6. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor IIS:</span><span class="sxs-lookup"><span data-stu-id="311f3-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="311f3-117">donde *ADCThreads* es un REG\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="311f3-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="311f3-118">*ADCThreads* no aparece en el registro hasta que se agrega específicamente.</span><span class="sxs-lookup"><span data-stu-id="311f3-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="311f3-119">El intervalo de valores válido es de 1 a 50.</span><span class="sxs-lookup"><span data-stu-id="311f3-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="311f3-120">Si el valor especificado por la clave del Registro es mayor que 50, entonces se utiliza el valor máximo (50).</span><span class="sxs-lookup"><span data-stu-id="311f3-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>
