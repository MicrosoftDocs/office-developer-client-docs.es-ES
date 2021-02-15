---
title: Propiedad CommandTimeout (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296132"
---
# <a name="commandtimeout-property-ado"></a><span data-ttu-id="3896c-102">Propiedad CommandTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="3896c-102">CommandTimeout property (ADO)</span></span>


<span data-ttu-id="3896c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3896c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3896c-104">Indica el tiempo que se va a esperar durante la ejecución de un comando para que finalice el intento y se genere un error.</span><span class="sxs-lookup"><span data-stu-id="3896c-104">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3896c-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="3896c-105">Settings and return values</span></span>

<span data-ttu-id="3896c-106">Establece o devuelve un valor de tipo **Long** que indica, en segundos, cuánto tiempo se va a esperar a que se ejecute un comando.</span><span class="sxs-lookup"><span data-stu-id="3896c-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute.</span></span> <span data-ttu-id="3896c-107">El valor predeterminado es 30.</span><span class="sxs-lookup"><span data-stu-id="3896c-107">Default is 30.</span></span>

## <a name="remarks"></a><span data-ttu-id="3896c-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3896c-108">Remarks</span></span>

<span data-ttu-id="3896c-p102">Use la propiedad **CommandTimeout** de un objeto [Connection](connection-object-ado.md) o un objeto [Command](command-object-ado.md) para permitir la cancelación de una llamada al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) debido a una demora en el tráfico de red o a la sobrecarga del servidor. Si el intervalo establecido en la propiedad **CommandTimeout** transcurre antes de que finalice la ejecución del comando, se genera un error y ADO cancela el comando. Si se establece el valor de la propiedad en cero, ADO esperará indefinidamente a que finalice la ejecución. Asegúrese de que el proveedor y el origen de datos en el que está escribiendo código admiten la funcionalidad **CommandTimeout**.</span><span class="sxs-lookup"><span data-stu-id="3896c-p102">Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method call, due to delays from network traffic or heavy server use. If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command. If you set the property to zero, ADO will wait indefinitely until the execution is complete. Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.</span></span>

<span data-ttu-id="3896c-113">La configuración de **CommandTimeout** en un objeto **Connection** no afecta a la configuración de **CommandTimeout** en un objeto **Command** del mismo objeto **Connection**; es decir, la propiedad **CommandTimeout** del objeto **Command** no hereda el valor de la propiedad **CommandTimeout** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="3896c-113">The **CommandTimeout** setting on a **Connection** object has no effect on the **CommandTimeout** setting on a **Command** object on the same **Connection**; that is, the **Command** object's **CommandTimeout** property does not inherit the value of the **Connection** object's **CommandTimeout** value.</span></span>

<span data-ttu-id="3896c-114">En un objeto **Connection**, la propiedad **CommandTimeout** sigue siendo de lectura y escritura después de abrirse el objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="3896c-114">On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.</span></span>

