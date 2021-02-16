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
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412579"
---
# <a name="hexfrombin"></a><span data-ttu-id="4cf02-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="4cf02-103">HexFromBin</span></span>

  
  
<span data-ttu-id="4cf02-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cf02-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cf02-105">Convierte un número binario en una representación de cadena de un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="4cf02-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cf02-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4cf02-106">Header file:</span></span>  <br/> |<span data-ttu-id="4cf02-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4cf02-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4cf02-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4cf02-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4cf02-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4cf02-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4cf02-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4cf02-110">Called by:</span></span>  <br/> |<span data-ttu-id="4cf02-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4cf02-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="4cf02-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cf02-112">Parameters</span></span>

 <span data-ttu-id="4cf02-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="4cf02-113">_pb_</span></span>
  
> <span data-ttu-id="4cf02-114">[entrada] Puntero a los datos binarios que se convertirán.</span><span class="sxs-lookup"><span data-stu-id="4cf02-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="4cf02-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="4cf02-115">_cb_</span></span>
  
> <span data-ttu-id="4cf02-116">[entrada] Tamaño, en bytes, de los datos binarios a los que apunta el _parámetro pb._</span><span class="sxs-lookup"><span data-stu-id="4cf02-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="4cf02-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="4cf02-117">_sz_</span></span>
  
> <span data-ttu-id="4cf02-118">[salida] Puntero a una cadena ASCII terminada en null que representa los datos binarios en dígitos hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="4cf02-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4cf02-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cf02-119">Return value</span></span>

<span data-ttu-id="4cf02-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4cf02-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cf02-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4cf02-121">Remarks</span></span>

<span data-ttu-id="4cf02-122">La **función HexFromBin** toma un puntero a una unidad de datos binarios cuyo tamaño se indica mediante el _parámetro cb._</span><span class="sxs-lookup"><span data-stu-id="4cf02-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="4cf02-123">Devuelve en la cadena  _sz,_ dentro de (2\*  _cb_)+1 bytes de memoria, una representación de esta información binaria en números hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="4cf02-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="4cf02-124">Si el valor de byte es decimal 10, por ejemplo, la cadena hexadecimal será 0A, por lo que un byte se convierte en dos bytes en la cadena.</span><span class="sxs-lookup"><span data-stu-id="4cf02-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

