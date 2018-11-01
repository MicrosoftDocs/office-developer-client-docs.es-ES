---
title: Tratar errores en Visual C++
TOCTitle: Handling Errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 937454a9277ec219f25a79074833138f6dd7f535
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887575"
---
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="9504e-102">Tratar errores en Visual C++</span><span class="sxs-lookup"><span data-stu-id="9504e-102">Handling Errors in Visual C++</span></span>


<span data-ttu-id="9504e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9504e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9504e-104">En COM, la mayoría de las operaciones devolverá un código de retorno HRESULT que indica si una función se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9504e-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="9504e-105">El \#directiva de importación genera código contenedor alrededor de cada método "sin procesar" o la propiedad y comprueba el HRESULT devuelto.</span><span class="sxs-lookup"><span data-stu-id="9504e-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="9504e-106">Si el HRESULT indica error, el código de contenedor genera un error COM llamando a \_com\_problema\_errorex() con el HRESULT devolver código como un argumento.</span><span class="sxs-lookup"><span data-stu-id="9504e-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="9504e-107">Objetos de error COM se pueden capturar en un bloque **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="9504e-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="9504e-108">(Para una mayor eficacia, detecte una referencia a un \_com\_objeto error.)</span><span class="sxs-lookup"><span data-stu-id="9504e-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="9504e-p102">Recuerde que se trata de errores de ADO: son el resultado de los errores de operaciones de ADO. Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="9504e-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="9504e-111">El \#directiva de importación sólo crea rutinas de tratamiento de errores para métodos y propiedades declarados en la DLL de ADO.</span><span class="sxs-lookup"><span data-stu-id="9504e-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="9504e-112">No obstante, puede sacar partido de este mismo mecanismo de control de errores escribiendo su propia macro o función en línea de comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="9504e-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="9504e-113">Vea ejemplos en el tema Extensiones de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9504e-113">See the topic Visual C++ Extensions for examples.</span></span>

