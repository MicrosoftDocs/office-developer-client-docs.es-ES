---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816990"
---
# <a name="hexfrombin"></a><span data-ttu-id="fbb9c-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="fbb9c-103">HexFromBin</span></span>

  
  
<span data-ttu-id="fbb9c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbb9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbb9c-105">Convierte a un número binario en una representación de cadena de un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fbb9c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fbb9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="fbb9c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fbb9c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fbb9c-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="fbb9c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fbb9c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fbb9c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fbb9c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="fbb9c-110">Called by:</span></span>  <br/> |<span data-ttu-id="fbb9c-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="fbb9c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="fbb9c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbb9c-112">Parameters</span></span>

 <span data-ttu-id="fbb9c-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="fbb9c-113">_pb_</span></span>
  
> <span data-ttu-id="fbb9c-114">[entrada] Puntero a los datos binarios que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="fbb9c-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="fbb9c-115">_cb_</span></span>
  
> <span data-ttu-id="fbb9c-116">[entrada] Tamaño, en bytes, de los datos binarios que señala el parámetro _pb_ .</span><span class="sxs-lookup"><span data-stu-id="fbb9c-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="fbb9c-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="fbb9c-117">_sz_</span></span>
  
> <span data-ttu-id="fbb9c-118">[out] Puntero a una cadena de ASCII terminada en null que representa los datos binarios de dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fbb9c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbb9c-119">Return value</span></span>

<span data-ttu-id="fbb9c-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fbb9c-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbb9c-121">Remarks</span></span>

<span data-ttu-id="fbb9c-122">La función **HexFromBin** toma un puntero a una unidad de datos binarios cuyo tamaño es indicada por el parámetro _cb_ .</span><span class="sxs-lookup"><span data-stu-id="fbb9c-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="fbb9c-123">Devuelve en la cadena _sz_ , comprendido en (2 \* _cb_) + 1 bytes de memoria, una representación de esta información binaria en números hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="fbb9c-124">Si el valor de tipo byte es 10 decimal, por ejemplo, la cadena hexadecimal será 0A, es así de un byte se convierte en dos bytes en la cadena.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

