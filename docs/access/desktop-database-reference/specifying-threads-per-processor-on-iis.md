---
title: Especificar subprocesos por procesador en IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5041eb32397fc9a234d0e4a0fff622f31b56a0a5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603360"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="e206f-102">Especificar subprocesos por procesador en IIS</span><span class="sxs-lookup"><span data-stu-id="e206f-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="e206f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e206f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e206f-104"><<<<<<< HEAD al utilizar RDS con servicios de Internet Information Server 4.0 o posterior, el número de subprocesos creados por procesador se puede controlar manipulando el registro en el servidor Web.</span><span class="sxs-lookup"><span data-stu-id="e206f-104"><<<<<<< HEAD When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the Web server.</span></span> <span data-ttu-id="e206f-105">El número de subprocesos por procesador puede afectar al rendimiento en una situación de tráfico elevado o en situaciones de poco tráfico con tamaños de consultas grandes.</span><span class="sxs-lookup"><span data-stu-id="e206f-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="e206f-106">El usuario debería experimentar para obtener los mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="e206f-106">The user should experiment for best results.</span></span>
<span data-ttu-id="e206f-107">=== Cuando se utiliza RDS con servicios de Internet Information Server 4.0 o posterior, el número de subprocesos creados por procesador se puede controlar manipulando el registro en el servidor web.</span><span class="sxs-lookup"><span data-stu-id="e206f-107">======= When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="e206f-108">El número de subprocesos por procesador puede afectar al rendimiento en una situación de tráfico elevado o en situaciones de poco tráfico con tamaños de consultas grandes.</span><span class="sxs-lookup"><span data-stu-id="e206f-108">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="e206f-109">El usuario debería experimentar para obtener los mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="e206f-109">The user should experiment for best results.</span></span>
>>>>>>> <span data-ttu-id="e206f-110">master</span><span class="sxs-lookup"><span data-stu-id="e206f-110">master</span></span>

<span data-ttu-id="e206f-111">El método utilizado para determinar y cambiar el valor predeterminado de esta configuración depende de la configuración del servidor de IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="e206f-111">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="e206f-p102">Con MDAC 2.1.2.4202.3 (GA), o una versión posterior, instalado en el servidor de IIS, RDS utiliza el mismo agrupamiento de subprocesos para Servicios de componentes (o Microsoft Transaction Services, si está utilizando NT de Windows) que las secuencias de comandos ASP. El valor predeterminado del número de subprocesos por procesador es 10. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor:</span><span class="sxs-lookup"><span data-stu-id="e206f-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="e206f-115">donde *MaxPoolThreads* es un REG\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="e206f-115">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="e206f-116">*MaxPoolThreads* no aparece en el registro hasta que se agrega específicamente.</span><span class="sxs-lookup"><span data-stu-id="e206f-116">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="e206f-117">Los valores válidos varían entre 5 y un máximo recomendado de 20.</span><span class="sxs-lookup"><span data-stu-id="e206f-117">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="e206f-118">Si el valor especificado por la clave del registro es mayor que el valor de la clave *PoolThreadLimit* (que se encuentra en la misma ruta de acceso), se usa el valor de *PoolThreadLimit* .</span><span class="sxs-lookup"><span data-stu-id="e206f-118">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="e206f-p104">Como alternativa, si MDAC 2.1 2.1.1.3711.11 (GA), o una versión anterior, está instalado en el servidor IIS, el valor predeterminado para el número de subprocesos por procesador es 6. Para cambiar este valor predeterminado, deberá agregar la clave siguiente al Registro del servidor IIS:</span><span class="sxs-lookup"><span data-stu-id="e206f-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="e206f-121">donde *ADCThreads* es un REG\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="e206f-121">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="e206f-122">*ADCThreads* no aparece en el registro hasta que se agrega específicamente.</span><span class="sxs-lookup"><span data-stu-id="e206f-122">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="e206f-123">El intervalo de valores válido es de 1 a 50.</span><span class="sxs-lookup"><span data-stu-id="e206f-123">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="e206f-124">Si el valor especificado por la clave del Registro es mayor que 50, entonces se utiliza el valor máximo (50).</span><span class="sxs-lookup"><span data-stu-id="e206f-124">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>

