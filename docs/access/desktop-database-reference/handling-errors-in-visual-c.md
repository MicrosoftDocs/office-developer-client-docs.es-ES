---
title: Control de errores en Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292030"
---
# <a name="handling-errors-in-visual-c"></a><span data-ttu-id="ac59d-102">Control de errores en Visual C++</span><span class="sxs-lookup"><span data-stu-id="ac59d-102">Handling errors in Visual C++</span></span>


<span data-ttu-id="ac59d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac59d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac59d-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span><span class="sxs-lookup"><span data-stu-id="ac59d-104">In COM, most operations return an HRESULT return code that indicates whether a function completed successfully.</span></span> <span data-ttu-id="ac59d-105">La \#Directiva de importación genera código de contenedor alrededor de cada método o propiedad "sin procesar" y comprueba el HRESULT devuelto.</span><span class="sxs-lookup"><span data-stu-id="ac59d-105">The \#import directive generates wrapper code around each "raw" method or property and checks the returned HRESULT.</span></span> <span data-ttu-id="ac59d-106">Si el HRESULT indica un error, el código de contenedor produce un error COM al \_llamar\_a\_errorex () con el código de retorno HRESULT como un argumento.</span><span class="sxs-lookup"><span data-stu-id="ac59d-106">If the HRESULT indicates failure, the wrapper code throws a COM error by calling \_com\_issue\_errorex() with the HRESULT return code as an argument.</span></span> <span data-ttu-id="ac59d-107">Los objetos de error COM se pueden capturar en un bloque **try-catch** .</span><span class="sxs-lookup"><span data-stu-id="ac59d-107">COM error objects can be caught in a **try-catch** block.</span></span> <span data-ttu-id="ac59d-108">(Por motivos de eficacia, Capture una referencia a un \_objeto\_de error com).</span><span class="sxs-lookup"><span data-stu-id="ac59d-108">(For efficiency's sake, catch a reference to a \_com\_error object.)</span></span>

<span data-ttu-id="ac59d-p102">Recuerde que se trata de errores de ADO: son el resultado de los errores de operaciones de ADO. Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="ac59d-p102">Remember, these are ADO errors: they result from the ADO operation failing. Errors returned by the underlying provider appear as **Error** objects in the **Connection** object's **Errors** collection.</span></span>

<span data-ttu-id="ac59d-111">La \#Directiva de importación sólo crea rutinas de tratamiento de errores para métodos y propiedades declarados en la. dll de ADO.</span><span class="sxs-lookup"><span data-stu-id="ac59d-111">The \#import directive only creates error-handling routines for methods and properties declared in the ADO .dll.</span></span> <span data-ttu-id="ac59d-112">No obstante, puede sacar partido de este mismo mecanismo de control de errores escribiendo su propia macro o función en línea de comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="ac59d-112">However, you can take advantage of this same error-handling mechanism by writing your own error-checking macro or inline function.</span></span> <span data-ttu-id="ac59d-113">Vea ejemplos en el tema Extensiones de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="ac59d-113">See the topic Visual C++ Extensions for examples.</span></span>

