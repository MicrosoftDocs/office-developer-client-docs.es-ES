---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336501"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="61a43-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="61a43-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="61a43-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61a43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61a43-105">Contiene una matriz de estructuras **STnefProblem** que describen uno o más problemas de procesamiento que se produjeron durante la codificación o descodificación de una secuencia TNEF (Transport neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="61a43-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61a43-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="61a43-106">Header file:</span></span>  <br/> |<span data-ttu-id="61a43-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="61a43-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="61a43-108">Members</span><span class="sxs-lookup"><span data-stu-id="61a43-108">Members</span></span>

 <span data-ttu-id="61a43-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="61a43-109">**cProblem**</span></span>
  
> <span data-ttu-id="61a43-110">Número de elementos de la matriz especificada en el miembro **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="61a43-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="61a43-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="61a43-111">**aProblem**</span></span>
  
> <span data-ttu-id="61a43-112">Matriz de estructuras [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="61a43-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="61a43-113">Cada estructura contiene información sobre un problema de procesamiento de propiedades o atributos.</span><span class="sxs-lookup"><span data-stu-id="61a43-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="61a43-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61a43-114">Remarks</span></span>

<span data-ttu-id="61a43-115">Si se produce un problema durante el procesamiento de atributos o propiedades, un parámetro de salida en el método [ITnef:: ExtractProps](itnef-extractprops.md) y en el método [ITnef:: Finish](itnef-finish.md) recibe un puntero a una estructura **STnefProblemArray** y \*\*ExtractProps \*\*y **termina** cada vez que devuelven el valor MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="61a43-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="61a43-116">Este valor de error indica que surgió un problema durante el procesamiento y se ha generado una estructura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="61a43-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="61a43-117">Si no se genera una estructura **STnefProblem** durante el procesamiento de un atributo o una propiedad, la aplicación cliente puede continuar bajo el supuesto de que el procesamiento de ese atributo o propiedad se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="61a43-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="61a43-118">La única excepción se produce cuando el problema surgió durante la descodificación de un bloque de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="61a43-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="61a43-119">Si el error se produjo durante esta descodificación, MAPI_E_UNABLE_TO_COMPLETE puede devolverse como el [SCODE](scode.md) en la estructura.</span><span class="sxs-lookup"><span data-stu-id="61a43-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="61a43-120">En este caso, se detiene la descodificación del componente correspondiente al bloque y la descodificación continúa en otro componente.</span><span class="sxs-lookup"><span data-stu-id="61a43-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61a43-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="61a43-121">See also</span></span>



[<span data-ttu-id="61a43-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="61a43-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="61a43-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="61a43-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="61a43-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="61a43-124">MAPI Structures</span></span>](mapi-structures.md)

