---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: e7b3774d8dce446f0e87f041f11dac607f464680
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820856"
---
# <a name="tchar"></a><span data-ttu-id="b2db7-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="b2db7-103">TCHAR</span></span>

  
  
<span data-ttu-id="b2db7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2db7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2db7-105">Una cadena de caracteres Win32 que puede utilizarse para describir las cadenas ANSI, DBCS o Unicode.</span><span class="sxs-lookup"><span data-stu-id="b2db7-105">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings.</span></span> <span data-ttu-id="b2db7-106">Para las plataformas ANSI y DBCS, TCHAR se define como sigue:</span><span class="sxs-lookup"><span data-stu-id="b2db7-106">For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="b2db7-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2db7-107">Remarks</span></span>

<span data-ttu-id="b2db7-108">Para las plataformas Unicode, TCHAR se define como sinónimos con el tipo de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="b2db7-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="b2db7-109">Los clientes MAPI pueden usar el tipo de datos TCHAR para representar una cadena del tipo de la WCHAR o char.</span><span class="sxs-lookup"><span data-stu-id="b2db7-109">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type.</span></span> <span data-ttu-id="b2db7-110">Asegúrese de definir el UNICODE constante simbólico y limitar la plataforma cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="b2db7-110">Be sure to define the symbolic constant UNICODE and limit the platform when it is required.</span></span> <span data-ttu-id="b2db7-111">MAPI interpretará la información de la plataforma y traducir internamente TCHAR por la cadena apropiada.</span><span class="sxs-lookup"><span data-stu-id="b2db7-111">MAPI will interpret the platform information and internally translate TCHAR to the appropriate string.</span></span> <span data-ttu-id="b2db7-112">El tipo de propiedad MAPI, PT_TSTRING, funciona igual que el tipo de datos TCHAR.</span><span class="sxs-lookup"><span data-stu-id="b2db7-112">The MAPI property type, PT_TSTRING, works just like the TCHAR data type.</span></span> <span data-ttu-id="b2db7-113">Cuando la plataforma es compatible con Unicode, las propiedades de tipo PT_TSTRING se asignan al tipo PT_UNICODE en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="b2db7-113">When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time.</span></span> <span data-ttu-id="b2db7-114">Cuando la plataforma no es compatible con Unicode, estas propiedades se asignan al tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="b2db7-114">When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="b2db7-115">Para obtener más información acerca de esta funcionalidad, vea [Conjuntos de caracteres](mapi-character-sets.md) y la [Lista de tipos de propiedad](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b2db7-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2db7-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2db7-116">See also</span></span>



[<span data-ttu-id="b2db7-117">Tipos de datos MAPI</span><span class="sxs-lookup"><span data-stu-id="b2db7-117">MAPI Data Types</span></span>](mapi-data-types.md)

