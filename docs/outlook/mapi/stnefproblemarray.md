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
ms.openlocfilehash: 924ddbc7c2ad1ed84ce6927ae089b6eb223bfb92
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563509"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="e00ec-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="e00ec-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="e00ec-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e00ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e00ec-105">Contiene una matriz de estructuras **STnefProblem** que describe uno o varios problemas que se ha producido durante la codificación de procesamiento o descodificación de una secuencia de formato de encapsulación neutro de transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="e00ec-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e00ec-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e00ec-106">Header file:</span></span>  <br/> |<span data-ttu-id="e00ec-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="e00ec-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="e00ec-108">Members</span><span class="sxs-lookup"><span data-stu-id="e00ec-108">Members</span></span>

 <span data-ttu-id="e00ec-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="e00ec-109">**cProblem**</span></span>
  
> <span data-ttu-id="e00ec-110">Recuento de elementos de la matriz especificada en el miembro **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="e00ec-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="e00ec-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="e00ec-111">**aProblem**</span></span>
  
> <span data-ttu-id="e00ec-112">Matriz de estructuras [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="e00ec-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="e00ec-113">Cada estructura contiene información acerca de una propiedad o un problema de procesamiento del atributo.</span><span class="sxs-lookup"><span data-stu-id="e00ec-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e00ec-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e00ec-114">Remarks</span></span>

<span data-ttu-id="e00ec-115">Si se produce un problema durante atributo o el procesamiento de propiedad, un parámetro de salida en el método [ITnef::ExtractProps](itnef-extractprops.md) y en el método [ITnef::Finish](itnef-finish.md) recibir un puntero a una estructura **STnefProblemArray** y **ExtractProps **y **Finalizar** cada devuelven el valor MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="e00ec-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="e00ec-116">Este valor de error indica que un problema surgieron durante el procesamiento y se ha generado una estructura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="e00ec-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="e00ec-117">Si no se genera una estructura de **STnefProblem** durante el procesamiento de un atributo o propiedad, la aplicación cliente puede continuar en la suposición de que se ha realizado correctamente en el procesamiento de ese atributo o propiedad.</span><span class="sxs-lookup"><span data-stu-id="e00ec-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="e00ec-118">La única excepción se produce cuando surgió el problema durante la descodificación de un bloque de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="e00ec-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="e00ec-119">Si se produjo el error durante este proceso de descodificación, se puede devolver MAPI_E_UNABLE_TO_COMPLETE como el [SCODE](scode.md) en la estructura.</span><span class="sxs-lookup"><span data-stu-id="e00ec-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="e00ec-120">En este caso, la descodificación del componente correspondiente al bloque se ha detenido y descodificación continúa en otro componente.</span><span class="sxs-lookup"><span data-stu-id="e00ec-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e00ec-121">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e00ec-121">See also</span></span>



[<span data-ttu-id="e00ec-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="e00ec-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="e00ec-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="e00ec-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="e00ec-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="e00ec-124">MAPI Structures</span></span>](mapi-structures.md)

