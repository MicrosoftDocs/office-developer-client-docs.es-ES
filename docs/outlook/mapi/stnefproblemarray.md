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
ms.openlocfilehash: baa2ac2e859b42234fcb07dd2bf521424ef9b465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820789"
---
# <a name="stnefproblemarray"></a><span data-ttu-id="4d2b2-103">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="4d2b2-103">STnefProblemArray</span></span>

  
  
<span data-ttu-id="4d2b2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d2b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d2b2-105">Contiene una matriz de estructuras **STnefProblem** que describe uno o varios problemas que se ha producido durante la codificación de procesamiento o descodificación de una secuencia de formato de encapsulación neutro de transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="4d2b2-105">Contains an array of **STnefProblem** structures describing one or more processing problems that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d2b2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4d2b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="4d2b2-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="4d2b2-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a><span data-ttu-id="4d2b2-108">Members</span><span class="sxs-lookup"><span data-stu-id="4d2b2-108">Members</span></span>

 <span data-ttu-id="4d2b2-109">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="4d2b2-109">**cProblem**</span></span>
  
> <span data-ttu-id="4d2b2-110">Recuento de elementos de la matriz especificada en el miembro **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="4d2b2-110">Count of elements in the array specified in the **aProblem** member.</span></span> 
    
 <span data-ttu-id="4d2b2-111">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="4d2b2-111">**aProblem**</span></span>
  
> <span data-ttu-id="4d2b2-112">Matriz de estructuras [STnefProblem](stnefproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="4d2b2-112">Array of [STnefProblem](stnefproblem.md) structures.</span></span> <span data-ttu-id="4d2b2-113">Cada estructura contiene información acerca de una propiedad o un problema de procesamiento del atributo.</span><span class="sxs-lookup"><span data-stu-id="4d2b2-113">Each structure contains information about a property or attribute processing problem.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4d2b2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d2b2-114">Remarks</span></span>

<span data-ttu-id="4d2b2-115">Si se produce un problema durante atributo o el procesamiento de propiedad, un parámetro de salida en el método [ITnef::ExtractProps](itnef-extractprops.md) y en el método [ITnef::Finish](itnef-finish.md) recibir un puntero a una estructura **STnefProblemArray** y **ExtractProps **y **Finalizar** cada devuelven el valor MAPI_W_ERRORS_RETURNED.</span><span class="sxs-lookup"><span data-stu-id="4d2b2-115">If a problem occurs during attribute or property processing, an output parameter in the [ITnef::ExtractProps](itnef-extractprops.md) method and in the [ITnef::Finish](itnef-finish.md) method each receive a pointer to an **STnefProblemArray** structure and **ExtractProps** and **Finish** each return the value MAPI_W_ERRORS_RETURNED.</span></span> <span data-ttu-id="4d2b2-116">Este valor de error indica que un problema surgieron durante el procesamiento y se ha generado una estructura **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="4d2b2-116">This error value indicates that a problem arose during processing and an **STnefProblemArray** structure was generated.</span></span> 
  
<span data-ttu-id="4d2b2-117">Si no se genera una estructura de **STnefProblem** durante el procesamiento de un atributo o propiedad, la aplicación cliente puede continuar en la suposición de que se ha realizado correctamente en el procesamiento de ese atributo o propiedad.</span><span class="sxs-lookup"><span data-stu-id="4d2b2-117">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the client application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="4d2b2-118">La única excepción se produce cuando surgió el problema durante la descodificación de un bloque de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="4d2b2-118">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="4d2b2-119">Si se produjo el error durante este proceso de descodificación, se puede devolver MAPI_E_UNABLE_TO_COMPLETE como el [SCODE](scode.md) en la estructura.</span><span class="sxs-lookup"><span data-stu-id="4d2b2-119">If the error occurred during this decoding, MAPI_E_UNABLE_TO_COMPLETE can be returned as the [SCODE](scode.md) in the structure.</span></span> <span data-ttu-id="4d2b2-120">En este caso, la descodificación del componente correspondiente al bloque se ha detenido y descodificación continúa en otro componente.</span><span class="sxs-lookup"><span data-stu-id="4d2b2-120">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d2b2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d2b2-121">See also</span></span>



[<span data-ttu-id="4d2b2-122">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="4d2b2-122">STnefProblem</span></span>](stnefproblem.md)
  
[<span data-ttu-id="4d2b2-123">SCODE</span><span class="sxs-lookup"><span data-stu-id="4d2b2-123">SCODE</span></span>](scode.md)


[<span data-ttu-id="4d2b2-124">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="4d2b2-124">MAPI Structures</span></span>](mapi-structures.md)

